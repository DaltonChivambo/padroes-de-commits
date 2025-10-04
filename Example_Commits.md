# Conventional Commits Guide

Este guia mostra os tipos de commits recomendados pelo padrão **Conventional Commits**, com explicações, exemplos e como usar com `git commit -m`.

---

## 📌 Tipos de Commits

### 🔹 feat

* **Descrição:** Adição de nova funcionalidade.
* **Exemplo:**

```bash
git commit -m ":sparkles: feat: add user authentication with JWT"
```

### 🔹 fix

* **Descrição:** Correção de bug.
* **Exemplo:**

```bash
git commit -m ":bug: fix: resolve null pointer in login service"
```

### 🔹 docs

* **Descrição:** Alterações na documentação (README, Wiki, comentários).
* **Exemplo:**

```bash
git commit -m ":books: docs: update README with installation guide"
```

### 🔹 style

* **Descrição:** Mudanças apenas de formatação/estilo, sem alterar comportamento.
* **Exemplo:**

```bash
git commit -m ":art: style: format code using black"
```

### 🔹 refactor

* **Descrição:** Alterações internas no código sem mudar o comportamento.
* **Exemplo:**

```bash
git commit -m ":recycle: refactor: simplify database connection logic"
```

### 🔹 perf

* **Descrição:** Melhorias de performance.
* **Exemplo:**

```bash
git commit -m ":zap: perf: optimize query performance with index"
```

### 🔹 test

* **Descrição:** Adição ou alteração de testes.
* **Exemplo:**

```bash
git commit -m ":white_check_mark: test: add unit tests for user service"
```

### 🔹 build

* **Descrição:** Mudanças que afetam o build do projeto (dependências, compilação).
* **Exemplo:**

```bash
git commit -m ":package: build: update dependencies to latest versions"
```

### 🔹 ci

* **Descrição:** Mudanças em integração contínua (CI/CD, GitHub Actions, Jenkins).
* **Exemplo:**

```bash
git commit -m ":construction_worker: ci: add pipeline step for linting"
```

### 🔹 chore

* **Descrição:** Tarefas de manutenção que não afetam o código de produção.
* **Exemplo:**

```bash
git commit -m ":wrench: chore: add .env.example file"
```

### 🔹 revert

* **Descrição:** Reverter um commit anterior.
* **Exemplo:**

```bash
git commit -m ":rewind: revert: undo changes from commit abc123"
```

---

## ⚡ Ícones sugeridos para cada tipo

* `:sparkles:` → feat
* `:bug:` → fix
* `:books:` → docs
* `:art:` → style
* `:recycle:` → refactor
* `:zap:` → perf
* `:white_check_mark:` → test
* `:package:` → build
* `:construction_worker:` → ci
* `:wrench:` → chore
* `:rewind:` → revert

---

Este guia pode ser copiado para o README do seu projeto para padronizar os commits da equipe e manter o histórico organizado e legível.
