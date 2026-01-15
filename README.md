# Digital Hustle Lab Memory

A clean, simple MCP memory service for AI assistants. Deploy to Railway and connect your favorite AI tools.

## Quick Start

1. **Deploy to Railway**: Connect this repo to Railway for automatic deployment
2. **Get your Railway URL** (provided by Railway after deployment)
3. **Configure your AI tools** with the Railway endpoint

## Features

- **Semantic Search**: Find memories using natural language
- **Tag Organization**: Categorize and filter memories by tags
- **Web Dashboard**: Manage memories through a web interface
- **Multi-Client Support**: Works with Claude, VS Code, Cursor, and more
- **SQLite Backend**: Fast, reliable local storage

## Railway Deployment

After connecting to Railway:
- Railway will provide your app URL: `https://your-app-name.up.railway.app`
- Use this URL in your MCP configurations

## Local Development

```bash
git clone https://github.com/Tattzy25/Digital-Hustle-Memory.git
cd Digital-Hustle-Memory
pip install -r requirements.txt
python -m mcp_memory_service.server
```

## MCP Configuration

**For Railway (Remote):**
```json
{
  "mcpServers": {
    "digital-hustle-lab": {
      "type": "streamableHttp",
      "url": "https://your-railway-url.up.railway.app/mcp"
    }
  }
}
```

**For Local Development:**
```json
{
  "mcpServers": {
    "digital-hustle-lab": {
      "command": "python",
      "args": ["-m", "mcp_memory_service.server"]
    }
  }
}
```

## Available Tools

- `store_memory` - Save conversations and context
- `retrieve_memory` - Search memories semantically
- `search_by_tag` - Find memories by tags
- `get_cache_stats` - View performance statistics
- `check_database_health` - Database diagnostics

## License

Apache 2.0
