# codex-skills-registry

Public registry index for Codex skills (MVP).

## What this repo contains

- `index.json` - top-level list of skills with latest version, tags, and artifact info
- `skills/<name>/manifest.json` - per-skill manifest with versions and install notes
- `artifacts/<name>/<version>.skill` - packaged skills (zip file with `.skill` extension)

## Add a new skill (MVP workflow)

1) Package the skill as a `.skill` (zip):
```
zip -r artifacts/<skill>/<version>.skill <skill-folder>
```

2) Compute sha256:
```
sha256sum artifacts/<skill>/<version>.skill
```

3) Update:
- `skills/<skill>/manifest.json`
- `index.json`

## Related repos

- CLI: https://github.com/iluxu/codex-skill
- MCP server: https://github.com/iluxu/codex-skills-mcp
- Theme toolchain: https://github.com/iluxu/temus
