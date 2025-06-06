# KittyGram

## Описание приложения
KittyGram — это социальная платформа для любителей кошек, позволяющая авторизованным пользователям публиковать фотографии своих питомцев. Приложение предоставляет закрытое сообщество, где все материалы доступны только после регистрации и входа в систему.

Основные функции:
- Защищённая авторизация пользователей
- Загрузка и хранение фотографий котиков
- Просмотр ленты публикаций
- Управление собственными постами

## Необходимые инструменты
Для запуска проекта потребуется:
- Docker (версия 20.10.0 или выше)
- Docker Compose (версия 1.29.0 или выше)
- Python 3.8+
- Node.js 14+ (для фронтенд-сборки)

## Установка и запуск

### 1. Клонирование репозитория
```bash
git clone https://github.com/bobgoz/kittygram.git
cd kittygram
```

### 2. Настройка окружения
Создайте файл .env в корне проекта:
```
POSTGRES_DB=kittygram
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=your_secure_password
SECRET_KEY=your_django_secret_key
DEBUG=False
ALLOWED_HOSTS=kittygram-bobgoz.duckdns.org,localhost
```

### 3. Запуск контейнеров
```
docker-compose -f docker-compose.production.yml up --build -d
```

### 4. Применение миграций
```
docker-compose exec backend python manage.py migrate
```

### 5. Сборка статики

