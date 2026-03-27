# xiaohongshu-mcp

A local OpenClaw skill for working with a Xiaohongshu MCP server through `mcporter`.

## Features

- Search Xiaohongshu notes
- Read note details and comments
- Post comments and replies
- Publish image posts
- Use local-image publishing via Docker-mounted `/images`

## Layout

- `SKILL.md` — skill instructions
- `scripts/` — helper scripts
- `assets/config/mcporter.json` — local mcporter config for the skill
- `assets/templates/` — publish JSON templates
- `assets/docker-compose.xiaohongshu-mcp.yml` — example local deployment
- `references/setup.md` — setup notes

## Quick start

### Search

```bash
./scripts/xhs-search.sh OpenClaw
```

### Pick from search results and load detail

```bash
./scripts/xhs-pick-detail.sh OpenClaw
./scripts/xhs-pick-detail.sh --comments OpenClaw
```

### Publish

```bash
./scripts/xhs-publish.sh assets/templates/publish-template-private.json
```

## Notes

- The default config expects a local MCP endpoint at `http://localhost:18060/mcp`
- For local images, publish container-visible paths such as `/images/demo.png`
- Keep runtime data out of the repository; see `.gitignore`
