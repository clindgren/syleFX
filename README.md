# styleFX-KSH.lib

---

**Version:** 0.0.5

**Shell:** KornShell 93 (KSH93)

**License:** Dual License - MPL-2.0 GPL-3.0

---

## Overview

`styleFX-KSH.lib` is a minimalist ANSI styling library designed for use with **KornShell 93**. It defines ANSI escape sequences using **compound variables**, enabling styled output with no unnecessary function overhead. This design keeps the library fast, modular, and easy to integrate into larger projects.

Unlike bloated frameworks, this library avoids in-line documentation and runtime variable logic. It is structured for use with a custom preprocessor that removes tagged comments (`#C#`, `#D#`, etc.) and retains only executable declarations.

---

## Features

- ANSI text styling for bold, italic, dim, underline, inverse, blink, and hidden text
- Foreground and background color definitions
- Uses compound variables (e.g., `styleFX.fg.red`)
- Designed for use with preprocessors and strict KSH environments
- Does not embed loader or comment bloat

---

## Usage

```ksh
. /path/to/styleFX-KSH.lib

print -n "${styleFX.bold}${styleFX.fg.cyan}Hello, World!${styleFX.reset}\n"
```

---

## Output Example

```
Hello, World!
```
*Text appears bold and cyan in compatible terminals.*

---

## Preprocessing Tags

This library uses standardized comment tags to assist with source parsing and documentation extraction:

- `#L#` → Layout and divider lines
- `#S#` → Section headers
- `#C#` → Internal developer comments
- `#D#` → Documentation comments (strippable for minimal builds)

---

## Developer Philosophy

- Documentation and help content are stored **outside** the core library
- Loading behavior is controlled by the developer's environment or script
- No embedded function logic or dynamic evaluation — this keeps execution clean

---

## Planned Enhancements

- Semantic themes (e.g., `styleFX.alert.warning`, `styleFX.status.ok`)
- Optional support for 256-color and truecolor (RGB)
- Extension libraries for terminal-specific controls (e.g., `styleFX-gnome-term.lib`)

---

## Author

[Binware-Core](https://github.com/clindgren)

[GitHub](https://github.com/clindgren)

---

## License

This project is released under a dual license with provisions:

- [Mozilla Public License V-2.0](https://opensource.org/license/mpl-2-0)
- [GNU GPLv3.0](https://www.gnu.org/licenses/gpl-3.0.html)

