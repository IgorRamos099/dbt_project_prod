# dbt_project_prod

Projeto de dbt para ambiente de produção

## Carregar variáveis de ambiente (PowerShell)

Para rodar `dbt` localmente, defina as variáveis de ambiente usadas em `profiles.yml`. Exemplo rápido para PowerShell (session scope):

```powershell
$env:GCP_DEV_PROJECT='dbt-core-498321'
$env:DBT_DEV_SCHEMA='schema_dev'
$env:GCP_DEV_KEYFILE_PATH='C:\\Users\\Gabriel Evangelis\\Downloads\\dbt-core-498321-ea5fc8aaeeab.json'

## Executar dbt debug
dbt debug --profiles-dir dbt_project_dbt --project-dir dbt_project_dbt
```

Se preferir persistir as variáveis, adicione-as nas Variáveis de Ambiente do Windows ou crie um script `load-env.ps1` com os comandos acima.