# poprix plugin for Claude

The Claude plugin for [poprix](https://poprix.ai), the AI customer-service desk. It connects Claude to your poprix desk through poprix's remote MCP server and adds skills for reviewing approvals and investigating cases.

This repository holds only the plugin bundle (manifest, skills, logo). The poprix service itself is not here.

## Install

Claude Code:

```bash
/plugin marketplace add dolevhayut/poprix-plugin
/plugin install poprix@poprix
```

Claude (web and desktop): add poprix from the connector directory, or add a custom connector with the URL `https://poprix.ai/api/mcp`.

Then sign in with your poprix account when Claude asks. See [plugins/poprix/README.md](plugins/poprix/README.md) and https://poprix.ai/welcome/claude.

## License

MIT
