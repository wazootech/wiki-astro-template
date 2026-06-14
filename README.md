# wiki-astro-template

Astro static site that consumes **`wiki export`** JSON-LD and pre-renders one route per vault page.

Registry: [Wiki CLI templates](https://github.com/wazootech/wiki/blob/main/docs/wiki/Wiki_CLI.md#ecosystem-templates).

## Quick start

```bash
pip install wazootech-wiki
bash scripts/export-wiki-data.sh
cd web && npm install && npm run build
```

Open `web/dist/` after `astro build`.

## Layout

| Path | Role |
| ---- | ---- |
| `wiki/` | Example vault |
| `wiki.yaml` | Wiki CLI config |
| `scripts/export-wiki-data.sh` | `wiki check` + `wiki export` → `web/data/wiki-export.json` |
| `web/` | Astro SSG app |

## Deploy

Deploy `web/dist/` to Netlify, Cloudflare Pages, or GitHub Pages. Re-run `scripts/export-wiki-data.sh` when the vault changes.

## Related

- [#96](https://github.com/wazootech/wiki/issues/96)
- [Wiki Subcommand export](https://github.com/wazootech/wiki/blob/main/docs/wiki/Wiki_Subcommand_export.md)
