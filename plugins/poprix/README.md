# poprix for Claude

poprix is an AI customer-service desk: AI agents answer a business's customers on WhatsApp, email, the website chat and Telegram, and escalate the hard cases (money, legal, safety, a customer asking for a person) to a human manager. This plugin lets that manager work the desk from Claude: see what is waiting for approval, read any conversation, check what the agents know, and approve or decline drafted replies, without opening the poprix console.

## What is included

- **The poprix MCP server** at `https://poprix.ai/api/mcp`. You sign in with your poprix account (Google or an email link) and approve access to one organisation. Tools: `list_pending_approvals`, `list_open_cases`, `read_case`, `search_knowledge` (read-only) and `decide_approval` (approve, decline or resolve a pending case through poprix's own approval gate).
- **Skills**: `review-approvals` walks through the approvals queue and always waits for your explicit decision before anything is sent; `investigate-case` finds and explains a case and checks answers against your knowledge base.

## Install

Claude Code:

```bash
/plugin install poprix --marketplace dolevhayut/poprix-plugin
```

Claude (web and desktop): add poprix from the connector directory, or add a custom connector with the URL `https://poprix.ai/api/mcp`, then sign in with your poprix account.

## Data

Claude receives conversations, drafts and knowledge-base passages of your organisation only when a tool reads them for you, within your poprix role. Every decision passes the same checks as in poprix and is recorded in your organisation's audit log. There are no delete tools. Disconnect at any time from Claude's connector settings.

- Documentation: https://poprix.ai/welcome/claude
- Privacy policy: https://poprix.ai/privacy?lang=en
- Terms: https://poprix.ai/terms?lang=en
- Support: sales@poprix.ai
