# Everlaw plugin for Google Antigravity

Search and analyze your Everlaw ediscovery projects from [Google Antigravity](https://antigravity.google) using natural language. The plugin connects Antigravity to the [Everlaw MCP server](https://support.everlaw.com/hc/en-us/articles/49986656959771-Everlaw-MCP-Server), which exposes a read-only set of tools for running searches, retrieving documents and metadata, and asking Deep Dive questions.

All actions run with the signed-in user's own Everlaw permissions: the plugin cannot see or do anything the user could not see or do in the Everlaw web UI.

## Requirements

- An Everlaw account in the US region (`app.everlaw.com`). Other regions are not yet supported by this plugin.
- Your Everlaw organization must have OAuth2 enabled by an Organization Admin. See [Set Up Everlaw MCP Connectors](https://support.everlaw.com/hc/en-us/articles/57429911212059-Set-Up-Everlaw-MCP-Connectors).
- Google Antigravity (App or CLI).

## Installation

From the Antigravity CLI:

```
agy plugin install https://github.com/Everlaw/antigravity-plugin
```

Or in the Antigravity App, install from **App Customizations → Marketplace** (once listed).

## Authentication

On first use, Antigravity opens your browser to sign in to Everlaw and authorize access (OAuth 2.0 with PKCE). No API keys or manual configuration are required. To disconnect, revoke the authorization from your Everlaw account settings or remove the plugin.

## Tools

The Everlaw MCP server currently provides read-only tools, including:

- Project search: build and run searches, explore and describe search terms, page through results
- Documents and metadata: document text, metadata fields and options, datasets, processed uploads, extraction fields
- Review data: Bates prefixes, binders, codes, productions, search term reports
- Deep Dive: ask questions and retrieve responses
- Users: list project users

For the authoritative tool list and schemas, see the [Everlaw MCP Server documentation](https://support.everlaw.com/hc/en-us/articles/49986656959771-Everlaw-MCP-Server).

## Permissions in Antigravity

Antigravity asks before each MCP tool call by default. Because the Everlaw MCP server is read-only, you can safely allow all of this plugin's tools with the permission pattern `mcp(everlaw_everlaw-mcp/*)`.

## Support

- [Everlaw MCP Server (developer documentation)](https://support.everlaw.com/hc/en-us/articles/49986656959771-Everlaw-MCP-Server)
- [Set Up Everlaw MCP Connectors (end-user documentation)](https://support.everlaw.com/hc/en-us/articles/57429911212059-Set-Up-Everlaw-MCP-Connectors)
- [Everlaw Support](https://support.everlaw.com)
