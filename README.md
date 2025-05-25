# 🚀 Laravel 12 + Docker Development Environment

This project provides a complete Laravel 12 development environment using Docker, including:

- PHP 8.4 + Composer
- MySQL 8
- Nginx
- phpMyAdmin
- Environment variable support via `.env` file

---

## 📁 Project Structure
```
laravel-docker/
├── docker/
│ ├── app/ # Dockerfile and PHP config
│ └── nginx/ # Nginx configuration (default.conf)
├── docker-compose.yml
├── .env # Environment variables for Docker services
└── src/ # Laravel application source code
```
---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone {link_reoisitiry}
cd laravel-docker
```

### 2. Create .env file
Create a .env file in the project root (next to docker-compose.yml):

```
DB_DATABASE=laravel
DB_USERNAME=laravel
DB_PASSWORD=secret
```

### 3. Build and start Docker containers
```
docker compose up -d --build
```

### 4. Run database migrations
```
docker exec -it laravel-app php artisan migrate
```

### 🌐 Access Services
| Service     | URL                                            | Notes                                          |
| ----------- | ---------------------------------------------- | ---------------------------------------------- |
| Laravel App | [http://localhost:8000](http://localhost:8000) | Laravel home page                              |
| phpMyAdmin  | [http://localhost:8080](http://localhost:8080) | Login with `laravel / secret` |
