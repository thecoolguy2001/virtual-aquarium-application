# Virtual Aquarium (cw05)

Virtual Aquarium is a cross-platform Flutter application that simulates a lightweight, interactive aquarium where users can create, animate, and manage fish in real time. The project combines playful UI interactions with local persistence to demonstrate practical app architecture concepts in Flutter, including stateful animation, collision behavior, and on-device data storage.

## Project Overview

This application provides a visual aquarium canvas where fish move continuously, respond to optional collision logic, and can be customized through user-controlled settings.

At its core, the app is designed as a compact showcase of:
- **Animation and rendering** with Flutter widgets (`Stack`, `Positioned`, and `AnimatedContainer`).
- **Interactive controls** for fish creation, speed tuning, and color selection.
- **Behavior simulation** via randomized movement and collision-triggered reactions.
- **Persistence with SQLite** (`sqflite`) to retain key aquarium settings between sessions.

## Key Features

- **Live Aquarium Simulation**  
  Fish are animated inside a bounded aquarium area and continuously update their positions.

- **Configurable Fish Properties**  
  Users can define fish color and speed before adding fish to the aquarium.

- **Collision Toggle**  
  A runtime switch enables or disables fish collision behavior. When enabled, close-proximity fish react by changing direction and color.

- **Save and Restore Settings**  
  The current fish count, selected speed, and selected color can be persisted to a local SQLite database and restored on launch.

- **Cross-Platform Flutter Base**  
  The repository includes platform scaffolding for Android, iOS, Web, Linux, macOS, and Windows.

## Technology Stack

- **Framework:** Flutter (Dart)
- **State Model:** Stateful widget lifecycle + animation controller updates
- **Database:** SQLite via `sqflite`
- **Path Utilities:** `path`
- **UI:** Material Design components

## Architecture Notes

The app follows a straightforward single-screen architecture with:
- A `Fish` model class for per-entity simulation state.
- A `StatefulWidget` home screen managing UI controls and simulation lifecycle.
- An `AnimationController` driving periodic position updates.
- A persistence layer embedded in screen state methods for saving/loading configuration data.

This structure keeps the project approachable while still demonstrating production-relevant concepts such as lifecycle management, asynchronous storage operations, and user-driven state mutation.

## Running the Project

1. Install Flutter SDK and verify setup:
   ```bash
   flutter doctor
   ```
2. Install dependencies:
   ```bash
   flutter pub get
   ```
3. Run on your selected platform:
   ```bash
   flutter run
   ```

## Future Enhancements

Potential next steps to evolve this project into a richer simulation include:
- Direction vectors and smoother motion physics.
- Variable fish sizes and species traits.
- Dedicated settings/history screens.
- Improved persistence model with per-fish state storage.
- Refactoring into layered architecture (state management + repository abstraction).

---

Virtual Aquarium is ideal as both a teaching reference and a foundation for expanding into a more advanced simulation or game-oriented Flutter experience.
