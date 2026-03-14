# Todo App - Mobile

A Flutter mobile application for managing personal todos with user authentication.

## Features

- User login and registration
- View, create, edit, and delete todos
- Mark todos as completed
- Clean, intuitive user interface
- Cross-platform support

## Getting Started

### Prerequisites

- Flutter SDK (3.10.7+)
- Dart SDK
- Android Studio / Xcode for mobile development

### Installation

1. Ensure Flutter is installed and configured:
   ```bash
   flutter doctor
   ```

2. Install dependencies:
   ```bash
   flutter pub get
   ```

3. Run the app:
   ```bash
   flutter run
   ```

### Building

For Android APK:
```bash
flutter build apk --release
```

For iOS (on macOS):
```bash
flutter build ios --release
```

For Web:
```bash
flutter build web --release
```

## Project Structure

```
lib/
├── main.dart              # App entry point
├── core/                  # Core utilities, services, and models
├── features/
│   ├── auth/              # Authentication screens and logic
│   │   ├── screens/       # Login, register, splash screens
│   │   └── ...            # Auth-related widgets and providers
│   └── todos/             # Todo management
│       ├── screens/       # Todo list, create/edit screens
│       └── ...            # Todo-related widgets and providers
```

## Backend Integration

This app connects to a Django REST API backend. Make sure the backend is running and update the API base URL in the configuration if needed.

## Supported Platforms

- Android
- iOS
- Web
- Windows
- macOS
- Linux

## Dependencies

Key packages used:
- `http` - For API calls
- `provider` - State management
- `shared_preferences` - Local data storage

See `pubspec.yaml` for the complete list of dependencies.

## Contributing

1. Follow Flutter best practices
2. Test on multiple platforms
3. Ensure code is properly formatted: `flutter format .`
4. Run tests: `flutter test`

## Resources

- [Flutter Documentation](https://docs.flutter.dev/)
- [Dart Documentation](https://dart.dev/)
- [Flutter Cookbook](https://docs.flutter.dev/cookbook)
