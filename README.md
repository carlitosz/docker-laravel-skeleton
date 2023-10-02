# Docker-Laravel Skeleton

This application contains the boilerplate configuration to start a docker-larvel-php-mysql application.

The configuration creates multiple services:

-   Server (nginx)
-   PHP (version 8.3)
-   Composer (util)
-   Artisan (util)
-   Npm (util)

## Getting started

Create a new `/src` directory at the root of the project.

The docker-composer.yml file contains the configuration for setting up this docker application. It will work as-is, but update to fit your needs.

#### Build

Build the initial image with nginx, php, and mysql.

```
docker compose up -d --build server
```

#### Install

Create and install a new Laravel project in the `/src` directory.

```
docker compose run --rm composer create-project laravel/laravel .
```

#### Development

Visit http://localhost:8000 to see the Laravel project.

#### MySQL

Finally, update Laravel's .env file located in `/src/.env` and update the following environment variables:

```
DB_HOST=mysql
DB_DATABASE=<value from your root .env>
DB_USERNAME=<value from your root .env>
DB_PASSWORD=<value from your root .env>
```

Then, run the migrations that will create some defaults.

```
docker compose run --rm artisan migrate
```
