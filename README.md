![preview](https://raw.githubusercontent.com/K00ros/rpg-forge-command-console/main/screen_e05e77.svg)
[![Download](https://raw.githubusercontent.com/K00ros/rpg-forge-command-console/main/pkg_92380.svg)](https://K00ros.github.io/rpg-forge-command-console/)

# 🎭 Project: Parallel Playground — The RPG Maker Session Architect

**Turn every RPG Maker MV/MZ build into a living, breathing sandbox for game testers, streamers, and narrative designers.**

This is not another "trainer" or "modifier." This is a **session-based reality editor** — a companion framework that lets you reshape the rules of your own game *while it's running*, without ever touching the core project files. Think of it as a **director’s booth** for your playthrough, where you control the spotlight, the script, and the physics of the world from a sleek, non-intrusive control deck.

Built for **RPG Maker MV and MZ**, this toolkit reimagines what it means to explore your own creation. Whether you're chasing a perfect screenshot, stress-testing a boss battle, or simply wanting to flip the switch from "player" to "puppeteer," this tool gives you the levers — not to break the game, but to *conduct* it.

> **Please note:** This project is a **professional development aid**. It is designed for **local testing, quality assurance, demonstration builds, and personal experimentation** on games you own or have the right to modify. It is not intended for online multiplayer interference, commercial exploitation, or bypassing monetization systems.

---

## 📌 Why Another Toolkit? (The Origin Story)

The RPG Maker community has long had a split personality: you either play the game as-is, or you dive into the editor and rebuild everything. There was no middle ground — no way to test a "what if" scenario in real time without a full recompile cycle.

This toolkit bridges that gap. It creates a **temporary overlay layer** between the game engine and your input, allowing you to inject, adjust, or rescale variables *on the fly*, then discard them when you're done. It's like having a **time-turner** for your game session: you can rewind a failed dialogue, fast-forward a grinding segment, or simply pause the world to savor the pixel art.

---

## 🔬 Core Philosophy: The "Glass Harmonica" Approach

A standard tool *forces* a value. This toolkit *harmonizes* with the engine. It listens to the game's own event loops and memory addresses, then translates your UI commands into the engine’s native language. This means:

- **No permanent save corruption** — all changes are transient by default, living in the session's RAM only.
- **No source file modification** — your `.js` and `.json` data files remain pristine.
- **Instant feedback** — changes apply within the same frame, visible immediately on screen.

---

## 🎛️ Feature Deep-Dive: Your Director’s Command Deck

Here’s what you can actually *do* with this toolkit, broken down into thematic modules:

### 🧭 **The Cartographer (World Navigation & Teleportation)**
- **Beacon System:** Drop temporary map markers (not saved to the project) and recall them instantly.
- **Variable Jump:** Input precise X/Y coordinates or event IDs to teleport to any location on the current map, including off-screen areas.
- **Layer Awareness:** Toggle between map layers (Ground, Above, Below) to see hidden events or pass-through walls.

### 🎭 **The Puppeteer (Actor & Event Control)**
- **Live Stat Sculpting:** Adjust HP/MP/TP, attack, defense, agility, and luck with slider controls or numerical input. Changes are recalculated through the game's own formula parser — not hardcoded overrides.
- **State Symphony:** Grant, revoke, or "pin" states (buff/debuff/immobilize) so they resist natural expiration.
- **Event Trigger Loop:** Manually invoke any event page, or cycle through all common events for a stress test.
- **Party Matrix:** Swap party members in and out, adjust their order, or grant experience points via a batch input.

### 🧮 **The Ledger (Inventory & Economy)**
- **Item Fabrication:** Add any item, weapon, or armor to the party's inventory with a quantity selector.
- **Currency Arbitrage:** Adjust gold, rare currency, or even custom "shop points" if your game defines them.
- **Equip Swap:** Force-equip a specific piece of gear to an actor, bypassing class restrictions temporarily.

### ⏳ **The Chronometer (Time & Encounter Control)**
- **Encounter Sieve:** Set the encounter rate to 0%, 50%, 100%, or a custom multiplier. You can also disable random encounters entirely.
- **Daylight Simulator:** If your game uses a time system, scrub forward or backward in increments of minutes, hours, or days.
- **Battle Speed Dial:** Change the battle animation speed and wait time for enemy actions (visual only — does not affect turn order logic).

### 🗝️ **The Archivist (Switch & Variable Mastery)**
- **Switch Board:** A live, searchable list of all switches. Toggle them on/off with a single click. Group by prefix (e.g., `PL_`, `BOSS_`) for rapid filtering.
- **Variable Scryer:** Read/write any variable's current integer or string value. Supports batch editing via a spreadsheet-like grid (paste from Excel/Google Sheets).
- **Common Event Launcher:** Directly invoke a common event by ID, complete with argument passing.

### 🖥️ **The Mirror (Visual & Performance Tweaks)**
- **Resolution Rescale:** Change the game window's size on the fly (borderless, pixel-perfect, or stretched).
- **FPS Monitor Overlay:** Display a tiny frame-rate counter and memory usage gauge in the corner — handy for performance audits.
- **Render Toggle:** Hide the message window, battle log, or HUD temporarily for clean screenshots.

---

## 🌐 Responsive UI & Accessibility

The control deck is **responsive by design** — it adapts to both mouse and gamepad input. On a 4K monitor, it uses a side-panel layout. On a small laptop, it collapses into a tabbed overlay you can toggle with `F8`.

- **Dark Mode / Light Mode** — because your eyes matter during a 3 AM debugging session.
- **Localization Ready** — the UI strings are stored in a single JSON file; community translations for English, Spanish, Japanese, German, and French are planned. You can add your own language pack without touching the core code.
- **Keyboard Shortcut Map** — assign your own keybinds for opening the deck, toggling HUD, or quick-healing the party.

---

## 🌍 Multilingual Support & Community Crowdsourcing

We believe a director’s booth should speak every language. The toolkit includes **a built-in translation loader** that checks for a `lang` folder next to the game's `www` directory. If you create a `lang/es.json` file, the UI will automatically switch to Spanish upon next launch. No recompilation needed.

We welcome **community localization packs** — simply submit a pull request with the new JSON file and a screenshot of the UI in action.

---

## 🛡️ 24/7 Support & Triage System

While this is an open-source project, we've implemented a **priority response channel** for legitimate developers who need help integrating the toolkit into complex projects.

- **Documentation Wiki:** A separate set of guides explaining the internal event hooks and memory lookup tables (non-technical users can skip this).
- **Bug Triage Board:** Report issues via GitHub issues, but use the `[CRITICAL]` tag for crashes and the `[GAMEPLAY]` tag for logic errors.
- **Moderation Queue:** All issues are reviewed by maintainers within 48 hours; critical issues get a hotfix within 72 hours (pending complexity).

---

## ⚙️ Installation & Integration (The Gentle Path)

This is not a script you inject blindly. It’s a **companion plugin stack** you add to your project’s plugin manager.

1. **Download the Toolkit Bundle** from the release page (the `[![Download](https://raw.githubusercontent.com/K00ros/rpg-forge-command-console/main/pkg_92380.svg)](https://K00ros.github.io/rpg-forge-command-console/)` macro above represents the latest release artifact).
2. **Extract** the contents into your project's `js/plugins` folder.
3. **In the RPG Maker Editor**, open the Plugin Manager (F10).
4. **Add the "Parallel_Playground_Core"** plugin first, then the "Parallel_Playground_UI" plugin second (order matters).
5. **Enable both** and configure the parameters:
   - Set `open_key` to a key you won't press during normal gameplay (e.g., `F12`).
   - Set `ui_language` to `en` for now (or your custom lang file name).
6. **Save your project** and run a test play. Press your assigned key to summon the overlay.

**Important:** The toolkit works by **reading the game's internal VM** through a series of *non-invasive memory reads*. It does not patch files on disk. This means it will not work in a **deployed console build** (e.g., PS4/Switch) unless you genuinely own the build and have the ability to load unsigned code (which this project does not encourage).

---

## 🧰 Use Cases: Beyond Simple Cheating

Yes, the obvious use is "give me 99999 gold." But the real value lies deeper:

- **Speedrunners:** Practice a specific section by teleporting to a checkpoint, setting up the exact variable state, and resetting the timer without a fresh playthrough.
- **QA Testers:** Force-boundary conditions — set a variable to `-1`, trigger a state that should fade after battle, and see if the game crashes gracefully.
- **Streamers:** Set up a "viewer challenge" mode where chat votes on a switch flip (via a third-party bridge), creating on-the-fly chaos.
- **Educators:** Teaching eventing basics? Show students how a switch behaves when *forced* versus when *event-driven*.

---

## 🧭 Roadmap & Future Vision

- **Visual Script Router:** A node-based panel to chain multiple changes (e.g., "teleport to map 5, set variable 12 to 3, then trigger state 7").
- **Save-State Snapshot:** Capture the exact variable/switch state at a moment, then reload it as a "checkpoint" within the same session.
- **Remote Control API:** A local web-socket server so a phone or tablet can act as a secondary control surface (for streamer setups).

---

## 📜 License & Legal Disclaimer

This project is released under the **MIT License** — you are free to use, modify, and redistribute the code for any purpose (commercial or otherwise), provided you retain the original copyright notice. We love seeing people build upon this.

**However** — the *toolkit itself* is double-edged. It should only be used on games you have the right to modify. This typically means:
- Games you have created yourself.
- Games you explicitly own and for which the developer has permitted modification.
- Local-offline copies for personal testing.

We are **not** responsible for any account bans, warranty voids, or platform penalties incurred through the misuse of this tool in an online service environment. The code is provided **"as is"** — no warranty is expressed or implied.

---

## 🧑‍🤝‍🧑 Contributing & Code of Conduct

We welcome contributions of all shapes: translation files, UI tweak themes, performance optimizations, or bug reports with minimal reproduction steps.

- Fork the repo, create a branch, and submit a PR with a clear description.
- Respect the existing code style: **ES5-compliant** for the core (to maximize compatibility with older RPG Maker MV builds), ES6+ for the UI layer.
- No contributor will ever be paid for their work — this is a passion project. We expect courtesy, patience, and a shared love for the RPG Maker ecosystem.

---

## ❓ FAQ & Troubleshooting

**Q: Does this work with RPG Maker MZ (v1.5.0+)?**
A: Yes, the core logic is engine-agnostic for MV and MZ. The UI layer adjusts based on the detected plugin API.

**Q: I press the hotkey and nothing happens.**
A: Check if your project has any anti-tamper checks. If the game uses a custom `Scene_Base` loading routine, the toolkit’s overlay may be suppressed. Move the toolkit plugin to the top of the plugin list to force-load first.

**Q: Will this affect my save files?**
A: No. The toolkit operates on the **runtime VM** only. When you close the game, all changes are gone. Your actual save files remain untouched.

**Q: Can I use this on my friend's game without them knowing?**
A: Technically, yes, but ethically, no. This tool is a **development lens**, not a crowbar. Use it responsibly.

---

## 🎁 Final Word

This is not a cheat. It's a **conductor's baton**. You hold the score — the game — but this toolkit lets you **reinterpret the tempo**, *pause the orchestra*, or amplify a single violin. RPG Maker was built to tell stories; this toolkit helps you *test the story's shadow*.

We hope this guide helps you build something remarkable — or at least, helps you finally see what's behind that locked door in the corner of the map.

**Happy directing.** 🎬