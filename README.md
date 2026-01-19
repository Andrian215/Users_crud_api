# Users CRUD API (FastAPI + MySQL)

Простий бекенд на FastAPI з MySQL для роботи з користувачами (CRUD).

## Опис
- Створення, перегляд та видалення користувачів
- Автоматична документація Swagger UI (`/docs`) та Redoc (`/redoc`)
- Підключення до MySQL через SQLAlchemy
- Використання `.env` для безпечного зберігання пароля

## Структура проєкту
main.py # FastAPI додаток
database.py # Підключення до MySQL
models.py # Моделі SQLAlchemy
schemas.py # Pydantic-схеми
.env # Пароль та налаштування БД (ігнорується Git)
.gitignore
requirements.txt


## Запуск
1. Створити `.env` з параметрами БД:
DB_USER=root
DB_PASSWORD=твій_пароль
DB_HOST=localhost
DB_NAME=fastapi_db
2. Встановити залежності:
pip install -r requirements.txt
3. Запустити сервер:
python -m uvicorn main:app --reload
- Сервер: [http://127.0.0.1:8000](http://127.0.0.1:8000)  
- Swagger UI: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

## Ендпоінти
- POST `/users` → створити користувача  
- GET `/users` → список користувачів  
- GET `/users/{id}` → отримати користувача  
- DELETE `/users/{id}` → видалити користувача  
- GET `/` → домашнє повідомлення
