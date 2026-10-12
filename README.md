# AdHedge Install Trust

Stop spending ad budget on installs that aren't real people. AdHedge verifies every Android install with Google's
Play Integrity API and shows your true cost per install, by network.

This repository is the plugin for AI coding tools: it connects your assistant to the AdHedge MCP server. There is
no code here. The server is `https://api.adhedge.io/mcp`, and you sign in with OAuth the first
time a tool connects. There is no token to copy.

## What you can ask

- "Add AdHedge to my Android app and tell me when the first verified install arrives."
- "How many of last week's installs were Trusted, Unverified and Suspect, by network?"
- "Here is my ad network's install report. What did I pay per Trusted install on each campaign?"
- "Build an evidence pack for last month."

## Install

### Cursor

Open this link, and Cursor adds the server:

cursor://anysphere.cursor-deeplink/mcp/install?name=adhedge&config=eyJ1cmwiOiJodHRwczovL2FwaS5hZGhlZGdlLmlvL21jcCJ9

### Claude Code

```
/plugin marketplace add https://github.com/adhedge-io/install-trust-plugin
/plugin install adhedge-install-trust@adhedge
```

### Codex

```
codex mcp add adhedge --url https://api.adhedge.io/mcp
codex mcp login adhedge
```

### Anything else that speaks MCP

Add a remote (streamable HTTP) server with the URL above.

## What is in here

- `plugins/adhedge-install-trust/mcp.json` and `.mcp.json`: the server's address, for Cursor and for Claude Code.
- `.cursor-plugin/` and `.claude-plugin/`: the manifests each tool reads.

The server tells a connected assistant how to do the common jobs. That guidance is served over MCP, so it is always
current, and none of it is copied here.

## Links

- Docs: https://adhedge.io/docs
- What the SDK sends: https://adhedge.io/data-safety
- Privacy: https://adhedge.io/privacy

## License

Apache-2.0. See `LICENSE`. The license covers the files in this repository. The AdHedge service is not part of it.
