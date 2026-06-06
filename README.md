[update-readmes]   Mode: rewrite — migrating to template structure...
# horizon

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/horizon)

<!-- AI:start:what-it-does -->
_Description pending._
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
_Architecture documentation pending._
<!-- AI:end:architecture -->

## Install


### Download (fastest)

Grab the latest binary from [**Releases**](https://github.com/peters/horizon/releases/latest) — no dependencies needed.

| Platform | Asset | |
|:---------|:------|:-|
| **Linux** x64 | `horizon-linux-x64.tar.gz` | Extract, `chmod +x`, run |
| **macOS** arm64 | `horizon-osx-arm64.tar.gz` | Extract, `chmod +x`, run |
| **macOS** x64 | `horizon-osx-x64.tar.gz` | Extract, `chmod +x`, run |
| **Windows** x64 | `horizon-windows-x64.exe` | Download and run |

### Build from source

```bash
git clone https://github.com/peters/horizon.git
cd horizon
git lfs install
git lfs pull
cargo run --release
```

> Requires **Git LFS** for bundled assets and **Rust 1.88+**. Linux needs system headers for GPU rendering — see [AGENTS.md](AGENTS.md#prerequisites) for per-distro install commands.

---

## Usage

<!-- Add usage examples here. This section is yours — the AI will not modify it. -->

## Configuration


The settings editor writes back to the same config file Horizon loaded. By default that is `~/.horizon/config.yaml`, and `config.yml` is also supported when discovered or passed explicitly. You can define workspaces, panel presets, feature flags, and keyboard shortcuts:

```yaml
shortcuts:
  command_palette: Ctrl+Shift+K
  new_terminal: Ctrl+Shift+N
  open_remote_hosts: Ctrl+Shift+H
  toggle_sidebar: Ctrl+Shift+B
  toggle_hud: Ctrl+Shift+U
  toggle_minimap: Ctrl+Shift+M
  align_workspaces_horizontally: Ctrl+Shift+A
  toggle_settings: Ctrl+Shift+Comma
  reset_view: Ctrl+Shift+0
  zoom_in: Ctrl+Shift+Plus
  zoom_out: Ctrl+Shift+Minus
  fullscreen_panel: F11
  exit_fullscreen_panel: Escape
  fullscreen_window: Ctrl+Shift+F11
  save_editor: Ctrl+Shift+S

workspaces:
  - name: Backend
    cwd: ~/projects/api
    panels:
      - kind: shell
      - kind: claude
      - kind: git_changes

  - name: Frontend
    cwd: ~/projects/web
    panels:
      - kind: shell
      - kind: shell

presets:
  - name: Shell
    alias: sh
    kind: shell
  - name: Claude Code
    alias: cc
    kind: claude
  - name: Git Changes
    alias: gc
    kind: git_changes

# Optional: disable the default attention feed
features:
  attention_feed: false
```

Use key names like `Plus`, `Minus`, `Comma`, `Escape`, and `F11` in YAML instead of punctuation-only shortcut components such as `Ctrl++`.

---

## CI

<!-- AI:start:ci -->
_CI documentation pending._
<!-- AI:end:ci -->

## Mirror chain

<!-- AI:start:mirror-chain -->
This repo is maintained in [`Interested-Deving-1896/horizon`](https://github.com/Interested-Deving-1896/horizon) and mirrored through:

```
Interested-Deving-1896/horizon  ──►  OpenOS-Project-OSP/horizon  ──►  OpenOS-Project-Ecosystem-OOC/horizon
```

Changes flow downstream automatically via the hourly mirror chain in
[`fork-sync-all`](https://github.com/Interested-Deving-1896/fork-sync-all).
Direct commits to OSP or OOC are detected and opened as PRs back to `Interested-Deving-1896`.
<!-- AI:end:mirror-chain -->

## Contributors

<!-- AI:start:contributors -->
_Contributors pending._
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
_No additional resource files found._
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
[MIT](https://github.com/Interested-Deving-1896/horizon/blob/main/LICENSE) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
