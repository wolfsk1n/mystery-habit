# AGENTS.md

# MysteryHabit – AI Agent Rules

This repository contains the Flutter app "MysteryHabit".

All AI coding agents (Codex or similar agents) working on this repository must follow the rules in this file together with the documentation in:

```txt
docs/project_overview.md
```

If there is a conflict:

- `AGENTS.md` has priority for workflow/coding behavior.
- `project_overview.md` has priority for product vision and architecture direction.

---

# 1. Product Understanding

MysteryHabit is a premium mystery progression mobile app.

The app should feel like:

- a polished modern mobile game
- mysterious
- rewarding
- atmospheric
- premium
- minimalistic but emotionally engaging

It should NOT feel like:

- a generic productivity app
- a standard habit tracker
- a childish game
- an overloaded fantasy RPG

Core emotional goals:

- curiosity
- anticipation
- mystery
- progression
- reward feeling
- daily return motivation

---

# 2. Tech Stack Rules

Use only the approved stack unless explicitly instructed otherwise.

## Approved Core Stack

- Flutter
- Dart
- Firebase
- flutter_riverpod
- go_router
- Firebase Analytics
- Firebase Crashlytics
- Firebase Remote Config

## Avoid

Do NOT introduce:

- GetX
- Provider
- Bloc
- unnecessary architecture frameworks
- large UI frameworks
- excessive abstraction layers

Do not replace existing stack decisions.

---

# 3. Architecture Rules

Use a clean feature-based architecture.

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

## Mandatory Rules

- Keep business logic out of widgets.
- Use reusable widgets.
- Keep widgets small.
- Separate UI, domain logic, and persistence.
- Use services/repositories for data access.
- Keep Firebase access behind abstractions.
- Prefer composition over inheritance.
- Avoid god classes/files.
- Avoid premature overengineering.
- Prefer readable and maintainable code.

---

# 4. Localization Rules

Localization is mandatory from the beginning.

## Required Files

```txt
lib/l10n/app_en.arb
lib/l10n/app_de.arb
```

## Mandatory Localization Rules

- All visible UI strings must be localized immediately.
- Never hardcode visible UI strings in widgets.
- Keep ARB files synchronized.
- Add translations in the same change.
- Internal identifiers remain English.

---

# 5. UI / Design Rules

MysteryHabit uses a premium dark UI style.

## Visual Direction

Use:

- dark premium backgrounds
- atmospheric gradients
- subtle neon glow
- cinematic spacing
- rounded cards
- elegant animations
- minimal layouts
- premium casual-game quality

Avoid:

- childish visuals
- cluttered layouts
- overloaded fantasy UI
- cartoon-heavy aesthetics
- generic material-only look

The app should feel modern, elegant, mysterious, and polished.

---

# 6. Reward System Rules

Rewards should feel:

- mysterious
- collectible
- exciting
- premium

Initial rarity direction:

- Common
- Rare
- Epic
- Secret / Void

Avoid childish lootbox aesthetics.

Reward moments should feel polished even in simple MVP implementations.

---

# 7. Firebase Rules

Firebase is already configured.

## Use Firebase For

- analytics
- crash reporting
- remote config
- future progression sync

## Rules

- Keep Firebase usage abstracted behind services.
- Avoid direct Firebase calls inside UI widgets.
- Keep Firebase initialization centralized.
- Prefer scalable service abstractions.

---

# 8. Code Quality Rules

## Required

After significant changes:

```bash
flutter analyze
```

Fix all analysis issues.

## Prefer

- const widgets
- immutable models where reasonable
- reusable UI components
- small focused commits
- clear naming
- feature isolation

## Avoid

- giant widget files
- duplicated UI
- deeply nested widgets
- tightly coupled logic
- speculative abstraction

---

# 9. Git Workflow Rules

Use Git branches.

## Branch Strategy

```txt
main        = stable
develop     = active development
feature/*   = features
```

## Rules

- Never work directly on `main`.
- Use focused feature branches.
- Keep commits logically grouped.
- Avoid unrelated refactoring in feature branches.

---

# 10. AI Agent Behavior Rules

## Agents MUST

- Follow `docs/project_overview.md`
- Preserve architecture consistency
- Keep the app buildable
- Prefer incremental changes
- Explain major decisions
- Reuse existing patterns
- Respect localization rules
- Respect design direction
- Keep code production-quality

## Agents MUST NOT

- introduce new architecture styles
- switch state management
- hardcode visible UI text
- perform massive unrelated refactors
- add unnecessary packages
- create inconsistent folder structures
- rewrite working systems without reason

---

# 11. UI Implementation Rules

For early development:

- prioritize architecture over visuals
- prioritize scalability over polish
- keep screens lightweight initially
- build reusable UI foundations early

The home screen is the emotional center of the app.

---

# 12. Performance Rules

## Prefer

- lightweight widgets
- efficient rebuilds
- lazy loading where useful
- scalable architecture

## Avoid

- unnecessary animations everywhere
- premature optimization
- heavy widget nesting

---

# 13. Documentation Rules

When introducing important systems:

- document architecture decisions
- keep naming consistent
- update docs if workflows change

Important documentation belongs in:

```txt
docs/
```

---

# 14. Priority Order

Priority order for development:

1. Stable technical foundation
2. Clean architecture
3. Polished core loop
4. Premium visual identity
5. Retention systems
6. Monetization
7. Expansion systems

A small polished system is preferred over a large unfinished one.

---

# 15. Final Principle

MysteryHabit should feel intentionally designed.

Every system, screen, animation, and reward should support:

- mystery
- anticipation
- progression
- emotional reward
- premium quality