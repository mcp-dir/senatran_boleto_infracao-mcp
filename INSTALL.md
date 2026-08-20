# Instalação rápida

SENATRAN: Boleto da Infração é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_senatran_boleto_infracao`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `SENATRAN: Boleto da Infração` / `https://api.mcp.ai/p_senatran_boleto_infracao`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "senatran_boleto_infracao": { "type": "http", "url": "https://api.mcp.ai/p_senatran_boleto_infracao" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=senatran_boleto_infracao&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9zZW5hdHJhbl9ib2xldG9faW5mcmFjYW8ifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "senatran_boleto_infracao": { "url": "https://api.mcp.ai/p_senatran_boleto_infracao" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=senatran_boleto_infracao&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_senatran_boleto_infracao%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "senatran_boleto_infracao": { "type": "http", "url": "https://api.mcp.ai/p_senatran_boleto_infracao" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_senatran_boleto_infracao
```

Dúvidas? [senatran_boleto_infracao@mcp.ai](mailto:senatran_boleto_infracao@mcp.ai)
