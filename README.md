# Eurobase plugins

Plugin marketplace for connecting AI coding agents to [Eurobase](https://eurobase.dev).

| Plugin | What it does |
|---|---|
| [`eurobase`](plugins/eurobase) | Connects Codex or Claude Code to the Eurobase MCP server with OAuth: deploy repositories, read deployments and logs. |

Codex:

```sh
codex plugin marketplace add eurobase-dev/plugins
codex plugin add eurobase@eurobase
```

Claude Code:

```sh
claude plugin marketplace add eurobase-dev/plugins
claude plugin install eurobase@eurobase
```

Docs: [eurobase.dev/docs/agents](https://eurobase.dev/docs/agents) · Support: support@eurobase.dev
