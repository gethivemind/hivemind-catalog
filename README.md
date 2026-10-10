# Hivemind catalog feed

The signed catalog Hivemind installs fetch daily (ADR-043): applications, MCP servers and agent manifests.

- `catalog.json` is built from the bundled catalogs by `pnpm catalog:build` in the Hivemind repository.
- `catalog.json.sig` is its Ed25519 signature; the public key is compiled into the app, so a tampered feed is refused.

Nothing here is private. Do not edit by hand: the next publish overwrites it.
