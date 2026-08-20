---
name: mpt_cnf_unificada-mcp
description: Skill da REST API do MPT Unificada: Certidão Negativa de Feitos na MCP.AI: 1 endpoint em /api/mpt_cnf_unificada. MPT Unificada: Certidão Negativa de Feitos, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# MPT Unificada: Certidão Negativa de Feitos — REST API skill

Você tem acesso à **MPT Unificada: Certidão Negativa de Feitos** REST API na MCP.AI.

> MPT Unificada: Certidão Negativa de Feitos, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/mpt_cnf_unificada
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/mpt_cnf_unificada/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"uf":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/mpt_cnf_unificada/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `mpt_cnf_unificada_consultar`

MPT Unificada: Certidão Negativa de Feitos, consulta em fonte oficial. _(POST /api/mpt_cnf_unificada/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cpf` | string | Não | Parâmetro de consulta "cpf". |
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `uf` | string | Sim | Parâmetro de consulta "uf". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_mpt_cnf_unificada` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
