# flutter-core-clean-mvvm

A flutter core with Clean architecture, MVVM design pattern with Bloc, Get_it, Dio, Hive and intl

## Getting Started

This project is a starting point for a Flutter application

## Packages structure
This project is structured in a way that follows the Clean Architecture principles. The main packages are:

```
lib/
├─ app.dart                   # App-level configuration and setup
├─ main_dev.dart              # Main entry for development builds
├─ core/                      # Shared utilities, dependency injection, network, constants
│  ├─ di/                     # Dependency injection setup (e.g., Get_it)
│  ├─ network/                # Network clients, API configuration (e.g., Dio)
│  └─ utils/                  # Common utility functions and helpers
├─ [features]/                # Modular feature folders (specific for each feature) 
│   ├─ data/                  # Data layer
│   │  ├─ datasources/        # Remote/local data sources
│   │  ├─ models/             # Data models (+ generated files)
│   |  └─ repositories/       # Data repository implementations
│   ├─ domain/                # Domain layer
│   │  ├─ entities/           # Business entities
│   │  ├─ repositories/       # Repository interfaces
│   │  └─ usecases/           # Use case classes
│   └─ presentation/          # Presentation layer
│      ├─ pages/              # UI pages/screens
│      ├─ viewmodels/         # MVVM view models
│      └─ widgets/            # Feature-specific widgets
├─ shared/                    # Shared UI widgets, theme, types
└─ routes/                    # Centralized app routing
```
Here’s a detailed section for your `README.md` describing the package structure and utility, tailored to your repo:

---
### Utility

- **app.dart / main_dev.dart**: Application entry points and configuration.
- **core/**: Houses shared logic for dependency injection, networking, and utilities used across features.
- **features/**: Each feature (meals, favorites, shopping) is self-contained, following Clean Architecture:
    - **data/**: Handles data access, models, and repository implementations.
    - **domain/**: Contains business entities, repository interfaces, and use cases.
    - **presentation/**: Manages UI, view models, and widgets for each feature.
- **shared/**: Provides reusable UI components, theming, and type definitions.
- **routes/**: Centralizes route definitions for navigation.

This structure supports modularity, scalability, and maintainability, following Clean Architecture and MVVM principles for Flutter development.

## Starting the project
1. Clone the repository
   ```bash
   git clone
    ```
2. Navigate to the project directory 
   ```bash
   cd flutter_core_clean_mvvm
   ```
3. Install dependencies
   ```bash
   flutter pub get
   ```
4. For code generation (models, localization, etc.), run:
   ```bash
   flutter pub run build_runner build --delete-conflicting-outputs
   ```
5. Run the app
   ```bash
    flutter run -t lib/main_dev.dart
    ```
