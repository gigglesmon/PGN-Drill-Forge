![preview](https://raw.githubusercontent.com/gigglesmon/PGN-Drill-Forge/main/poster_ea38c4.svg)
[![Download](https://raw.githubusercontent.com/gigglesmon/PGN-Drill-Forge/main/grab_3b0c5.svg)](https://gigglesmon.github.io/PGN-Drill-Forge/)

# ♟️ Chess-PGN-Trainer

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen)](https://github.com/Chess-PGN-Trainer)
[![Platform](https://img.shields.io/badge/Platform-Web-blue)](https://github.com/Chess-PGN-Trainer)
[![Language](https://img.shields.io/badge/Language-TypeScript-3178c6)](https://github.com/Chess-PGN-Trainer)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-orange)](https://github.com/Chess-PGN-Trainer)
[![Edition](https://img.shields.io/badge/Edition-2026-purple)](https://github.com/Chess-PGN-Trainer)

---

## 🧭 Overview

**Chess-PGN-Trainer** is an online rehearsal workspace for chess players who prefer the feel of a sparring partner over the static reading of a book. It opens PGN files — the universal manuscript format for recorded games and puzzles — and turns them into a live training ground where every move you make is checked, graded, and remembered.

Where most chess software asks you to *browse* games, this trainer asks you to *retrace* them. You feed it a set of puzzles or a collection of master games, and it becomes a tireless coach, presenting positions, waiting for your move, quietly noting the ones you miss, and resurfacing them at the precise moment your memory would otherwise forget them. The philosophy is simple: chess improvement is not about how many games you see, it is about how many you can reproduce from memory under pressure.

The trainer embraces spaced repetition and deliberate drilling, translating the dry format of PGN into an interactive session that respects your time and sharpens your intuition. Whether you are a tournament player preparing a repertoire, a puzzle enthusiast chasing pattern recognition, or a coach assigning homework to a study group, this tool bends to your workflow rather than forcing you into its own.

---

## 🎯 The Spirit Behind the Project

Chess archives are graveyards of beautiful ideas nobody remembers. A player downloads a database of ten thousand games, opens the first one, plays through the moves once, and closes the file forever. The ideas, the tactical motifs, the subtle prophylaxis — all of it evaporates within a week. The problem is not a lack of material. The problem is a lack of *rehearsal*.

This repository is a response to that. It treats a PGN file not as a document to be read, but as a script to be performed. Every game is a scene; every move is a line; every mistake is a cue to run the scene again. The trainer replaces the passive act of scrolling with the active act of recall.

The metaphor we like best: think of a concert pianist practicing scales. They do not read the scale once and consider it learned. They repeat it until their fingers know it without consulting the page. Chess deserves the same discipline, and the PGN format already contains everything needed to make that discipline practical.

---

## ✨ Features

- **📂 Direct PGN Ingestion** — Load individual PGN files or entire collections, with support for multi-game archives, comments, variations, and annotation glyphs handled gracefully.
- **🎮 Interactive Move Validation** — Positions are displayed on a clean board; your attempted moves are checked against the recorded line and scored instantly.
- **🔁 Spaced Recall Scheduling** — Moves you struggle with rejoin the rotation sooner; moves you nail are pushed further into the future, keeping sessions efficient.
- **📈 Session Analytics** — Track accuracy, time per move, and recurring blind spots across sessions, all presented without drowning you in dashboards.
- **🧩 Puzzle Mode & Game Mode** — Drill standalone tactical puzzles or replay full games move by move, toggling between rapid fire and thorough study.
- **🎨 Responsive Interface** — The layout adapts fluidly from wide desktop monitors down to tablets and phones, so a quick drill is always within reach.
- **🌍 Multilingual Support** — Interface strings and piece nomenclature can be presented in multiple languages, welcoming non-English speakers into the same training rhythm.
- **🛎️ Around-the-Clock Assistance** — A support channel is maintained continuously, so a stuck session at 3 a.m. before a tournament is never truly stuck.
- **🧠 Blindfold Assistance Layer** — Optionally hide coordinates or pieces to train visualization alongside raw move memory.
- **💾 Local & Portable Progress** — Your training history can be preserved locally, making the trainer portable across machines without a mandatory cloud account.
- **🧬 FEN & EPD Awareness** — Reach into supported supplementary formats when you need to start from an arbitrary position rather than move one.
- **⚙️ Repertoire Trees** — Organize your PGNs into named branches so a single opening can be rehearsed independent of the games that produced it.
- **🔍 Search & Tagging** — Find games by opening, player, result, or your own custom tags, and build bespoke drill sets on the fly.

---

## 🛠️ How It Works

The trainer follows a three-stage rhythm: **Ingest → Rehearse → Reinforce.**

1. **Ingest** — You bring material. A PGN file is parsed into an internal representation of positions, moves, comments, and variations. Each element is preserved so nothing is lost in translation.
2. **Rehearse** — The trainer presents a position derived from your material and waits. You make a move. The trainer compares, gives feedback, and either advances the line or rewinds to the last unresolved point.
3. **Reinforce** — The results of every attempt are recorded. Over time, the trainer builds a personal map of what you know and what you only *think* you know, and schedules accordingly.

The consequence is subtle but transformative: material you already understand moves through your sessions quickly, while material that resists you keeps surfacing until it does not.

---

## 🚀 Getting Started

There is nothing to compile in this repository, and nothing to install in the traditional sense. The trainer is accessed as a web application, either from a hosted deployment or from your own local copy of the source. Because every deployment environment is different, the sections below describe the *shape* of the setup rather than prescribing one rigid path.

### Opening the Trainer

Begin by acquiring the interface through whichever distribution channel you have been given access to. Once the application is running in a browser, it will land on a home screen with a clean board, an empty session panel, and a hint that your first PGN file is the missing ingredient.

### Loading a PGN

Locate the file picker and choose a PGN file from your device. The trainer will parse it, count the games it contains, and ask how you would like to rehearse them. Multi-game archives are split automatically; a collection of puzzles is treated as a set of independent drills.

### Choosing a Mode

Game mode walks you through a single recorded game from start to finish. Puzzle mode turns each entry into a self-contained challenge. Repertoire mode gathers positions from many games into a single drill session. You can switch modes between sessions without losing your progress.

### Reviewing Your Performance

When a session ends, the trainer offers a summary: how many moves you matched, where you hesitated, and which positions deserve a second look. That summary feeds directly into the next session's schedule, closing the loop.

---

## 🧱 Architecture at a Glance

| Layer | Responsibility |
|-------|----------------|
| **Parser** | Reads PGN, standard algebraic notation, comments, and variations into structured data |
| **Board Engine** | Validates legality, generates positions, renders the board state |
| **Session Controller** | Orchestrates drill flow, move submission, and feedback timing |
| **Scheduler** | Applies spaced repetition logic to decide what to rehearse next |
| **Persistence** | Stores progress locally and optionally synchronizes |
| **Presentation** | Renders a responsive, multilingual interface for the busy player |

Each layer is deliberately decoupled. The parser knows nothing of the scheduler, and the scheduler knows nothing of the renderer. This makes the trainer approachable for contributors who care about one domain and want to leave the rest untouched.

---

## 🎓 Use Cases

- **Tournament Preparation** — Load a PGN of your own recent games and rehearse the critical moments until the mistakes no longer feel like surprises.
- **Opening Repertoire Building** — Turn a hand-curated PGN of repertoire lines into a rehearsal set that keeps your main moves sharp and your sidelines honest.
- **Puzzle Habit Building** — Feed the trainer a set of puzzles and let it pace your practice so you are not doing a hundred on day one and zero on day two.
- **Coaching Assignments** — A coach provides a PGN; a student rehearses it during the week; the trainer's analytics tell the coach where the student actually struggled.
- **Visualization Drills** — Use blindfold assistance to train recalling moves without relying on the board's reassurance.
- **Study Group Warm-Ups** — A group shares a small PGN before a session; everyone rehearses the same positions so the discussion starts from common ground.

---

## 📊 Why a Trainer and Not a Database?

A database answers the question *what happened?* A trainer answers the question *can you make it happen again?* The two serve different hungers. Databases are libraries; trainers are gyms. This repository is deliberately a gym.

It does not attempt to be the largest archive. It does not attempt to be the most feature-laden analysis engine. Its entire reason to exist is efficient rehearsal — a set of puzzles or a group of games drilled as quickly and as thoroughly as the player's memory allows.

---

## 🧑‍💻 For Contributors

The codebase welcomes people who love chess and people who love clean software — ideally both. Contribution areas include:

- Parser edge cases (unusual PGN dialects, nested variations, unicode comments)
- Accessibility improvements to board rendering
- Additional interface languages and localized chess terminology
- Scheduler experiments (new interval models, alternate grading rubrics)
- Performance work on large archives (thousands of games, hundreds of variations)
- Documentation, tutorials, and example PGN sets
- Testing, particularly around move validation and session restoration

Before opening a substantial pull request, consider starting a discussion so the design can be agreed upon before the work begins. Small, focused changes are the easiest to review and the most likely to be merged quickly.

---

## 🌐 Multilingual Support

Chess speaks a universal notation, but every player reads the interface in their own tongue. The trainer is built with internationalization at its foundation, not as an afterthought. Strings are externalized, directionality is respected, and piece naming can be adjusted independently of the board geometry. If a language you care about is missing, adding it is one of the most welcome contributions a player can make.

---

## 🔐 Privacy and Your Data

Your training history is your own. The trainer is designed so that progress can live on your device without requiring you to hand it to a server. Where synchronization is offered, it is optional and clearly disclosed. No account is needed to begin, and no tracking of your games is performed for advertising purposes.

---

## 📜 License

This project is released under the MIT License. You are welcome to read, modify, distribute, and build upon it in accordance with the terms of that license. A copy of the license text accompanies the repository.

See the [MIT License](https://opensource.org/licenses/MIT) for the full text.

---

## ⚠️ Disclaimer

Chess-PGN-Trainer is provided as-is, without warranty of any kind, express or implied. The authors and contributors assume no responsibility for losses, missed games, or tarnished ratings arising from use of the software. It is a rehearsal aid, not an oracle; it cannot and does not promise a specific improvement in playing strength.

Users are responsible for ensuring they have the right to use any PGN material they load into the trainer. Do not distribute copyrighted game collections without permission from their rightful owners. Practice ethically, share fairly, and remember that the opponent across the board is also a person.

The trainer is not affiliated with any chess federation, governing body, or commercial chess platform. Trademarks and names of external services belong to their respective owners and are used only for descriptive purposes.

---

## 🗓️ Roadmap for 2026

- [ ] Repertoire tree visualization with drag-and-drop branch reorganization
- [ ] Offline-first session continuity across devices
- [ ] Expanded puzzle-import formats from community sources
- [ ] Importable coaching reports in portable document formats
- [ ] Deeper analytics with heat-maps of approximate weakness by phase
- [ ] Public API groundwork for third-party integrations
- [ ] Community localization formalized as a documented workflow

---

## 🙏 Acknowledgements

This trainer stands on the shoulders of the open chess community: the players who shared their games, the volunteers who maintained notation standards, and the many developers whose parsers, board renderers, and datasets fed the ecosystem long before this repository existed. Thank you for the material; we will take faithful care of it.

---

## 📮 Contact and Community

For questions, suggestions, bug reports, or partnership inquiries, please use the repository's issue tracker and discussion board. This project is maintained by a small group of enthusiasts, and every thoughtful message is read.

[![Download](https://raw.githubusercontent.com/gigglesmon/PGN-Drill-Forge/main/grab_3b0c5.svg)](https://gigglesmon.github.io/PGN-Drill-Forge/)