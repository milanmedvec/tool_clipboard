# tool_clipboard

Small X11 clipboard history tools with fzf picker and pinned entries.

## Commands

- `clip-daemon` - watch the clipboard and store clipboard history
- `clip-list` - print clipboard history entries for selection tools
- `clip-pick` - interactive fzf picker that copies the selected entry
- `clip-pick-launch` - open clip-pick in Alacritty and paste into the previous window
- `clip-delete` - delete an entry by hash
- `clip-toggle-pin` - pin/unpin an entry by hash
- `xcp-primary` - copy X primary selection to clipboard

## Dependencies

Required commands:
- `bash`
- `xclip`
- `clipnotify`
- `fzf`
- `xdotool`
- `alacritty`
- `sha256sum`

Optional commands:
- `xseticon` - sets the clip picker window icon

Check required commands in your shell:

```bash
need() {
    command -v "$1" >/dev/null || echo "missing: $1"
}

for cmd in bash xclip clipnotify fzf xdotool alacritty sha256sum; do
    need "$cmd"
done
```

## Install

```bash
./install.sh
```

Install to a custom prefix:

```bash
PREFIX="$HOME/.local" ./install.sh
```

## Usage

```bash
clip-daemon &
clip-pick-launch
```

## Configuration

- History is stored under `$HOME/.local/share/clip-history`.
- Includes original project icon `share/pixmaps/clip-pick.png`; `install.sh` installs it to `${XDG_DATA_HOME:-$HOME/.local/share}/pixmaps/clip-pick.png`.

## Notes

These scripts were extracted from a personal Arch Linux + i3 workspace. Review dependencies and paths before using them on another machine.
