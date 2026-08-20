# Instalação detalhada

MPT Unificada: Certidão Negativa de Feitos é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_mpt_cnf_unificada`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_mpt_cnf_unificada` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_mpt_cnf_unificada` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_mpt_cnf_unificada` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.mpt_cnf_unificada` (ou `servers.mpt_cnf_unificada` no VS Code) do config do cliente e reinicie.
