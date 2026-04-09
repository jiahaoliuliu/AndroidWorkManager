# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This project explores different ways to work with Android WorkManager.

## Build & Test Commands

```bash
# Build
./gradlew assembleDebug
./gradlew assembleRelease

# Unit tests
./gradlew testDebugUnitTest
# Run a single test class
./gradlew testDebugUnitTest --tests "com.jiahaoliuliu.androidworkmanager.ExampleUnitTest"

# Instrumentation tests (requires connected device/emulator)
./gradlew connectedDebugAndroidTest

# Lint
./gradlew lintDebug
./gradlew lintFix
```

## Architecture

Single-module Android app (`app`) with:
- **Jetpack Compose** for all UI (no XML layouts)
- **Material Design 3** theming with dynamic color support (Android 12+)
- **Single Activity** (`MainActivity`) as the entry point
- **Min SDK 24** (Android 7.0), **Target/Compile SDK 36** (Android 15)

### Package Structure

`com.jiahaoliuliu.androidworkmanager`
- `ui/theme/` — Material3 theme, color palette, typography

### Key Configuration

- Dependencies managed via version catalog: `gradle/libs.versions.toml`
- Kotlin 2.0.21, AGP 8.12.1, Compose BOM 2024.09.00
