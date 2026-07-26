# AnimalShelter Backend

Курсовой проект по дисциплине «Веб-разработка» (ДВФУ, 2024).

AnimalShelter Backend — серверная часть сайта приюта для животных 9Life. Предоставляет API для работы с анкетами животных, пользователями, аутентификацией и личным кабинетом.

## Технологии

- PHP
- Laravel
- Composer
- JWT Authentication
- Docker

## Развёртывание

### Клонирование репозитория

```bash
git clone https://github.com/purpurrya/AnimalShelter_Backend.git
cd AnimalShelter_Backend
```

### Установка зависимостей

```bash
composer install
```

### Настройка окружения

```bash
cp .env.example .env
```

После создания файла `.env` необходимо указать параметры подключения к базе данных.

### Генерация ключей

```bash
php artisan key:generate
php artisan jwt:secret
```

### Миграции

```bash
php artisan migrate
php artisan db:seed
```

## Запуск

### Ручной запуск

```bash
php artisan serve
```

API будет доступно по адресу:

```
http://localhost:8000
```

### Запуск через Docker

```bash
docker build -t animalshelter_backend .
docker run -d -p 8000:80 animalshelter_backend
```

Приложение будет доступно по адресу:

```
http://localhost:8000
```
- управление анкетами животных;
- личный кабинет пользователя;
- сохранение понравившихся животных.
