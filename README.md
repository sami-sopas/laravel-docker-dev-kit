# Laravel Docker Dev Kit

This is a simple docker development kit for Laravel projects. It includes a Nginx web server, PHP, and MySql.

# Requirements

- Docker (lol)

# How to use it

## First time setup

- `git clone https://github.com/sami-sopas/laravel-docker-dev-kit.git`
- `docker compose up -d --build`
- `docker compose exec phpmyadmin chmod 777 /sessions`
- `docker compose exec php bash`
- `chown -R www-data:www-data /var/www/storage /var/www/bootstrap/cache`
- `chmod -R 775 /var/www/storage /var/www/bootstrap/cache`
- `composer setup`
- `npm install`

## Second time onwards

- `docker compose up -d`


