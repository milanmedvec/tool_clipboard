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

- bash
- xclip
- clipnotify
- fzf
- xdotool
- alacritty
- sha256sum/coreutils

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

## Notes

These scripts were extracted from a personal Arch Linux + i3 workspace. Review dependencies and paths before using them on another machine.
