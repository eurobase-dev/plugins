# Eurobase for Codex and Claude Code

Connects your agent to Eurobase's remote MCP server at `https://api.eurobase.dev/mcp`
with OAuth. The plugin contains only that connection: no local server, hook, script,
bundled credential or permission bypass. Eurobase decides what the agent may do.

## Install

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

Start a new session and sign in to the `eurobase` server when the agent asks
(Claude Code: `/mcp`). Eurobase opens in your browser: choose the projects, the
organization where the agent may create projects, and the level of each permission.

Prefer a direct connection without the plugin? See
[eurobase.dev/docs/agents](https://eurobase.dev/docs/agents). Use either the plugin or a
direct connection, not both, so the agent does not see duplicate tools.

## Use

- "Deploy this repository on Eurobase." The agent creates the project, starts the first
  deployment and follows it until the site responds. Add secret values in the Eurobase
  dashboard; they never pass through the agent.
- "Show the latest deployment of my project and explain its failure from the logs."
- "Publish this function in my Eurobase project." With Functions write access the agent
  creates or updates an HTTP Function and publishes its code; send the complete source and
  keep secret values out of it.

Writes need the Write or Full level you grant on the consent page.
The agent cannot delete anything. Never paste tokens, cookies or secrets into a prompt
or into `.mcp.json`.

## Revoke

Revoke access in Eurobase under Settings → Connected apps. Removing the plugin alone
does not revoke the connection.
