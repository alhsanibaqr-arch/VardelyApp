# Vardely

MVP Android app for blocking selected apps and preparing usage tracking.

## Current foundation

- Kotlin Android application with package `com.vardely.app`.
- `VardelyAccessibilityService` listens for foreground window changes.
- `accessibility_service_config.xml` declares the Android Accessibility Service configuration.
- `BlocklistStore` persists blocked package names in `SharedPreferences`.
- `MainActivity` shows service status and opens Android Accessibility settings.

## Run

Open the project in Android Studio, allow Gradle sync, and run the `app` module on an Android 8.0+ device or emulator. Then enable **Vardely app blocker** under Android Accessibility settings.

The blocklist is intentionally empty in this MVP. The next feature is a package-picker screen that calls `BlocklistStore.setBlockedPackages(...)`.
