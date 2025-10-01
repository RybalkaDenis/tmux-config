# Tmux Configuration

Vim-centric tmux configuration with macOS clipboard integration and ergonomic keybindings.

## Features

- 🎯 Vim-style pane navigation (`hjkl`)
- ✂️ Intuitive split commands (`v` for vertical, `s` for horizontal)
- 📋 macOS clipboard integration with `pbcopy`
- 🖱️ Mouse support enabled
- 📝 Vim copy mode with visual selection
- ⚡ Quick config reload
- 🔢 Windows/panes start at 1 (not 0)

## Quick Install

### One-liner (Mac/Linux)

```bash
curl -fsSL https://raw.githubusercontent.com/RybalkaDenis/tmux-config/main/.tmux.conf -o ~/.tmux.conf && tmux source-file ~/.tmux.conf 2>/dev/null || echo "✓ Config installed! Start tmux to use it."
```

### Manual Install

```bash
# Backup existing config (optional)
mv ~/.tmux.conf ~/.tmux.conf.backup

# Download config
curl -o ~/.tmux.conf https://raw.githubusercontent.com/RybalkaDenis/tmux-config/main/.tmux.conf

# Reload if tmux is running
tmux source-file ~/.tmux.conf
```

## Keybindings

All commands use the default prefix: `Ctrl+b`

### Pane Navigation
- `prefix + h/j/k/l` - Move left/down/up/right (vim-style)
- `prefix + ←/↓/↑/→` - Move with arrow keys

### Pane Management
- `prefix + v` - Split vertically (side by side)
- `prefix + s` - Split horizontally (top/bottom)
- `prefix + H/J/K/L` - Resize pane (capital letters)

### Copy Mode
- `prefix + [` - Enter copy mode
- `v` - Start visual selection
- `y` - Yank (copy) and exit
- `hjkl` - Navigate in copy mode

### Clipboard
- `Ctrl+Shift+C` - Copy tmux buffer to clipboard
- `Ctrl+Shift+V` - Paste from clipboard
- Mouse drag automatically copies to clipboard

### Other
- `prefix + r` - Reload config
- Mouse enabled - click/drag panes and borders

## Requirements

- tmux 2.4+
- macOS (for `pbcopy` clipboard integration)
  - Linux users: replace `pbcopy` with `xclip -selection clipboard` or `xsel --clipboard`

## Uninstall

```bash
rm ~/.tmux.conf
mv ~/.tmux.conf.backup ~/.tmux.conf  # Restore backup if exists
```

## License

MIT
