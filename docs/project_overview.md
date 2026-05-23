# MysteryHabit – Project Overview

## 1. Product Vision

MysteryHabit is a premium mystery progression mobile app.

The app gives users small daily mystery-based challenges, hidden unlocks, reward boxes, riddles, and progression moments. It should feel like a polished mobile game, while remaining a lightweight lifestyle / entertainment app.

The core emotional goals are:

- curiosity
- mystery
- anticipation
- reward feeling
- daily return motivation
- subtle progression

MysteryHabit should not feel like a standard habit tracker. It should feel like opening a small daily secret.

---

## 2. Core App Idea

Each day, the user receives a small mysterious challenge.

Examples:

- Take a photo of something blue.
- Walk a small number of steps.
- Drink a glass of water.
- Find something round.
- Solve a small riddle.
- Complete a tiny real-world task.

After completion, the user receives a small reward moment, such as:

- mystery box opening
- hidden item unlock
- streak progression
- visual reward
- lore fragment
- rarity reveal
- cosmetic progression

The app should create a loop of:

Challenge → Completion → Mystery Reward → Progression → Come back tomorrow.

---

## 3. Target Experience

The user should feel:

- “What will I get today?”
- “What is inside the box?”
- “What happens if I keep going?”
- “I want to keep my streak.”
- “This feels premium and slightly magical.”

The experience should be simple, fast, and emotionally rewarding.

---

## 4. Visual Direction

MysteryHabit uses a premium dark mobile UI.

Design keywords:

- dark premium UI
- atmospheric gradients
- subtle neon glow
- cinematic lighting
- magical mystery atmosphere
- elegant materials
- clean mobile game quality
- minimal but rewarding
- modern casual game aesthetic

Avoid:

- childish treasure chests
- pirate themes
- overloaded fantasy RPG design
- cartoon-heavy visuals
- cluttered UI
- generic habit tracker look

---

## 5. Core MVP Features

The MVP should focus on a small but polished loop.

MVP scope:

- daily mystery challenge
- challenge completion state
- streak counter
- mystery reward box
- simple reward reveal
- basic progression
- home screen
- reward history / collection preview
- local persistence
- basic settings
- localization in German and English

The MVP should be technically clean, visually attractive, and expandable.

---

## 6. Planned Future Features

Potential later features:

- rarity system: common, rare, epic, secret / void
- reward collection
- hidden lore fragments
- premium reward boxes
- seasonal events
- challenge categories
- user profile progression
- cosmetic unlocks
- achievements
- Firebase-backed progression sync
- Remote Config controlled experiments
- rewarded ads
- premium subscription or one-time unlock
- push notifications
- onboarding
- analytics-based balancing

Do not implement future features before the MVP foundation is stable.

---

## 7. Technology Stack

The app is built with Flutter.

Preferred stack:

- Flutter
- Dart
- Firebase
- Riverpod for state management
- go_router for navigation
- Firebase Analytics
- Firebase Crashlytics
- Firebase Remote Config
- local persistence for offline-first MVP data
- ARB localization files for German and English

Avoid introducing alternative state management solutions unless explicitly requested.

Do not use GetX.

---

## 8. Architecture Principles

Use a clean, feature-based architecture.

Preferred structure:

```txt
lib/
 ├── app/
 ├── core/
 ├── features/
 ├── navigation/
 ├── services/
 ├── shared/
 ├── theme/
 └── main.dart

## 8. Architecture Principles

Use a clean, feature-based architecture.

Preferred structure:

```txt
lib/
 ├── app/
 ├── core/
 ├── features/
 ├── navigation/
 ├── services/
 ├── shared/
 ├── theme/
 └── main.dart
```

### General Rules

- Keep business logic out of widgets.
- Use small reusable widgets.
- Use services and repositories for data access.
- Keep Firebase usage behind service abstractions.
- Keep UI, domain logic, and persistence separated.
- Prefer readable code over overly abstract code.
- Avoid large files.
- Avoid premature complexity, but keep the app expandable.

---

## 9. Localization Rules

All user-facing UI strings must be localized immediately.

Required files:

```txt
lib/l10n/app_en.arb
lib/l10n/app_de.arb
```

### Rules

- Keep English and German ARB files in sync.
- Do not hardcode visible UI strings in widgets.
- New UI text must be added to both localization files in the same change.
- Internal enum names and technical identifiers stay in English.

---

## 10. Design System Rules

The app should have a consistent theme system from the beginning.

### Use

- dark color palette
- premium gradients
- subtle glow effects
- rounded cards
- cinematic spacing
- consistent typography
- reusable buttons
- reusable cards
- reusable reward box widgets

UI should be attractive but not over-engineered.

The home screen is the emotional center of the app.

---

## 11. Reward System Direction

Rewards should feel mysterious and collectible.

Initial rarity direction:

- Common
- Rare
- Epic
- Secret / Void

Rewards should be visually differentiated but not childish.

Reward reveal moments should feel polished even if technically simple in the MVP.

---

## 12. Development Workflow

Use Git branches.

Recommended branch structure:

```txt
main        = stable version
develop     = active development
feature/*   = individual features
```

### Rules for Larger Changes

- Create a feature branch.
- Keep commits focused.
- Run analysis/tests before merging.
- Avoid unrelated refactoring in feature branches.

---

## 13. AI / Codex Working Rules

When working with Codex or another AI coding agent:

- Follow this project overview.
- Do not change architecture without explicit instruction.
- Do not introduce new major packages without explaining why.
- Do not mix state management approaches.
- Do not hardcode UI strings.
- Do not place business logic directly inside widgets.
- Prefer incremental, testable changes.
- Keep the app buildable after every step.
- Run `flutter analyze` after significant code changes.
- Add or update tests where useful.

---

## 14. Product Priorities

Priority order:

1. Stable technical foundation
2. Polished core loop
3. Premium visual identity
4. Retention mechanics
5. Monetization
6. Expansion systems

The first release should feel small but high-quality.

A limited polished app is better than a broad unfinished app.