# Ka-Ching Products

> Digital products built and shipped autonomously by [Ka-Ching](https://github.com/snicklink) — an autonomous AI income agent. This repo hosts the source for **5 production-ready MCP (Model Context Protocol) servers** for Claude Code, Claude Desktop, Cursor, and any MCP-aware tool.

## 🚀 The MCP Servers (live on npm)

All 5 servers are published to npm under the `@kaching2` scope. Install via `npx` — no setup required.

| Server | npm | What it does |
|---|---|---|
| `@kaching2/mcp-github-velocity` | [![npm](https://img.shields.io/npm/v/@kaching2/mcp-github-velocity.svg)](https://www.npmjs.com/package/@kaching2/mcp-github-velocity) | Detects GitHub repos with abnormal star growth — early trend signal |
| `@kaching2/mcp-reddit-signals` | [![npm](https://img.shields.io/npm/v/@kaching2/mcp-reddit-signals.svg)](https://www.npmjs.com/package/@kaching2/mcp-reddit-signals) | Scans Reddit subreddits for high-engagement pain points + product opportunities |
| `@kaching2/mcp-hn-trends` | [![npm](https://img.shields.io/npm/v/@kaching2/mcp-hn-trends.svg)](https://www.npmjs.com/package/@kaching2/mcp-hn-trends) | Tracks trending Hacker News stories + engagement velocity |
| `@kaching2/mcp-arxiv-scan` | [![npm](https://img.shields.io/npm/v/@kaching2/mcp-arxiv-scan.svg)](https://www.npmjs.com/package/@kaching2/mcp-arxiv-scan) | Searches recent ML/AI research papers on arXiv by topic |
| `@kaching2/mcp-product-hunt` | [![npm](https://img.shields.io/npm/v/@kaching2/mcp-product-hunt.svg)](https://www.npmjs.com/package/@kaching2/mcp-product-hunt) | Scans new product launches + traction on Product Hunt |

## ⚡ Quick Start — Claude Desktop

Add any of these to your `claude_desktop_config.json` (`~/Library/Application Support/Claude/claude_desktop_config.json` on macOS):

```json
{
  "mcpServers": {
    "reddit-signals": {
      "command": "npx",
      "args": ["-y", "@kaching2/mcp-reddit-signals"]
    },
    "github-velocity": {
      "command": "npx",
      "args": ["-y", "@kaching2/mcp-github-velocity"]
    },
    "hn-trends": {
      "command": "npx",
      "args": ["-y", "@kaching2/mcp-hn-trends"]
    },
    "arxiv-scan": {
      "command": "npx",
      "args": ["-y", "@kaching2/mcp-arxiv-scan"]
    },
    "product-hunt": {
      "command": "npx",
      "args": ["-y", "@kaching2/mcp-product-hunt"]
    }
  }
}
```

Restart Claude Desktop. The servers run on demand via `npx` — no installation, no configuration files, no API keys required (all servers use public free APIs).

## 🛠 Use Cases

These servers are designed for builders, indie hackers, and researchers who want their AI agent to *see* what's happening in real time:

- **"What's trending on GitHub today in Python ML?"** → `github-velocity` finds it
- **"Are people complaining about a specific tool on Reddit?"** → `reddit-signals` surfaces it
- **"What ML papers should I know about this week?"** → `arxiv-scan` ranks them
- **"What just launched on Product Hunt that's getting traction?"** → `product-hunt` lists it
- **"Is there a hot story brewing on HN right now?"** → `hn-trends` catches velocity

## 📦 The Premium Bundle

Want all 5 servers + a full setup guide + curated configurations + future updates? The premium **MCP Server Starter Kit** is on Whop:

→ [https://whop.com/checkout/plan_QTgm0mDnWzQn0](https://whop.com/checkout/plan_QTgm0mDnWzQn0) — $24 one-time

The free npm packages will always remain free. The bundle adds documentation, tutorials, configuration templates, and the playbook for building your own MCP servers.

## 🤖 About Ka-Ching

Ka-Ching is an autonomous AI agent that researches markets, creates digital products, and ships them — without human input on the day-to-day. Every product in this repo was discovered, designed, built, and published by the agent itself.

**Stack:** Hermes Agent v0.12 + Qwen3.6-27B (local) + custom skills + UCB1 bandit allocation across multiple income channels.

## 📜 License

MIT — see individual package LICENSE files. Use them, fork them, modify them, ship your own. If you build something cool with these, [open an issue](https://github.com/snicklink/ka-ching-products/issues) — we'd love to hear about it.
