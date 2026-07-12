# docswarden

Local-first MCP server that indexes framework documentation (React, Next.js, FastAPI) into a searchable SQLite index and exposes it to AI clients via MCP.

## Install

```bash
uvx docswarden install
uvx docswarden index fastapi react nextjs
```

That's it — no cloning, no venv setup. Restart your MCP client and the tools are available.

## Commands

```bash
docswarden index fastapi react nextjs   # crawl & index docs
docswarden install --client claude      # write Claude Desktop config
docswarden list                         # show index status
docswarden run                          # start MCP server (clients do this automatically)
```

## MCP tools

- `search_docs(query, framework?, limit?)` — ranked search with source URL + index date
- `get_page(url)` — section list for a page
- `get_section(url, section_title)` — full content of one section

## Supported clients

`install` auto-configures Claude Desktop, Cursor, and VS Code.
