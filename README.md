# Docker-Laravel Skeleton

This application contains the boilerplate configuration to start a docker-larvel-php-mysql application.

The configuration creates multiple services:

-   Server (nginx)
-   PHP (version 8.3)
-   Composer (util)
-   Artisan (util)
-   Npm (util)

## Getting started

#### Start the server

To start the server, php, and mysql:

```
docker compose up -d --build server
```

#### Create Laravel app

Create a new `/src` directory at the root and run

```
docker compose run --rm composer create-project laravel/laravel .
```

#### Run db migrations

```
docker compose run --rm artisan migrate
```
