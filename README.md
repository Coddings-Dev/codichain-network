# ⛓️ CodiChain Network - Blockchain Pública

> **Repositório público da blockchain CodiChain - Estrutura de dados**

---

## 📂 Estrutura de Diretórios

```
codichain-network-old/
├── blocks/                    # Blocos da blockchain
│   └── {hash}.json
│
├── addresses/                 # Registro centralizado de endereços
│   └── {address}/
│       ├── info.json          # Informações do endereço
│       └── tokens/            # Saldos por token
│           └── {tokenId}.json
│
├── tokens/                    # Tokens
│   └── {tokenId}/
│       ├── contract.json     # Contrato do token
│       ├── transactions/      # Transações do token
│       │   └── {txId}.json
│       └── holders/           # Referências para addresses/
│           └── {address}.json
│
├── staking/                   # Staking locks
│   └── locks/
│       └── {lockId}.json
│
└── index/                     # Índices para busca rápida
    ├── addresses.json
    ├── tokens.json
    └── blocks.json
```

---

## 📄 Descrição das Pastas

### `blocks/`
Contém todos os blocos da blockchain. Cada bloco é um arquivo JSON nomeado pelo seu hash.

### `addresses/`
Registro centralizado de todos os endereços. Cada endereço tem:
- `info.json`: Informações gerais do endereço
- `tokens/`: Saldos do endereço por token

### `tokens/`
Contém todos os tokens criados na blockchain. Cada token tem:
- `contract.json`: Informações do token e lastreamento
- `transactions/`: Todas as transações do token
- `holders/`: Referências para endereços que possuem o token

### `staking/`
Contém locks de staking ativos.

### `index/`
Índices para busca rápida de endereços, tokens e blocos.

---

## 🔄 Como Funciona

1. **Transações** são salvas em `tokens/{tokenId}/transactions/`
2. **Saldos** são atualizados em `addresses/{address}/tokens/{tokenId}.json`
3. **Referências** são atualizadas em `tokens/{tokenId}/holders/{address}.json`
4. **Blocos** são criados em `blocks/{hash}.json`
5. **Índices** são atualizados em `index/`

---

## 📝 Convenções

- Endereços são normalizados (sem `0x`, minúsculas)
- Cada arquivo é JSON formatado
- Commits no Git representam blocos
- Todos os arquivos são versionados no Git

---

**Versão**: 1.0.0  
**Última Atualização**: 2024-12-01
