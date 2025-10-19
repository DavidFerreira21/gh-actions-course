# 🧩 Resumo – GitHub Actions

## 🧱 Estrutura do Workflow

### **Workflows**
- Definidos no nível do repositório (`.github/workflows/`).
- Contêm os *gatilhos* (triggers) e a lógica de automação.

### **Jobs**
- Definidos dentro dos workflows.
- Executam em ambientes isolados (Ubuntu, Windows, etc.).
- Rodam **em paralelo** por padrão, mas podem ter dependências (`needs:`).

### **Steps**
- Etapas dentro de um job.
- Executam **em sequência**.
- Podem rodar **comandos diretos** ou **actions**.

---

## ⚡ Workflow Triggers (Eventos)

- **Eventos de repositório**: `push`, `pull_request`, `issues`, etc.
- **Manuais**: executados via console ou API (`workflow_dispatch`).
- **Agendados**: com `schedule` usando sintaxe *cron*.

---

## 🏃 Workflow Runners

- **GitHub-Hosted**: executores padrão do GitHub.
- **Self-Hosted**: executores instalados por você (VMs, servidores, etc.).
- **Advanced Runners**: executores gerenciados com mais controle e segurança.

---

## ⚙️ GitHub Actions

- Blocos reutilizáveis de automação.
- Disponíveis no **Marketplace** (criados pela comunidade).
- Podem ser **customizadas** (Actions próprias em Docker, Node.js ou Composite).

---

## 🔍 Filters and Activity

- Limitam quando um workflow ou job roda.
- Exemplo:
  ```yaml
  on:
    push:
      branches: [main]
