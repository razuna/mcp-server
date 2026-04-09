# Razuna MCP Server

> AI-powered digital asset management. Find, organize, and manage your files with natural language.

Razuna is a hosted MCP server that connects any MCP-compatible AI tool to your Razuna digital asset management workspace.

## Features

- **AI-powered file search** — find files by description, content, or visual similarity
- **Workspace management** — manage folders, metadata, and permissions
- **Notes & memory** — store and retrieve knowledge tied to your assets
- **Semantic image search** — find visually similar images using CLIP embeddings
- **59 tools** — full DAM operations via natural language
- **Two data centers** — US (`mcp.razuna.com`) and EU (`mcp-eu.razuna.com`)

## Quick Start

1. Sign up at [razuna.com](https://razuna.com) to get your access token
2. Add to your MCP client config:

```json
{
  "mcpServers": {
    "razuna": {
      "url": "https://mcp.razuna.com/mcp",
      "headers": {
        "access-token": "YOUR_ACCESS_TOKEN"
      }
    }
  }
}
```

### EU Data Center

```json
{
  "mcpServers": {
    "razuna": {
      "url": "https://mcp-eu.razuna.com/mcp",
      "headers": {
        "access-token": "YOUR_ACCESS_TOKEN"
      }
    }
  }
}
```

## Available Tools (59 total)

- `search_files` — AI-powered natural language file search
- `find_similar_images` — find visually similar images
- `get_file_metadata` — get detailed file information
- `list_workspaces` — list all accessible workspaces
- `get_folder_tree` — get hierarchical folder structure
- `search_knowledge` — search across notes and memories
- `store_memory` / `recall_memory` — persistent AI memory
- `create_note` / `search_notes` — structured notes

[Full tool reference](https://razuna.com/docs/mcp)

## Authentication

All requests require an `access-token` header. Get your token from your Razuna account settings.

## Data Centers

| Region | URL |
|---|---|
| US | `https://mcp.razuna.com/mcp` |
| EU | `https://mcp-eu.razuna.com/mcp` |

## License

AGPL-3.0
