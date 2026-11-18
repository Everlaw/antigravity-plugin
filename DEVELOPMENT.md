# Development

## Validate

```
agy plugin validate --strict .
```

## Install from a local checkout

```
agy plugin install /path/to/antigravity-plugin
```

Then confirm in Antigravity that the plugin installs enabled, the **Authenticate** button completes the browser OAuth flow, and the Everlaw tools appear.

## Pointing at a different server

To test against a non-production Everlaw environment, edit `serverUrl` in `mcp_config.json` in your local checkout before installing. The OAuth client named in `mcp_config.json` must be registered on that environment with Antigravity's redirect URI (`https://antigravity.google/oauth-callback`) and PKCE (S256) required.

## Releasing

1. Bump `version` in `plugin.json` (SemVer).
2. Validate with `--strict`.
3. Tag the release and push.
