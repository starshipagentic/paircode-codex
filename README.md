# paircode-codex

Codex CLI marketplace plugin that registers `/paircode` as a slash command.

**This repo contains only the slash-command manifest.** The actual Python tool lives at [`starshipagentic/paircode`](https://github.com/starshipagentic/paircode) and must be installed separately.

## Install

```bash
# 1. Install the paircode Python CLI (once)
pipx install paircode

# 2. Register the marketplace, then install /paircode
codex plugin marketplace add starshipagentic/paircode-codex
codex plugin add paircode@paircode
```

Now, from inside any `codex` interactive session, type `/paircode` — the slash-command menu lists it.

## Alternative: let paircode's installer do it for you

```bash
pipx install paircode
paircode install      # registers /paircode in Codex, Claude, Gemini all at once
```

## What's in here

```
.agents/plugins/marketplace.json     marketplace manifest listing this plugin
plugins/paircode/
  .codex-plugin/plugin.json          plugin manifest
  commands/paircode.md               the /paircode slash-command prompt
```

Versions here track the main paircode release via `scripts/release.py` in the paircode repo.

## License

MIT. See `LICENSE`.
