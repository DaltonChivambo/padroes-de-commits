
# 🧭 Conventional Commits Guide — Guia Completo e Ampliado

Este guia descreve o padrão **Conventional Commits**, ajudando a manter um histórico de código **limpo, legível e automatizável**.  
Cada commit deve começar com um **tipo**, opcionalmente seguido de um **escopo**, e uma **descrição curta** e clara.

---

## 📘 Formato padrão

````
git commit -m "<emoji> <tipo>(<escopo opcional>): <descrição breve>"
````

**Exemplo:**

```bash
git commit -m ":sparkles: feat(auth): add JWT authentication for users"
````

---

## 📌 Tipos de Commits

### 🔹 feat — Nova funcionalidade

* **Descrição:** Quando você **adiciona uma nova funcionalidade** ao sistema.
* **Use quando:** A mudança cria algo que **não existia antes**.
* **Exemplo:**

```bash
git commit -m ":sparkles: feat: add user authentication with JWT"
git commit -m ":sparkles: feat(profile): implement avatar upload feature"
```

---

### 🔹 update — Atualização de funcionalidade existente 🧩 *(subtipo de feat)*

* **Descrição:** Quando você **melhora ou altera o comportamento de uma funcionalidade existente**, sem ser uma correção de bug.
* **Use quando:** A função continua a mesma, mas **funciona de modo ligeiramente diferente** (melhor UX, fluxo ajustado, novo parâmetro etc).
* **Exemplo:**

```bash
git commit -m ":hammer_and_wrench: update(auth): adjust token expiration time for better UX"
git commit -m ":hammer_and_wrench: update(payment): allow partial refunds"
```

💡 *Dica:* Muitos times usam `feat` também para atualizações pequenas, mas usar `update` ajuda a distinguir novas features de melhorias em features antigas.

---

### 🔹 fix — Correção de erro 🐛

* **Descrição:** Corrige **bugs, exceções ou comportamentos incorretos**.
* **Exemplo:**

```bash
git commit -m ":bug: fix(login): handle null pointer in login service"
git commit -m ":bug: fix(cart): prevent negative quantities in cart"
```

---

### 🔹 docs — Documentação 📚

* **Descrição:** Mudanças em documentação, comentários, guias, etc.
* **Exemplo:**

```bash
git commit -m ":books: docs: update README with installation guide"
git commit -m ":books: docs(api): add usage examples for /auth endpoint"
```

---

### 🔹 style — Estilo e formatação 🎨

* **Descrição:** Alterações visuais no código, **sem alterar comportamento** (espaços, ponto e vírgula, identação, etc).
* **Exemplo:**

```bash
git commit -m ":art: style: format code using black"
git commit -m ":art: style(ui): align login form fields"
```

---

### 🔹 refactor — Refatoração 🔄

* **Descrição:** Melhorias no código **sem alterar o comportamento final**, com foco em **limpeza, organização, modularização ou legibilidade**.
* **Exemplo:**

```bash
git commit -m ":recycle: refactor(db): simplify connection logic"
git commit -m ":recycle: refactor(api): extract middleware for token validation"
```

💡 *Use quando a mudança é estrutural, não funcional.*

---

### 🔹 perf — Performance ⚡

* **Descrição:** Alterações que **melhoram o desempenho** do sistema.
* **Exemplo:**

```bash
git commit -m ":zap: perf(query): optimize search with database index"
git commit -m ":zap: perf(images): reduce image load time by compression"
```

---

### 🔹 test — Testes ✅

* **Descrição:** Adição, correção ou melhoria de **testes automatizados**.
* **Exemplo:**

```bash
git commit -m ":white_check_mark: test: add unit tests for user service"
git commit -m ":white_check_mark: test(auth): mock JWT in integration tests"
```

---

### 🔹 build — Build e dependências 📦

* **Descrição:** Alterações que afetam o **build**, **dependências** ou ferramentas de compilação.
* **Exemplo:**

```bash
git commit -m ":package: build: update dependencies to latest versions"
git commit -m ":package: build: migrate to Vite from Webpack"
```

---

### 🔹 ci — Integração Contínua 🧰

* **Descrição:** Mudanças em pipelines de CI/CD (GitHub Actions, Jenkins, etc).
* **Exemplo:**

```bash
git commit -m ":construction_worker: ci: add linting step to pipeline"
git commit -m ":construction_worker: ci: fix deployment path in GitHub Actions"
```

---

### 🔹 chore — Manutenção 🔧

* **Descrição:** Tarefas **não relacionadas diretamente ao código de produção** (configurações, scripts, limpeza, etc).
* **Exemplo:**

```bash
git commit -m ":wrench: chore: add .env.example file"
git commit -m ":wrench: chore: remove unused assets"
```

---

### 🔹 revert — Reversão ⏪

* **Descrição:** Reverte um commit anterior.
* **Exemplo:**

```bash
git commit -m ":rewind: revert: undo changes from commit abc123"
```

---

## 🎯 Outros tipos opcionais (avançados)

| Tipo         | Descrição                              | Exemplo                                                                            |
| ------------ | -------------------------------------- | ---------------------------------------------------------------------------------- |
| **merge**    | Indica merge de branches               | `git commit -m ":twisted_rightwards_arrows: merge: merge feature/login into main"` |
| **hotfix**   | Correção urgente em produção           | `git commit -m ":fire: hotfix: patch broken login flow"`                           |
| **security** | Alterações de segurança                | `git commit -m ":lock: security: patch XSS vulnerability in comments"`             |
| **config**   | Configurações de ambiente ou aplicação | `git commit -m ":gear: config: set NODE_ENV to production"`                        |

---

## 🧠 Boas práticas

1. **Use o imperativo**: “add”, “fix”, “update”, e não “added”, “fixed”, “updating”.
2. **Descrição breve e clara** — até **72 caracteres**.
3. **Inclua escopos** (entre parênteses) para contexto:

   ```bash
   git commit -m ":sparkles: feat(auth): add password reset via email"
   ```
4. **Use commits pequenos e atômicos** — 1 commit = 1 propósito.
5. **Adicione corpo e rodapé** (opcional) para contexto ou issues:

   ```bash
   git commit -m ":bug: fix(auth): handle token expiration"

   # Corpo
   The token was expiring prematurely due to incorrect TTL calculation.

   # Rodapé
   Closes #42
   ```

---

## ⚡ Ícones sugeridos

| Tipo   | Emoji                            | Tipo     | Emoji                      |
| ------ | -------------------------------- | -------- | -------------------------- |
| feat   | ✨ `:sparkles:`                   | fix      | 🐛 `:bug:`                 |
| update | 🛠️ `:hammer_and_wrench:`        | docs     | 📚 `:books:`               |
| style  | 🎨 `:art:`                       | refactor | ♻️ `:recycle:`             |
| perf   | ⚡ `:zap:`                        | test     | ✅ `:white_check_mark:`     |
| build  | 📦 `:package:`                   | ci       | 👷 `:construction_worker:` |
| chore  | 🔧 `:wrench:`                    | revert   | ⏪ `:rewind:`               |
| merge  | 🔀 `:twisted_rightwards_arrows:` | security | 🔒 `:lock:`                |

---

## 🧩 Exemplos completos

```bash
git commit -m ":sparkles: feat(user): add profile page"
git commit -m ":hammer_and_wrench: update(user): change password reset flow"
git commit -m ":bug: fix(api): prevent crash when token is missing"
git commit -m ":recycle: refactor(auth): extract middleware for validation"
git commit -m ":zap: perf(db): add indexes to improve query speed"
git commit -m ":books: docs: explain environment setup in README"
git commit -m ":white_check_mark: test(api): add test for 404 response"
git commit -m ":wrench: chore: remove deprecated functions"
```

---

## 🧭 Dica final

📁 **Sugestão:** Adicione este guia ao seu repositório como `CONVENTIONAL_COMMITS_GUIDE.md` ou inclua um resumo no `README.md`.
Isso ajuda a manter **consistência entre todos os colaboradores** e **melhor rastreabilidade das mudanças**.

```

---

Deseja que eu gere esse conteúdo direto como um arquivo `.md` pronto para download?
```
