# GNOME-custom

My personal GNOME desktop rice. Dark theme, macOS-inspired look.

## What's inside

- **GTK Theme:** Breeze
- **Icons:** WhiteSur-dark
- **Cursors:** capitaine-cursors
- **Fonts:** SF Pro Display / SF Mono
- **Accent:** Purple
- **Color scheme:** Prefer dark
- **WM buttons:** icon:minimize,maximize,close
- **Wallpaper:** included (`wallpaper.jpg`)
- **dconf dump:** full GNOME settings

### Extensions (bundled)

| Extension | Description |
|-----------|-------------|
| Blur my Shell | Blur effects for shell UI |
| Dash to Dock | Dock with app launchers |
| Touchpad Gesture Customization | Custom touchpad gestures |

### Extensions (NOT bundled — install manually)

| Extension | Link |
|-----------|------|
| Dash to Panel | https://extensions.gnome.org/extension/1160/dash-to-panel/ |
| Gesture Improvements | https://extensions.gnome.org/extension/4245/gesture-improvements/ |

## Prerequisites

- GNOME Shell (tested on GNOME 45+)
- `dconf` CLI tool (usually pre-installed)
- Fonts: [SF Pro](https://github.com/sahibjotsaggu/San-Francisco-Pro-Fonts) and [SF Mono](https://github.com/supercomputra/SF-Mono-Font) installed to `~/.fonts` or `~/.local/share/fonts`
- Icon theme `WhiteSur-dark` installed
- Cursor theme `capitaine-cursors` installed
- GTK theme `Breeze` installed

## Installation

```bash
# Extract the bundle
tar -xzf gnome-bundle.tar.gz
cd gnome-bundle

# Run the install script
chmod +x install.sh
./install.sh
```

The script will:
1. Copy the wallpaper to `~/.config/background`
2. Install bundled extensions to `~/.local/share/gnome-shell/extensions/`
3. Load all dconf settings (theme, keybinds, extension configs, etc.)

## After install

1. Install the two missing extensions manually (Dash to Panel, Gesture Improvements)
2. Restart GNOME Shell: `Alt+F2` → type `r` → Enter (X11) or just re-login (Wayland)
3. Enable extensions via `gnome-extensions-app` or Extension Manager if they didn't auto-enable

## Uninstall

```bash
# Reset all GNOME settings to defaults
dconf reset -f /

# Remove bundled extensions
rm -rf ~/.local/share/gnome-shell/extensions/blur-my-shell@aunetx
rm -rf ~/.local/share/gnome-shell/extensions/dash-to-dock@micxgx.gmail.com
rm -rf ~/.local/share/gnome-shell/extensions/touchpad-gesture-customization@coooolapps.com
```
