# Claudian 2.2.6 — release build for second-brain

> **This is not the official Claudian repository.** It holds the unmodified release files of
> **[Claudian](https://github.com/YishenTu/claudian)** by Yishen Tu (YishenTu), MIT-licensed, so that
> [second-brain](https://github.com/adamkopelman/second-brain) can pin them as an optional git
> submodule at `.obsidian/plugins/realclaudian`. For documentation (https://github.com/YishenTu/claudian#readme), support, bug reports
> and newer versions go to **[YishenTu/claudian](https://github.com/YishenTu/claudian)** — all credit belongs to its authors.

In second-brain, Claudian runs Claude Code / opencode / Codex in an Obsidian side panel, the recommended way to use second-brain's skills (optional).

## Why this repo exists
Obsidian loads a community plugin from `main.js`, `manifest.json` and `styles.css` in
`<vault>/.obsidian/plugins/realclaudian/`. Upstream keeps its sources in git and publishes those built
files only as release assets, so the upstream repository can't be used as that folder directly.
This repo contains exactly those three files from release [`2.2.6`](https://github.com/YishenTu/claudian/releases/tag/2.2.6), byte for byte, plus
this README, upstream's license and ignore rules. Nothing was modified.

| File | sha256 |
| --- | --- |
| `main.js` | `ecac017f1cf02aca00535687dc76a0767cb43bad0e09c2139195ecc068418b33` |
| `manifest.json` | `03daf2c5d330768f4b5b28f8426a4a9c2061c1f05137455d40ff95077199059a` |
| `styles.css` | `e9e77a6d919ab4d30aa0dc21bcaaed3f92d66640a73437b5920c1958796fdf21` |

The plugin id is `realclaudian` (as in upstream's manifest), so the folder is `.obsidian/plugins/realclaudian`.

## Your settings stay local
Obsidian saves the plugin's settings to `data.json` in this folder; `.gitignore` ignores it and
everything else the plugin writes here, so your settings (including any API keys) are never
committed. second-brain doesn't preset any settings for this plugin.

## Alternative: install from Obsidian
Skip this submodule and install **Claudian** from Settings → Community plugins → Browse; Obsidian
puts it in the same folder.

## Updating
```sh
gh release download <tag> --repo YishenTu/claudian --pattern main.js --pattern manifest.json --pattern styles.css --clobber
```
Update the version and hashes above, commit, and bump the submodule in second-brain.

## License
MIT — [`LICENSE`](LICENSE) is copied verbatim from
[YishenTu/claudian at `2.2.6`](https://github.com/YishenTu/claudian/blob/2.2.6/LICENSE) (Copyright (c) 2025).
