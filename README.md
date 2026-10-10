# AISkills402 MCP server

Remote MCP server for **AISkills402** (https://aiskills402.com): a catalog of tested AI agent skill files
(`SKILL.md`, Agent Skills format). Searching is free. A skill file is bought once over x402 for cents in USDC on
Base and is yours to keep, with free re-downloads and free new versions.

This repository holds the listing metadata for MCP catalogs. The server itself is hosted; there is nothing to
install or run locally.

## Connect

- Endpoint (Streamable HTTP): `https://mcp.aiskills402.com/mcp`
- No account, no API key.

Claude Code:

```bash
claude mcp add --transport http aiskills402 https://mcp.aiskills402.com/mcp
```

Any other client: add a remote (Streamable HTTP) server with the URL above.

## Tools

| Tool | What it does |
|---|---|
| `search_skills` | Search the skill files for sale by plain-language query, category, tag or language. Each card says what the skill is for, what it is not for, its price and how it was tested with a strong and a weak model. |
| `list_categories` | The skill categories with a short introduction and how many skills each holds. |
| `get_skill` | One skill card plus the exact x402 payment requirements for buying its file, and how to buy. |
| `redownload_skill` | Download a file you already bought again, with the token from your purchase receipt. |

All four tools are free. The MCP server never takes payments: a purchase is an HTTP request to
`https://api.aiskills402.com/v1/skills/<slug>/file`, answered with `402 Payment Required` and paid with any x402
client. Check the amount in the 402 before your agent signs.

## Links

- Catalog: https://aiskills402.com/skills
- What an agent signs, and how to verify it before paying: https://aiskills402.com/trust
- For language models: https://aiskills402.com/llms.txt
- Official MCP Registry entry: `com.aiskills402/mcp`
