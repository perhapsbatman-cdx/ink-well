# AGENTS.md

## Product goal
Build "Ink Well": an Android word processor for long-form writing with fast typing performance and reliable offline autosave.

## Tech stack
- Kotlin
- Jetpack Compose
- MVVM
- Room (documents/local persistence)
- DataStore (settings)
- WorkManager (background tasks)

## Working rules
- Keep PRs and commits small and focused.
- Do not introduce unnecessary dependencies.
- Preserve editor stability and typing responsiveness.
- Prefer clear, maintainable code.
- Add or update tests when business logic changes.

## Build & test expectations
- Project should sync and build in Android Studio.
- Command-line build target: `./gradlew assembleDebug`
- Unit tests target: `./gradlew test`

## Definition of done (default)
- Code compiles.
- No obvious regression in document open/save/editor behavior.
- Relevant tests added/updated.
- README updated when behavior changes.

## Initial feature priorities
1. Document list screen
2. Editor screen
3. Local save/load
4. Autosave
5. Export `.txt` then `.pdf`
