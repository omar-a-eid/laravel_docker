# Dockerized Laravel App

This repository contains a Laravel application that has been dockerized for easy deployment and development.

## Prerequisites

Before you begin, ensure you have Docker installed on your machine

## Getting Started

1. Clone the repository:

```bash
git clone https://github.com/omar-a-eid/laravel_docker
cd laravel_docker
```

2. Build the Docker containers:

```bash
docker compose build
```

3. Start the Docker containers:

```bash
docker compose up -d
```

4. Copy the .env.example file to .env:

```bash
docker compose exec app cp .env.example .env
```

5. Install PHP dependencies:

```bash
docker compose exec app composer install
```

6. Install JavaScript dependencies:

```bash
docker compose exec app npm install
```

7. Generate the application key:

```bash
docker compose exec app php artisan key:generate
```

8. Run the database migrations:

```bash
docker compose exec app php artisan migrate
```

9. Visit `http://localhost:8101` in your browser to view the application.
