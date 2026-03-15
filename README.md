# Pip-Boy Terminal Theme for Home Assistant

A Fallout Pip-Boy / Vault-Tec terminal aesthetic theme for Home Assistant.
Derived from [Nezz's visionOS theme](https://github.com/Nezz/homeassistant-visionos-theme),
rebuilt as a post-apocalyptic CRT phosphor terminal.

Two variants are included:

**Pip-Boy** -- Fallout 3/4 phosphor green on near-black `#0C0C0C`

**Pip-Boy Amber** -- Fallout New Vegas burnt orange-gold on warm near-black `#0D0800`

### Pip-Boy (Green)
<img width="800" alt="Pip-Boy green theme" src="screenshots/pipboy.png" />

### Pip-Boy Amber
<img width="800" alt="Pip-Boy Amber theme" src="screenshots/pipboy-amber.png" />

## Features

- Phosphor green or amber CRT palette throughout
- Scanline overlay on all cards simulating CRT display lines
- Vignette effect darkening screen edges like a real CRT
- Subtle phosphor flicker animation on the full interface
- Partial border chrome on section headers (top + right only) matching Pip-Boy UI panels
- Phosphor glow text-shadow on section headers
- Square corners everywhere -- no rounded Apple-style cards
- Monospace terminal font (Share Tech Mono) applied globally
- Sidebar scanline treatment
- Semantic color thresholds: phosphor green = nominal, amber = caution,
  orange = warning, red = critical

## Requirements

- [card-mod](https://github.com/thomasloven/lovelace-card-mod) (install via HACS)

## Installation

1. Copy `themes/pipboy/pipboy.yaml` into your Home Assistant
   `config/themes/pipboy/` directory.

2. Add the following to your `configuration.yaml` if not already present
   (reboot required):
```yaml
frontend:
  themes: !include_dir_merge_named themes
```

3. Reload themes via **Settings > System > Restart menu > Quick reload**,
   or call the service:
```yaml
service: frontend.reload_themes
```

4. Select **Pip-Boy** or **Pip-Boy Amber** from your profile theme dropdown.

## Font

The theme uses [Share Tech Mono](https://fonts.google.com/specimen/Share+Tech+Mono)
loaded via Google Fonts. An internet connection is required on first load for the
font to render correctly. If running a fully local HA setup, host the font locally
and update the `@import` URL in `card-mod-root`.


The `liquid_glass.yaml` file is kept as a reference base. Do not edit it directly.

## Remarks

Derived from [Nezz's visionOS & Liquid Glass Theme](https://github.com/Nezz/homeassistant-visionos-theme)

Originally based on [Bas Nijholt's iOS Themes](https://github.com/basnijholt/lovelace-ios-themes)

Dropdown fixes from [Wessam Lauf's Frosted Glass Theme](https://github.com/wessamlauf/homeassistant-frosted-glass-themes)