# Neni Font 🐾

**Neni** is an open-source monospaced typeface engineered for long software development sessions (**10h+ daily coding**), built upon the open-source [Meslo LG](https://github.com/andreberg/Meslo-Font) and [Bitstream Vera Sans Mono](https://www.gnome.org/fonts/) lineage — preserving the iconic proportions and glyph geometry of classic macOS developer typography while remaining **100% open-source (Apache 2.0 / Bitstream Vera)** and completely free of proprietary Apple code or metadata.

The font is named after my great three-legged companion, **Neni**!

![Neni the Mascot](./assets/Neni.jpg)

---

## 📦 Font Formats & Available Variants

The repository provides pre-built font binaries organized under the [`fonts/`](./fonts) directory:

### 1. Standard TrueType Fonts (`fonts/ttf/`)
* Lightweight, pure coding fonts (`~500 KB` per weight) without extra icon sets — ideal for code editors, IDEs, and desktop installation:
  - `Neni-Regular.ttf`
  - `Neni-Italic.ttf`
  - `Neni-Bold.ttf`
  - `Neni-BoldItalic.ttf`

### 2. Nerd Fonts Edition (`fonts/nf/`)
* Includes **10,500+ developer icons** (Font Awesome, Devicons, Octicons, Material Design Icons, Codicons, Powerline symbols, etc.). Perfect for Neovim, Starship, Powerlevel10k, tmux, Lazygit, and modern terminal prompts:
  - `NeniNF-Regular.ttf`
  - `NeniNF-Italic.ttf`
  - `NeniNF-Bold.ttf`
  - `NeniNF-BoldItalic.ttf`

### 3. TrueType Collections (`fonts/ttc/`)
* Single-file font bundles containing all 4 styles (`Regular`, `Bold`, `Italic`, `Bold Italic`) in one file:
  - `Neni.ttc` (Standard Collection)
  - `NeniNF.ttc` (Nerd Fonts Collection)

---

## 🛠️ Ergonomic Engineering for 10h+ Daily Coding

**Neni** applies surgical typographic and metric refinements designed to reduce eye strain, eliminate visual jitter, and keep terminal UIs razor-sharp across long development days:

1. **Anti-Fatigue Native Line Height (`1.25×` EM)**
   - Configured natively via `hhea.lineGap = 176` and `OS/2.sTypoLineGap = 176` (`Ascent 1901` / `Descent -483` / `2560` total units on a `2048` UPM grid, with `USE_TYPO_METRICS` enabled).
   - Gives lines of code comfortable vertical breathing room out-of-the-box without requiring manual `lineHeight` overrides in every editor.

2. **Unified Mathematical & Operator Axis (`Y = 642`)**
   - All core operators (`+`, `-`, `=`, `<`, `>`, `~`, `*`, `×`, `÷`, `±`, `≤`, `≥`, `≈`, `←`, `→`, `↔`, `⇐`, `⇒`, `⇔`, `–`, `—`, `·`) and strikethrough (`yStrikeoutPosition = 642`) are vertically centered on the exact same optical axis (`Y = 642.0`) across all 4 weights.
   - Compound sequences like `->`, `=>`, `~=`, `*=` and `!==` align on a single horizontal plane, and Italic `=` / `≐ ≑ ≒ ≓` use clean non-overlapping contours.

3. **Zero Vertical Shift & Mirrored Symmetry on Delimiters (`()`, `[]`, `{}`)**
   - Enclosing brackets `()`, `[]`, `{}` are vertically locked to `Y = 642.0` across `Regular`, `Bold`, `Italic`, and `Bold Italic` (fixing the 100-unit vertical jump between upright and bold/italic weights when syntax highlighters or rainbow-bracket plugins bold active brackets).
   - Left and right outer margins are mirrored around the horizontal cell center (`X = 616.5`) across all 4 styles (including `Italic` and `Bold Italic`) so opening and closing delimiters sit at identical distances from enclosed text.

4. **Horizontal Optical Centering (`X = 616.5`) & Round Baseline Punctuation (`.`, `,`, `:`, `;`)**
   - Code symbols (`+`, `-`, `=`, `<`, `>`, `~`, `*`, `/`, `\`, `|`, `!`, `:`, `.`, `'`, `"`, `` ` ``, `$`, `@`, `#`, `·`) are horizontally centered inside the `1233`-unit monospace cell (following the `-11°` slant axis on Italic/Bold Italic for `.`, `,`, `:`, `;`).
   - `.`, `,`, `:` and `;` use clean round geometry anchored directly on baseline `Y = 0` (`0..376` Regular/Italic, `0..416` Bold/Bold Italic), with identical upper dots on `:` and `;` flush with x-height (`Y = 1120`) and identical smooth round comma tails (`Y = -320`) on `,` and `;`.
   - `_` spans full-bleed (`0..1233`) seamlessly across all 4 weights, `|` locks to `Y = -483..1565` with zero weight jump, and `hmtx` left sidebearings match `glyf.xMin` with zero mismatches across all glyphs.

5. **Zero Ligatures (Strict 1:1 Character Grid)**
   - All OpenType ligature tables (`GSUB`, `GPOS`, `GDEF`) and precomposed ligature glyphs (`fi`, `fl`, `ff`, `ffi`, `ffl`, `U+FB00..U+FB06`) are completely stripped. Every character you type renders strictly in its own cell.

6. **Seamless Full-Bleed Terminal Box Drawing (`U+2500..U+259F`) & Powerline**
   - All 160 Box Drawing and Block Element glyphs are unified across all 4 weights to span the full vertical envelope (`-697` to `+2115`), matching Powerline dividers (`U+E0B0..U+E0BF`) so TUI borders in `tmux`, `Neovim`, `btop`, and `Lazygit` connect without horizontal gaps even at `1.25×` line height.

7. **Clean IDE Diagnostic Underlines & Sanitized `U+FEFF` BOM**
   - `post.underlinePosition` lowered from `-130` to `-220` (`underlineThickness = 95`) so compiler/LSP wavy and solid underlines never collide with the baseline or descenders (`g`, `p`, `q`, `j`, `y`).
   - Unmapped `U+FEFF` (UTF-8 Byte Order Mark / Zero-Width No-Break Space) so files containing a BOM never render stray icon glyphs.
   - Strict monospace flag (`post.isFixedPitch = 1` and `PANOSE.bProportion = 9`) enforced on all 4 styles, with unified symmetric ClearType/grayscale smoothing (`gasp = 0x000A`).

---

## 🚀 Installation Guide

### Desktop (Windows, macOS, Linux)

1. Navigate to the [`fonts/`](./fonts) directory in this repository.
2. Choose your preferred edition:
   - **Standard edition**: Install from `fonts/ttf/` or `fonts/ttc/Neni.ttc`.
   - **Nerd Fonts edition**: Install from `fonts/nf/` or `fonts/ttc/NeniNF.ttc`.
3. Install on your OS:
   - **Windows**: Select the font files -> Right-click -> **Install** (or **Install for all users**).
   - **macOS**: Double-click the font files -> Click **Install Font** in Font Book.
   - **Linux**: Copy the font files to `~/.local/share/fonts/` and run `fc-cache -f -v`.

### Configuring in your Editor / Terminal

* **VS Code / Cursor / Zed**:
  ```json
  "editor.fontFamily": "'Neni', 'Neni NF', monospace",
  "editor.fontLigatures": false
  ```

* **Alacritty / Kitty / WezTerm / Ghostty / Windows Terminal**:
  Set font family to `Neni NF` (or `Neni`).

---

## 🌐 Web Specimen & Playground

Open [`index.html`](./index.html) in any browser to test **Neni** and **Neni NF** live:
- Interactive code editor playground.
- Side-by-side comparison of `Regular`, `Italic`, `Bold`, and `Bold Italic`.
- Highlight showcase of aligned operators (`Y = 642`), symmetric brackets, and full-bleed Box Drawing.
- Toggle between Standard (`Neni`) and Nerd Fonts (`Neni NF`) with live size and theme controls.

---

## 📜 Licensing & Terms (Apache 2.0 & Bitstream Vera)

**Neni** is 100% open-source software distributed under the **Apache License, Version 2.0** and the **Bitstream Vera Font License** (with Nerd Fonts glyph patches under the **MIT License**).

- Free for **personal and commercial use**, modification, bundling, and redistribution.
- Contains **zero proprietary Apple binary data, trademarks, or brand icons**.
- Full license texts and copyright notices are available in [LICENSE.md](./LICENSE.md).

---

## 🤝 Credits

- **Bitstream Vera Sans Mono:** Designed by **Jim Lyles** at Bitstream Inc. — the foundational typeface of this family tree.
- **Meslo LG:** Created by **André Berg** under the Apache 2.0 License, adapting Bitstream Vera Sans Mono to match classic macOS monospace proportions.
- **Nerd Fonts:** Created by **Ryan L McIntyre (ryanoasis)** and contributors for the developer icon sets.
- **Neni:** The best dog and programming assistant in the world, who inspired this project. 🐾
