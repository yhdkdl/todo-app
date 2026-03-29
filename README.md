# Todo App

A full-stack todo application with a Django REST API backend and a Flutter mobile frontend.

## Features

- User authentication and registration
- Create, read, update, and delete todos
- Mark todos as completed
- User-specific todo lists
- Cross-platform mobile app (Android, iOS, Web, Desktop)

## Project Structure

```
todo-app/
├── todo_backend/          # Django REST API backend
│   ├── apps/
│   │   ├── authentication/  # User authentication app
│   │   └── todos/          # Todo management app
│   ├── config/            # Django project settings
│   ├── db.sqlite3         # SQLite database
│   ├── manage.py          # Django management script
│   └── requirements.txt   # Python dependencies
├── todo_mobile/           # Flutter mobile application
│   ├── lib/
│   │   ├── core/          # Core utilities and services
│   │   ├── features/
│   │   │   ├── auth/      # Authentication screens and logic
│   │   │   └── todos/     # Todo screens and logic
│   │   └── main.dart      # App entry point
│   ├── pubspec.yaml       # Flutter dependencies
│   └── README.md          # Mobile app specific README
└── README.md              # This file
```

## Backend Setup (Django)

### Prerequisites
- Python 3.8+
- pip

### Installation

1. Navigate to the backend directory:
   ```bash
   cd todo_backend
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run database migrations:
   ```bash
   python manage.py migrate
   ```

5. Create a superuser (optional):
   ```bash
   python manage.py createsuperuser
   ```

6. Start the development server:
   ```bash
   python manage.py runserver
   ```

The API will be available at `http://127.0.0.1:8000/`

### API Endpoints

- `POST /api/auth/login/` - User login
- `POST /api/auth/register/` - User registration
- `GET /api/todos/` - List user's todos
- `POST /api/todos/` - Create a new todo
- `GET /api/todos/{id}/` - Get specific todo
- `PUT /api/todos/{id}/` - Update todo
- `DELETE /api/todos/{id}/` - Delete todo

## Mobile App Setup (Flutter)

### Prerequisites
- Flutter SDK (3.10.7+)
- Dart SDK
- Android Studio / Xcode (for mobile development)

### Installation

1. Navigate to the mobile app directory:
   ```bash
   cd todo_mobile
   ```

2. Install dependencies:
   ```bash
   flutter pub get
   ```

3. Run the app:
   ```bash
   flutter run
   ```

### Supported Platforms

- Android
- iOS
- Web
- Windows
- macOS
- Linux

## Technologies Used

### Backend
- **Django** - Web framework
- **Django REST Framework** - API development
- **SQLite** - Database (can be changed to PostgreSQL/MySQL for production)

### Frontend
- **Flutter** - Cross-platform UI framework
- **Dart** - Programming language

## Development

### Running Tests

Backend:
```bash
cd todo_backend
python manage.py test
```

Mobile:
```bash
cd todo_mobile
flutter test
```

### Building for Production

Backend:
```bash
cd todo_backend
python manage.py collectstatic
```

Mobile:
```bash
cd todo_mobile
flutter build apk  # For Android
flutter build ios  # For iOS
flutter build web  # For Web
```


5. Submit a pull request

## License

This project is licensed under the MIT License.
