# styleFX-KSH.lib

**Version:** 0.0.5
**Shell:** KornShell 93 (KSH93)  
**License:** Dual Licensed MPL-2 GPL-3.0

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
