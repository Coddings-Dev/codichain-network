# ⛓️ CodiChain Network

> **A blockchain pública e gratuita no GitHub**

---

## 🌟 O Que É Isso?

Este repositório é a **blockchain pública da CodiChain**. Aqui você encontra todos os blocos, transações e tokens que foram criados na rede CodiChain.

### 💡 Conceito Simples

Imagine este repositório como um **livro-razão público** onde:
- ✅ Todas as transações são registradas
- ✅ Todos os blocos são armazenados
- ✅ Todos os tokens são definidos
- ✅ Qualquer pessoa pode verificar
- ✅ Nada pode ser alterado (imutável)

---

## 📁 O Que Você Vai Encontrar Aqui?

### 📦 `blocks/` - Os Blocos da Blockchain

Cada arquivo aqui representa um **bloco** da blockchain. Os blocos são como "páginas" do livro-razão, contendo várias transações agrupadas.

**Exemplo**: `blocks/0000abc123def456....json`

- Cada bloco tem um **hash único** (como uma impressão digital)
- O nome do arquivo é o próprio hash do bloco
- Isso garante que ninguém pode alterar um bloco sem ser detectado

**Por que isso é importante?**
- 🔒 **Segurança**: Se alguém tentar alterar um bloco, o hash muda e fica óbvio
- 🔍 **Verificação**: Qualquer um pode verificar se um bloco está correto
- 📚 **Histórico**: Todo o histórico da blockchain está aqui

---

### 🪙 `tokens/` - Os Tokens Criados

Aqui você encontra todos os **tokens** que foram criados na CodiChain. Cada token tem sua própria pasta com todas as informações.

**Estrutura de um token**:
```
tokens/
└── gametoken/
    ├── contract.json        # Informações do token (nome, símbolo, preço, etc)
    ├── transactions/       # Todas as transações deste token
    │   ├── tx-abc123.json
    │   └── tx-def456.json
    └── wallets/            # Saldos de cada endereço que possui este token
        ├── 0x1111....json
        └── 0x2222....json
```

**O que cada arquivo faz?**

1. **`contract.json`**: 
   - Informações básicas do token (nome, símbolo, supply total)
   - Preço atual e capitalização
   - Lastreamento (garantia em BRL)
   - Estatísticas (quantos holders, volume, etc)

2. **`transactions/`**:
   - Cada arquivo é uma transação
   - Mostra quem enviou, quem recebeu, quanto e quando
   - Histórico completo e verificável

3. **`wallets/`**:
   - Saldo atual de cada endereço
   - Histórico de movimentações
   - Informações de cada carteira

---

## 🔍 Como Funciona?

### 1. Transação Acontece

Quando alguém faz uma transação (envia tokens, compra, vende):
- A transação é salva em `tokens/{token}/transactions/tx-abc123.json`
- Os saldos são atualizados em `tokens/{token}/wallets/`
- O `contract.json` é atualizado (se necessário)

### 2. Bloco É Criado

Várias transações são agrupadas em um **bloco**:
- O bloco é salvo em `blocks/{hash}.json`
- Cada bloco tem um hash único (como uma impressão digital)
- Os blocos são encadeados (cada bloco referencia o anterior)

### 3. Commit no Git

Tudo é registrado no Git:
- Cada bloco vira um **commit** no Git
- O Git garante que nada pode ser alterado
- O GitHub torna tudo público e verificável

---

## 🎯 Por Que Isso É Importante?

### ✅ Transparência Total

- **Qualquer pessoa** pode ver todas as transações
- **Qualquer pessoa** pode verificar se está tudo correto
- **Nada é escondido** - tudo é público

### ✅ Segurança

- **Imutável**: Uma vez registrado, não pode ser alterado
- **Verificável**: Qualquer um pode verificar a integridade
- **Descentralizado**: Não depende de um servidor central

### ✅ Gratuito

- **100% gratuito**: Usa GitHub (gratuito)
- **Sem taxas**: Não precisa pagar para usar
- **Acessível**: Qualquer um pode acessar

---

## 🚀 Como Usar?

### Para Ver Transações

1. Vá em `tokens/{nome-do-token}/transactions/`
2. Abra qualquer arquivo `.json`
3. Veja os detalhes da transação

### Para Ver Saldos

1. Vá em `tokens/{nome-do-token}/wallets/`
2. Abra o arquivo do endereço que você quer verificar
3. Veja o saldo atual

### Para Ver Informações de um Token

1. Vá em `tokens/{nome-do-token}/contract.json`
2. Veja todas as informações do token:
   - Nome, símbolo, supply
   - Preço atual
   - Lastreamento
   - Estatísticas

### Para Ver Blocos

1. Vá em `blocks/`
2. Abra qualquer arquivo `.json`
3. Veja as transações que foram incluídas no bloco

---

## 🔒 Segurança e Integridade

### Como Verificar se Está Tudo Correto?

1. **Verificar Hash do Bloco**:
   - O nome do arquivo deve ser igual ao hash dentro do arquivo
   - Se não for, algo está errado

2. **Verificar Cadeia de Blocos**:
   - Cada bloco referencia o bloco anterior
   - Se a cadeia estiver quebrada, algo está errado

3. **Verificar Saldos**:
   - Os saldos devem bater com as transações
   - Se não bater, algo está errado

### O Que Garante a Segurança?

- ✅ **Git**: Histórico imutável
- ✅ **Hash**: Impressão digital de cada bloco
- ✅ **Assinatura GPG**: Commits assinados digitalmente
- ✅ **Público**: Qualquer um pode verificar

---

## 📊 Exemplos Práticos

### Exemplo 1: Ver uma Transação

```
1. Vá em: tokens/codicoin/transactions/tx-abc123.json
2. Veja:
   - Quem enviou: 0x1111...
   - Quem recebeu: 0x2222...
   - Quantidade: 100 CDC
   - Quando: 2024-12-01 10:30:00
```

### Exemplo 2: Ver Saldo de um Endereço

```
1. Vá em: tokens/codicoin/wallets/0x1111....json
2. Veja:
   - Saldo atual: 1000 CDC
   - Total recebido: 5000 CDC
   - Total enviado: 4000 CDC
   - Última transação: 2024-12-01
```

### Exemplo 3: Ver Informações de um Token

```
1. Vá em: tokens/gametoken/contract.json
2. Veja:
   - Nome: GameToken
   - Símbolo: GAME
   - Supply: 10.000 tokens
   - Preço: R$ 1,00
   - Lastreamento: R$ 1.000,00
   - Holders: 50 pessoas
```

---

## 🌐 Ecossistema

### CodiChain + CodiWallet

Este repositório é a **blockchain pública** (CodiChain Network). Ele funciona junto com:

- **CodiWallet**: Interface onde usuários criam tokens, fazem transações, etc
- **CodiChain API**: Backend que processa tudo e atualiza este repositório

**Fluxo**:
```
Usuário usa CodiWallet
    ↓
CodiChain API processa
    ↓
Atualiza este repositório (CodiChain Network)
    ↓
Tudo fica público e verificável
```

---

## 📈 Estatísticas

Você pode ver estatísticas da blockchain:

- **Total de blocos**: Quantos blocos foram criados
- **Total de transações**: Quantas transações foram feitas
- **Total de tokens**: Quantos tokens foram criados
- **Volume**: Quanto valor foi movimentado

Tudo isso está nos arquivos JSON deste repositório!

---

## 🤔 Perguntas Frequentes

### Posso Alterar Algo Aqui?

**Não!** Este repositório é **somente leitura** para todos, exceto o sistema CodiChain. Isso garante que ninguém pode alterar transações ou criar blocos falsos.

### Como Posso Verificar se Está Tudo Correto?

Você pode:
- Verificar os hashes dos blocos
- Verificar se os saldos batem com as transações
- Verificar se a cadeia de blocos está intacta

### O Que Acontece se Alguém Tentar Alterar?

- O hash do bloco mudaria
- A cadeia seria quebrada
- Ficaria óbvio que algo está errado
- O Git detectaria a alteração

### Posso Criar Meu Próprio Token?

Sim! Use o **CodiWallet** para criar seu token. Ele será registrado aqui automaticamente.

---

## 🔗 Links Úteis

- **CodiWallet**: [codicoin.coddings.com](https://codicoin.coddings.com)
- **Documentação**: [docs.codichain.coddings.com](https://docs.codichain.coddings.com)
- **API**: [api.codichain.coddings.com](https://api.codichain.coddings.com)

---

## 📝 Notas Importantes

### ⚠️ Este Repositório É Automático

- **Não edite manualmente**: Tudo é atualizado automaticamente pelo sistema
- **Não faça commits diretos**: O sistema faz isso automaticamente
- **Apenas leia**: Use para verificar e explorar

### ✅ Tudo É Público

- Todas as transações são públicas
- Todos os saldos são públicos
- Tudo pode ser verificado por qualquer pessoa

### 🔒 Mas É Seguro

- Ninguém pode alterar o que já foi registrado
- Tudo é verificado e assinado
- A integridade é garantida pelo Git

---

## 🎉 Conclusão

Este repositório é a **prova pública** de todas as transações, blocos e tokens da CodiChain. É transparente, seguro e verificável por qualquer pessoa.

**Explore, verifique e confie!** 🚀

---

<div align="center">

### ⛓️ CodiChain Network

**Transparente. Seguro. Público.**

Feito com ❤️ pela equipe Coddings

</div>

