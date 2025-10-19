🧩 Resumo – GitHub Actions
🧱 Estrutura do Workflow
Workflows

Definidos no nível do repositório (.github/workflows/).

Contêm os gatilhos (triggers) e a lógica de automação.

Jobs

Definidos dentro dos workflows.

Executam em ambientes isolados (como Ubuntu, Windows, etc.).

Rodam em paralelo por padrão, mas podem ter dependências (needs:).

Steps

São as etapas dentro de um job.

Executam em sequência.

Podem rodar comandos diretos ou actions.

⚡ Workflow Triggers (Eventos)

Eventos de repositório: push, pull_request, issues, etc.

Manuais: executados via console ou API (workflow_dispatch).

Agendados: com schedule usando sintaxe cron.

🏃 Workflow Runners

GitHub-Hosted: executores padrão do GitHub.

Self-Hosted: executores instalados por você (em VMs ou servidores).

Advanced Runners: executores gerenciados com mais controle e segurança.

⚙️ GitHub Actions

Blocos reutilizáveis de automação.

Disponíveis no Marketplace (criados pela comunidade).

Podem ser customizadas (Actions próprias em Docker, Node.js ou Composite).

🔍 Filters and Activity

Usados para limitar quando um workflow ou job roda.

Exemplo:

on:
  push:
    branches: [main]


Também é possível filtrar por paths, tags, tipos de evento, etc.

🧩 Contexts

Dados disponíveis durante a execução (github, env, job, steps, etc.).

Exemplo:

echo "Executado por: ${{ github.actor }}"

🧮 Expressions

Usadas dentro de ${{ }} para lógica e manipulação de dados.

Permitem usar operadores, funções e variáveis.

Exemplo:

if: ${{ contains(github.ref, 'main') }}

🔑 Variables

Valores armazenados para uso em steps ou jobs.

Tipos:

env → variáveis de ambiente

secrets → dados sensíveis

vars → variáveis definidas no repositório/org

🧠 Functions

Funções internas usadas em expressions.

Exemplos:

contains()

startsWith()

endsWith()

format()

join()