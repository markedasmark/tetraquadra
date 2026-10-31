<div align="center">

# tetraquadra

Smaller dotfiles

[![OS](https://img.shields.io/badge/OS-Linux_Wayland-0e0e0e?style=flat-square)](#)
[![WM](https://img.shields.io/badge/WM-DriftWM/Swindle-0e0e0e?style=flat-square)](#)
[![Shell](https://img.shields.io/badge/Shell-Zsh-0e0e0e?style=flat-square)](#)
[![Bloat](https://img.shields.io/badge/Bloat-0%25-d64933?style=flat-square)](#)

*DriftWM · Swindle · Alacritty · Zsh · Waybar · Wofi · SwayNC*

</div>

## Overview

Plain config files, nothing else — no install script, no framework, no bloat. Take what you need.

- **Near-monochrome palette** — dark gray, light gray, one red accent, zero rounded corners
- **DriftWM** — Canvas wayland compositor (hevel-like)
- **Swindle** — dwm-style tiling compositor (tags + dwindle layout) as the alternative setup
- **Zsh** — hand-rolled prompt that shows file-type icons per path segment, no prompt framework
- **Firefox** — userChrome theme so the browser matches the rest
- **Cava** — audio visualizer with custom GLSL shaders

## What's inside

```
.
├── alacritty/       terminal + colors
├── btop/            system monitor
├── cava/            audio visualizer + GLSL shaders
├── driftwm/         infinite-canvas wayland compositor
├── micro/           terminal editor
├── swaync/          notification center
├── swindle/         tiling compositor (dwm-style tags)
├── waybar/          status bar
├── wofi/            app launcher
├── userChrome.css   firefox theme
├── zprofile         login environment
└── zshrc            shell, aliases, prompt
```

## Keybinds

DriftWM — `Super` is the mod key:

| Keys | Action |
|---|---|
| `Super + T` | Terminal |
| `Alt + Space` | App launcher |
| `Super + Q` | Firefox |
| `Super + E` | File manager |
| `Super + N` | Notifications |
| `Super + L` | Lock screen |
| `Super + Esc` | Power menu |
| `Super + O` | Zoom out to see the whole canvas |
| `Super + Wheel` | Zoom in / out |
| `Super + Arrows` | Focus nearest window |
| `Super + Ctrl + Arrows` | Pan the canvas |
| `Super + Shift + Arrows` | Nudge window |
| `Super + Shift + Ctrl + Arrows` | Move window to another monitor |
| `Super + F` / `Super + Shift + F` | Fit / fullscreen |
| `Super + W` | Close window |
| `Super + 1–4` | Jump to canvas bookmarks |

Media, volume and brightness keys work out of the box (PipeWire, playerctl, brightnessctl).

## Palette

| Role | Hex | |
|---|---|---|
| Background | `#0e0e0e` | ![](https://img.shields.io/badge/x-x-0e0e0e?style=flat-square&labelColor=0e0e0e) |
| Terminal background | `#131313` | ![](https://img.shields.io/badge/x-x-131313?style=flat-square&labelColor=131313) |
| Foreground | `#e2e2e2` / `#ebebeb` | ![](https://img.shields.io/badge/x-x-e2e2e2?style=flat-square&labelColor=e2e2e2) |
| Accent | `#d64933` | ![](https://img.shields.io/badge/x-x-d64933?style=flat-square&labelColor=d64933) |
| Dim text | `#8a8a8a` | ![](https://img.shields.io/badge/x-x-8a8a8a?style=flat-square&labelColor=8a8a8a) |

Fonts: **IosevkaTerm Nerd Font Propo** (terminal, bar) and **GoMono Nerd Font** (launcher, notifications).

## Dependencies

```
alacritty  btop  cava  driftwm  eza  fastfetch  flameshot  hyprlock  micro
nautilus  playerctl  swaybg  swaync  swindle  waybar  wofi  wofi-emoji
wofi-power-menu  wireplumber  brightnessctl  zsh
```

Plus a Nerd Font or two.

## Installation

No script — symlink or copy things where they belong:

1. Config directories go to `~/.config/<name>`: `alacritty`, `btop`, `cava`, `driftwm`, `micro`, `swaync`, `swindle`, `waybar`, `wofi`
2. Shell files go to `~/.zshrc` and `~/.zprofile`
3. For Firefox, copy `userChrome.css` into `<profile>/chrome/` and enable `toolkit.legacyUserProfileCustomizations.stylesheets` in `about:config`

## Notes

- **The canvas model** — DriftWM replaces workspaces with an infinite canvas. `Super + 1–4` are just bookmarks that fly the camera to saved positions; you can also pan and zoom freely and arrange windows anywhere.
- The prompt icon map, aliases and history settings live directly in `zshrc` — everything is in plain sight.
