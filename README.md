# 1clicklangs
1Click is a native macOS app that lets you install any programming language in one click — no Terminal commands, no Homebrew juggling, no documentation hunting. Pick a language or a Bundle, hit Install, and get back to building.

---

## Features

### Live Dashboard
See your entire language environment at a glance — installed count, disk usage, version coverage, recent installs, and per-category progress. Inspired by the best package manager GUIs, built for languages.

### Language Bundles
7 hand-curated stacks let you install an entire domain in one tap:

| Bundle | Languages |
|---|---|
| **Web Dev** | Node.js, TypeScript, Deno, Bun, CoffeeScript |
| **Systems** | Rust, Go, Zig, C, C++, D |
| **ML / Data** | Python, Julia, R, Cython |
| **Scripting** | Python, Ruby, Perl, Lua, Raku |
| **Functional** | Haskell, OCaml, Elixir, Erlang, Clojure, F# |
| **Mobile** | Swift, Kotlin, Dart, Java |
| **Blockchain** | Solidity, Rust, Vyper, Go |

### CLI Companion
Install languages from any terminal window. Run `oneclick install` and 1Click queues it with live progress — no copy-pasting brew commands.

```bash
oneclick install nodejs typescript deno
oneclick install rust go zig
oneclick uninstall ruby
oneclick list
```

Install the CLI from **Settings → CLI Companion → Install CLI**.

### Everything else
- **147 languages** across 13 categories — Web, Systems, Mobile, Functional, Data / AI, Blockchain, Game Dev, Shading, Infrastructure, Embedded, and more
- **Detects what's already installed** — scans system paths on launch and marks existing tools automatically
- **Real download progress** — live per-language progress bar, not a spinner that lies
- **Up to 3 concurrent downloads** — the rest queue automatically
- **Real language icons** — every language shows its actual logo, not a generic emoji
- **Modifies your PATH** — adds installed tools to your shell profile so they work immediately in any terminal
- **Menu Bar companion** — a lightweight status widget showing installed count and version coverage without opening the app
- **Install history** — every install is logged with version and timestamp, accessible in Settings → History
- **88% version coverage** — latest stable versions fetched from Homebrew CDN, npm, PyPI, GitHub Releases, and endoflife.date, cached and refreshed every 6 hours

---

## Install

### Homebrew (recommended)

```bash
brew tap NurikDz/apps && brew install --cask oneclick
```

### Manual

1. Download **OneClickLangs.dmg** from [Releases](https://github.com/NurikDz/1clicklangs/releases)
2. Open the DMG and drag **OneClickLangs.app** to your Applications folder
3. Launch the app — then go to **Settings → CLI Companion → Install CLI** to set up the terminal tool

> **Gatekeeper notice:** The app is ad-hoc signed (not notarized). On first launch, right-click → Open if macOS blocks it.

---

## Languages

| Category | Count | Examples |
|---|---|---|
| Web Frontend | 12 | TypeScript, Elm, WebAssembly, CoffeeScript, PureScript |
| Web Backend | 18 | Go, Python, Ruby, PHP, Elixir, Scala, Crystal |
| Systems | 14 | Rust, Zig, C, C++, Nim, Odin, Carbon, D |
| Functional | 17 | Haskell, OCaml, F#, Clojure, Erlang, Racket, Lean |
| Data / AI / ML | 10 | Julia, R, Mojo, Cython, Hy |
| Game Dev | 10 | GDScript, Lua, GLSL, Wren, AngelScript |
| Blockchain / Web3 | 6 | Solidity, Vyper, Move, Cairo, Cadence |
| Infrastructure | 14 | Terraform, Nix, Pkl, Nickel, Dhall |
| Mobile | 4 | Swift, Kotlin, Dart, Java |
| Embedded / IoT | 4 | MicroPython, CircuitPython, Arduino, Forth |
| Creative / Education | 6 | Processing, Scratch, Logo, Snap! |
| Shading / GPU | 7 | GLSL, HLSL, WGSL, Metal, SPIR-V |
| Historical / Legacy | 25 | COBOL, Fortran, Pascal, Ada, BASIC, Lisp |

---

## Requirements

- macOS 14 Sonoma or later
- Apple Silicon or Intel Mac
- Internet connection for downloading languages and version data

---

## How version data works

1Click pre-fetches the latest stable version for each language at startup and refreshes every 6 hours. Sources:

| Source | Languages | Notes |
|---|---|---|
| Homebrew CDN | 54 | No rate limits |
| endoflife.date | 13 | Python, Terraform, and others |
| npm registry | 7 | TypeScript, Solidity, AssemblyScript… |
| PyPI | 3 | Vyper, Cython, Hy |
| GitHub Releases | 53 | Used as last resort — rate-limited |
| Not trackable | 17 | Commercial / Windows-only / ancient |

---

## Building from source

```bash
git clone https://github.com/NurikDz/1clicklangs
open 1clicklangs/OneClickLangs.xcodeproj
```

Requires Xcode 15+ and macOS 14 SDK. No external dependencies — pure Swift and SwiftUI.
<img width="1392" height="912" alt="Screenshot 2026-06-15 at 01 42 27" src="https://github.com/user-attachments/assets/7a3265bd-e680-4694-b76e-dec559c181d2" />
<img width="1392" height="912" alt="Screenshot 2026-06-15 at 01 42 23" src="https://github.com/user-attachments/assets/6abab34d-7305-4be7-8efc-2ab029f8ebcd" />
<img width="1392" height="912" alt="Screenshot 2026-06-15 at 01 42 20" src="https://github.com/user-attachments/assets/76ac6845-10c6-4c2c-927e-30e4b9332fd3" />
