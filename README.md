# Hub de Integração · Governança de TI

Portal web de governança de TI com extração automática de dados via N8N.

## Arquivos principais

| Arquivo | Descrição |
|---|---|
| `index.html` | Portal de Governança TI · Enterprise |
| `hub_integracao_gov_ti.html` | Hub de Integração (gerencia fontes e N8N) |
| `data/data.json` | **Dados vivos** — atualizado automaticamente pelo N8N |

## Como o N8N atualiza os dados

O N8N extrai dados das fontes (SAP, Oracle, ServiceNow, Jira, GLPI) e atualiza
o arquivo `data/data.json` via GitHub API:

```
PUT https://api.github.com/repos/SEU_USUARIO/SEU_REPO/contents/data/data.json
Authorization: Bearer GITHUB_TOKEN
Content-Type: application/json

{
  "message": "chore: atualização automática via N8N",
  "content": "<base64 do novo data.json>",
  "sha": "<sha do arquivo atual>"
}
```

## Acesso Admin

Senha padrão: `GovTI@Adm2026`  
Altere em: Hub → aba Configurações → Segurança do Administrador

## Frameworks suportados

COBIT · ITIL · ISO 27001 · ISO 42001 · NIST · LGPD · TBM
