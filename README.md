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

# Notes

## App

- **URL:** http://localhost:8080

## MySql

- **Server:** db
- **Port:** 3306
- **Username:** Depends on .env file
- **Password:** Depends on .env file
- **Database:** Depends on .env file

# Basic docker commands

- `docker compose up -d` - Create and start the containers
- `docker compose build` - Build or rebuild services
- `docker compose down` - Stop and remove containers and networks (Data is preserved)
- `docker compose stop` - Stop all services
- `docker compose restart` - Restart containers
- `docker compose exec <container> <command>` - Run a command in a specific container

# Common commands in development

- **Access the App container:** Here you can run php artisan, composer, npm, git etc. 
  - `docker compose exec php bash` 

- **Access the MySql container:** Here you can run mysql commands.
  - `docker compose exec db bash`
  - `mysql -u <username> -p <password>`