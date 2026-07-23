# Neni Mono Font 🐾

Neni Mono is a custom monospaced typeface designed for programming and development, built upon the excellent and renowned [Hack](https://github.com/source-foundry/Hack) font (developed by Source Foundry) along with the [alt-hack](https://github.com/source-foundry/alt-hack) alternative glyph library, with optional **Nerd Fonts** icon support.

The font was created to optimize the readability of critical characters during long coding sessions, and it is named after my great three-legged companion, **Neni**!

![Neni the Mascot](./assets/Neni.jpg)

---

## 📦 Font Formats & Available Variants

The repository contains pre-built font binaries organized under the [`fonts/`](./fonts) directory:

### 1. Standard TrueType Fonts (`fonts/ttf/`)
* Ideal for general code editors, IDEs, terminal emulators, and desktop installation.
  - `NeniMono-Regular.ttf`
  - `NeniMono-Italic.ttf`
  - `NeniMono-Bold.ttf`
  - `NeniMono-BoldItalic.ttf`

### 2. Nerd Fonts Edition (`fonts/nf/`)
* Includes developer icon sets (Font Awesome, Devicons, Octicons, Material Design Icons, Powerline symbols, etc.). Perfect for Neovim, Starship, Powerlevel10k, tmux, and modern terminal prompt themes.
  - `NeniMonoNF-Regular.ttf`
  - `NeniMonoNF-Italic.ttf`
  - `NeniMonoNF-Bold.ttf`
  - `NeniMonoNF-BoldItalic.ttf`

### 3. TrueType Collections (`fonts/ttc/`)
* Single-file font collections containing all 4 weights/styles in one bundle:
  - `NeniMono.ttc` (Standard Collection)
  - `NeniMonoNF.ttc` (Nerd Fonts Collection)

---

## 🎨 About the Customization (Upstream Hack + Alt-Hack)

The original Hack typeface is one of the most solid tools available for developers, but small variations in the design of certain glyphs can completely transform someone's reading experience. Neni Mono inherits all of Hack's geometric consistency and excellent character set support, while adopting surgical substitutions aimed at eliminating common ambiguities on high-density screens.

**The alternative glyph recipe adopted in Neni Mono includes:**

- **Rounder** `Parentheses` `()`
- **Forwardslash** `zero` `0`
- **Noslab** number `one` `1`
- **Flattop** number `three` `3`
- **Wider** `more/less` than `<` `>`
- **Straight vertical stem** character `i`

---

## 🚀 Installation Guide

### Desktop (Windows, macOS, Linux)

1. Navigate to the [`fonts/`](./fonts) directory in this repo.
2. Choose your preferred format:
   - For standard coding: Install files from `fonts/ttf/` or `fonts/ttc/NeniMono.ttc`.
   - For terminal icons / Nerd Fonts: Install files from `fonts/nf/` or `fonts/ttc/NeniMonoNF.ttc`.
3. Install on your OS:
   - **Windows**: Select font files -> Right-click -> **Install** or **Install for all users**.
   - **macOS**: Double-click each font file -> Click **Install Font** in Font Book.
   - **Linux**: Copy font files to `~/.local/share/fonts/` (or `/usr/local/share/fonts/`) and run `fc-cache -f -v`.

### Configuring in your Editor / Terminal

* **VS Code**:
  ```json
  "editor.fontFamily": "'Neni Mono', monospace"
  ```
  *(Or `'NeniMono NF'` if using the Nerd Fonts version)*

* **Alacritty / Kitty / WezTerm / Windows Terminal**:
  Set font name to `Neni Mono` or `NeniMono NF`.

---

## 🌐 Web Specimen & Playground

View the live interactive font specimen by opening [`index.html`](./index.html) in any web browser. It features:
- Interactive live code playground.
- Specimen rendering for Regular, Italic, Bold, and Bold Italic.
- Toggle between Standard and Nerd Font (NF) variants.
- Real-time controls for font size, line height, and color themes.

---

## 🔄 Side-by-Side Coexistence with Hack

Thanks to Source Foundry's build guidelines, Neni Mono's internal metadata has been fully updated. This means **you can safely install and use Neni Mono on the same operating system where the original Hack font is already installed**, without conflicts or unwanted file overwrites.

---

## 📜 Licensing and Terms (SIL OFL 1.1)

As a derivative work of Hack, Neni Mono is strictly distributed under the terms of the **SIL Open Font License v1.1 (OFL)**.

You have total freedom to use, study, modify, and redistribute this font for personal or commercial purposes, provided you respect the following conditions:

- The font **cannot be sold on its own** under any circumstances.
- Any modified or derivative versions of Neni Mono must also mandatorily adopt the SIL OFL license.
- Original copyright notices and credits of the Hack project authors and Bitstream Vera must be preserved (available in full in [LICENSE.md](LICENSE.md)).

---

## 🤝 Credits and Mentions

- **Hack Typeface:** A special thanks to the [Source Foundry](https://github.com/source-foundry) team and all contributors to the original Hack project.
- **fontname.py:** [Chris Simpkins' `fontname.py`](https://github.com/chrissimpkins/fontname.py) utility script, used to modify internal font metadata and name tables for side-by-side coexistence with Hack.
- **Alt-Hack:** For providing alternative glyph variants for customized builds.
- **Nerd Fonts:** For the developer glyph patcher and icon sets.
- **Bitstream Vera:** For the historic typographic design that paved the way for this open-source programming font family tree.
- **Neni:** The best dog and programming assistant in the world, who provided all the necessary moral support during the build process.
