# Hadron — Claude Code plugins

A [Claude Code](https://code.claude.com) plugin marketplace for the [Hadron](https://hadronmemory.com) AI-memory platform.

## Install

In Claude Code (the CLI or the **Code** tab):

```
/plugin marketplace add hadron-memory/hadron-plugins
/plugin install hadron@hadron
```

No GitHub account is required — this is a public repo, fetched anonymously.

You get three slash commands:

| Command | What it does |
|---|---|
| `/hadron:h-task <name>` | Run a runnable Hadron task by fuzzy name (wraps the `h-run-task` MCP tool). Omit the name to pick from a list. |
| `/hadron:h-search <text>` | Global search across the Hadron graph — nodes, memories, agents, apps (wraps `h-search`). |
| `/hadron:h-open-node <name\|urn>` | Find a node and open it in the portal at `https://hadronmemory.com/app/u/<urn>`. |

## Prerequisite: the Hadron MCP connector

These commands call Hadron's MCP tools, so connect Hadron first via **OAuth** — one user-level connection that also lights up the Claude **Chat** tab. The plugin intentionally does **not** bundle a connector: authenticate at the user level so Hadron is available across every surface that speaks MCP, under one identity.

## Surfaces

Slash commands are a Claude Code feature (CLI + Code tab). On the **Chat tab** you still have the Hadron MCP tools via the OAuth connector — you just invoke them in natural language rather than with `/hadron:*`. Cowork uses its own plugin format; Chrome has no slash commands.
