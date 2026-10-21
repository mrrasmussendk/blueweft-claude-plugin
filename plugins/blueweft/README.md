# Blueweft for Claude and Codex

Create and edit architecture diagrams in your agent conversation. Blueweft connects
to your browser workspace and displays an interactive canvas in MCP Apps-capable
hosts. This package contains the connection configuration and architecture skill;
the application runs at [blueweft.com](https://blueweft.com).

## Install in Claude Code

```text
/plugin marketplace add mrrasmussendk/blueweft-claude-plugin
/plugin install blueweft@blueweft-plugins
```

Use `/mcp` to authenticate Blueweft. Approve the intended workspace in the browser
profile where you use Blueweft, then return to Claude. No Blueweft account,
provider API key, or copied token is required for architecture editing.

For later versions, refresh this marketplace and update `blueweft@blueweft-plugins`.
The package version is **1.0.5**. Server updates and plugin updates are
separate; reconnect or rescan when server tool metadata changes.

## Connect from Claude, Claude Desktop, or Cowork

Add a custom web connector using `https://blueweft.com/mcp`, OAuth and
**Register automatically**. Connect and approve the intended browser workspace.
The server supports Dynamic Client Registration and PKCE S256, with no client
secret. A public Claude directory listing is separate from this repository's
marketplace; these instructions also work before directory publication.

For Codex, add `https://blueweft.com/mcp` as a Streamable HTTP MCP server and
authenticate. A Codex plugin manifest and the same architecture skill are included
in `plugins/blueweft` for plugin-capable hosts.

## What you can do

- Create architecture and C4 diagrams, components, connections and boundary rules.
- Add component sequences, flowcharts, state diagrams, deployment models and API contracts.
- Record decisions, review and apply edits, validate design rules and restore checkpoints.
- Manage saved views and project history, and export documents and implementation handoffs.

Try: “Create an order-processing architecture with a web client, Orders API and
PostgreSQL. Forbid direct web-to-database access and open the interactive canvas.”

Claude and ChatGPT use the same tools and Vue canvas. Host support determines
inline rendering, display modes and downloads. Unsupported downloads expose
copyable source. Repository execution is local-only. Design validation does not
run repository tests or prove implementation compliance. Optional AI document
narratives require server-configured providers and an authenticated account
connection; ordinary agent-driven diagram editing uses your host's model.

## Access and privacy

The declared connector sends requested project content and authorized edits to
`https://blueweft.com/mcp`. Blueweft stores saved projects, history, snapshots,
connection metadata and token hashes. Saved work persists under the service's
retention and backup arrangements. OAuth access tokens last one hour; rotating
refresh grants last up to 30 days. Revoke access through **Connect agent** in
Blueweft and disconnect it in your host.

This hosted package runs no local installer and contains no credentials. The
approval page disables analytics. The website enables optional analytics only
after consent. Read the [privacy policy](https://blueweft.com/privacy) and
[service terms](https://blueweft.com/terms) before connecting. Keep the browser
profile that owns your projects; another profile can select a different workspace.

Support: [GitHub issues](https://github.com/mrrasmussendk/blueweft-claude-plugin/issues) or
[mr@marcrasmussen.dk](mailto:mr@marcrasmussen.dk).

## License and releases

The plugin is proprietary. See the
[plugin license](https://github.com/mrrasmussendk/blueweft-claude-plugin/blob/main/plugins/blueweft/LICENSE).
Public availability does not grant unrestricted reuse or redistribution.

This repository receives generated plugin releases. It contains no application
server source, frontend application source, credentials or application Git history.
