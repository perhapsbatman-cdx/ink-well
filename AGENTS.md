# AGENTS.md

## Project
Ink Well (Android writing app)

## Product Goal
Build an Android writing app inspired by Scrivener-style workflows for long-form writing, chapter organization, and project-based drafting. Deliver incrementally with MVP-first scope control.

## Current Repository Context
- Repo name: `ink-well`
- Local directory: `~/ink-well-app`
- Package: `com.inkwell.app`
- Baseline scaffold exists and runs locally in Android Studio
- Kotlin + Jetpack Compose configured
- Android 10+ support required (minSdk 26)

## Delivery Strategy
Do NOT build full product scope at once.
Implement in small, testable milestones using focused branches and PRs.

### Scope Roadmap
#### MVP-1
- 3-pane workspace shell:
  - Left: Outline
  - Center: Editor
  - Right: Notes
- Adjustable/collapsible side panes
- Distraction-free editor-only toggle
- Adaptive UI for small screens (tab/segmented fallback)
- Local persistence foundation (Room entities/repo in follow-up task)
- Autosave behavior planned and added incrementally

#### MVP-2
- Writing mode timer (standard mode first)
- Rich text-lite formatting actions:
  - bold/italic/underline/strikethrough
  - heading model (Title/H1-H4) in state
- Keyboard-shortcut support where available

#### MVP-3
- Sprint mode
- Import/export first wave: `.txt` and markdown
- Notes/document linkage refinement

#### Later
- Additional import/export (`.docx`, `.pdf`, `.rtf`, `.epub`, `.html`, `.scriv` if feasible)
- Google Drive sync
- Templates
- E-ink Lite Mode optimization
- Editing mode differentiation

## Technical Stack
- Kotlin
- Jetpack Compose
- MVVM
- Room
- DataStore
- WorkManager (for future sync/background jobs)

## Engineering Rules
1. Keep PRs small and single-purpose.
2. Do not introduce speculative abstractions.
3. Prefer beginner-readable, maintainable code.
4. Preserve app stability and current behavior unless task requires change.
5. Add/update tests when data logic changes.
6. Include manual verification steps in PR notes.
7. Update README “MVP Progress” when features land.

## Codex Cloud Environment Constraint (Critical)
This is an Android app. Codex cloud environments may not have Android SDK configured.
Therefore, in Codex cloud:
- Do NOT run Android compile/build commands:
  - `gradle build`
  - `./gradlew build`
  - `./gradlew assembleDebug`
- Do NOT fail task completion solely due to missing Android SDK in cloud.
- Perform code changes only, then provide local verification steps.

Android build verification is performed locally by user in Android Studio / local CLI.

##
