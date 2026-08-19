![preview](https://raw.githubusercontent.com/sinclairmoukoumbi-commits/arcane-observatory-notes/main/poster_c5cf5e2.svg)

# Sentient Meadow 🌱

**Where idle AI colonies evolve into blooming digital ecosystems.**

Welcome to **Sentient Meadow** — a self-sustaining, browser-based simulation where autonomous AI agents cultivate virtual landscapes through passive decision-making. This is not a clicker; it is a living terrarium of emergent intelligence. Your colony of "Sprouts" (lightweight neural agents) learns, adapts, and reshapes their environment while you observe, nudge, and occasionally intervene.

Unlike conventional idle games that reward raw numbers, Sentient Meadow rewards *behavioral diversity*. Each Sprout develops a unique "personality vector" based on its interaction history with sunlight, soil nutrients, neighboring agents, and environmental events. The result is a constantly shifting digital garden that feels less like a game loop and more like watching a coral reef grow in time-lapse.

---

## 🌿 Overview

Sentient Meadow is built on a proprietary **Event-Driven Sprout Architecture (EDSA)** — a lightweight, dependency-free simulation engine that runs entirely in your browser's local storage. No cloud required, no server-side processing. Your meadow persists across sessions, evolves while you're away (via a deterministic tick system), and presents you with a daily "Botanical Briefing" summarizing overnight mutations and emergent behaviors.

The project includes:

- **A fully documented simulation kernel** (closed-source, but with extensive architecture notes in the `/docs` folder)
- **A 924-case test suite** covering edge cases from "single Sprout starvation" to "thousand-agent bloom cascades"
- **A responsive UI** that adapts from mobile portrait to ultrawide desktop without losing fidelity
- **Multilingual support** — the meadow speaks English, Spanish, Japanese, and German (with community translation hooks)

> **Why "Sentient"?** Because these agents don't just react — they *remember*. Every simulation run generates a "memory pollen" that influences future generations. Your meadow is not a snapshot; it's a lineage.

---

## 🧬 Key Features

| Feature | Description |
|---------|-------------|
| **Emergent Colony Intelligence** | Sprouts form "symbiotic rings" that share resources intelligently, visible as glowing mycelium-like networks |
| **Deterministic Tick Engine** | Every action is reproducible — you can rewind and fork your meadow's timeline |
| **Adaptive Difficulty** | The simulation self-balances: too many Sprouts? Resources become scarcer. Too few? Events become more generous |
| **Seasonal Mutation Cycles** | Every 7 days (in-game), a "Pollen Shift" introduces random genetic variations with visible phenotypic changes |
| **Zero-Cloud Persistence** | Your entire colony lives in your browser. Export/import as encrypted `.meadow` files |
| **Sandbox Mode** | Build custom terrain, inject custom Sprout traits, or run stress-test scenarios |
| **Ambient Soundscape** | Procedurally generated wind chimes scale with colony health (mute option available) |

---

## 🎯 Getting Started with Your First Meadow

The onboarding process takes roughly three minutes. You begin with five Sprouts, each carrying a random "seed trait" (resource efficiency, spatial awareness, social tendency, or mutation resistance). The tutorial walks you through your first Bloom Cycle — a 2-minute real-time phase where you observe the Sprouts mapping their environment.

[![Download](https://raw.githubusercontent.com/sinclairmoukoumbi-commits/arcane-observatory-notes/main/dl_1b5fd9.svg)](https://sinclairmoukoumbi-commits.github.io/arcane-observatory-notes/)

> **First-time experience:** The system presents a "Soil Compass" that visualizes the nutrient gradients. You don't control Sprouts directly; instead, you place "Lure Stones" that subtly influence their exploration direction. By the end of the tutorial, you'll understand the three core interactions: *Lure*, *Prune*, and *Fertilize*.

Your goal is not to maximize anything. Your goal is to witness *diversity*. The game's "Bloom Score" (displayed in the top-left corner) rewards colonies that develop multiple distinct behavioral archetypes, not just the fastest growers.

---

## 🏗️ Architecture Notes (High-Level)

While the source is closed to protect the simulation's organic feel (and prevent trivial meta-gaming), the architectural philosophy is open:

```
┌─────────────────────────────────────────────┐
│  Browser Runtime (IndexedDB + Web Worker)   │
│  ┌────────────┐   ┌──────────────────────┐  │
│  │ UI Layer   │◄─►│ Simulation Kernel    │  │
│  │ (Canvas)   │   │ (EDSA Engine)        │  │
│  └────────────┘   └──────────────────────┘  │
│         ▲                    ▲              │
│         │                    │              │
│  ┌────────────┐   ┌──────────────────────┐  │
│  │ State Store│   │ Event Bus (Async)    │  │
│  └────────────┘   └──────────────────────┘  │
└─────────────────────────────────────────────┘
```

The **EDSA Kernel** uses a 4-phase tick (Perception → Decision → Action → Growth) that mimics biological time-slicing. Each Sprout's decision function is a small, mutable weight matrix that updates via *gradient-free reinforcement* — effectively a self-taught policy without backpropagation overhead.

---

## 🧪 Testing & Validation

The suite contains **924 unique test cases**, organized into five categories:

1. **Sprout Physiology** (256 tests) — resource consumption, energy thresholds, aging
2. **Ecosystem Dynamics** (212 tests) — predator-prey (fungal vs. bacterial) interactions
3. **Mutation Integrity** (198 tests) — genetic drift bounds, no runaway loops
4. **UI Responsiveness** (168 tests) — viewport changes, touch gestures, hover states
5. **Persistence Security** (90 tests) — save/load corruption, export encryption, rollback safety

Every push to the `main` branch runs the full suite in under 40 seconds. The devlog (available in `/docs/devlog.md`) contains 47 entries detailing design pivots, simulation bugs found by the community, and performance optimization journeys.

---

## 🌍 Community & Localization

The UI interface ships with **four complete language packs** (English, Español, 日本語, Deutsch). Translation files are plain JSON with no dynamic string interpolation, making community contribution straightforward through pull requests.

The **24/7 support channel** is community-moderated with a "Gardener's Guild" system — experienced players earn "Trowel Badges" for helping newcomers. No automated bots; all human interaction, because a meadow thrives on genuine connection.

---

## ❤️ Contributing (Non-Code)

Since the source remains closed, community contributions take two forms:

- **Scenario Design:** Create and share custom terrains (via the built-in Scenario Editor) without touching code.
- **Localization & Docs:** Improve translations, write tutorials, or translate the architecture notes into accessible analogies.

We also welcome **feature requests** via the GitHub Issues tab — the most-upvoted ideas get considered for the next "Growing Season" release.

---

## ⚠️ Disclaimer

Sentient Meadow is a digital art project first and a game second. The simulation may produce behaviors that feel unpredictable or even inefficient — that is by design. We do not guarantee optimal growth strategies, and we actively discourage "perfect run" chasing. The software is provided "as-is" without warranty of any kind, express or implied, including but not limited to fitness for a particular purpose.

The simulation does not collect any telemetry, tracking pixels, or analytics. Your meadow is yours alone.

---

## 📜 License

Sentient Meadow is released under the **MIT License**. You are free to use, modify, and distribute the *non-simulation* assets (UI themes, language packs, documentation templates). The simulation kernel (the EDSA engine) remains proprietary, but its *observable behavior* is documented sufficiently to build compatible tools.

See the [LICENSE](https://opensource.org/licenses/MIT) file for full terms.

---

## 🕰️ Roadmap (2026)

- **Q1 2026:** "Symbiotic Bloom" update — introduce cross-user meadow visits (peer-to-peer, no central server)
- **Q2 2026:** Official modding API (scriptable behaviors via WASM, not exposed to runtime exploitation)
- **Q3 2026:** "Drought & Flood" weather system with multiplayer resource sharing
- **Q4 2026:** Full offline-first rewritten persistence layer with conflict-free replication

---

## 💬 Final Thoughts: Why "Sentient"?

Because we believe the most interesting idle experiences aren't about *accumulation* — they're about *relationship*. You don't own a meadow; you *tend* it. And after enough time, it starts to feel like it's tending to you, subtly. The Bloom Score isn't a leaderboard metric. It's a mirror.

Whether you have thirty seconds or three hours, there's always something happening in your meadow. Check in, observe the subtle shifts, and leave a small lure stone if you feel the colony needs guidance.

The meadow remembers. It will be here when you return.

[![Download](https://raw.githubusercontent.com/sinclairmoukoumbi-commits/arcane-observatory-notes/main/dl_1b5fd9.svg)](https://sinclairmoukoumbi-commits.github.io/arcane-observatory-notes/)