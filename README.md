# laravel-docker
<snippet>
  <content><![CDATA[
Docker Laravel
Php + Nginx + Mysql (Optional)

Instructions

1. clone project laravel via git repository to this repo
    $ git clone https://github.com/laravel/laravel.git

2. Directory Structure
    laravel
    |
    |---docker-php
    |   |
    |   |---Dockerfile
    |
    |---docker-nginx
    |   |--- Dockerfile
    |   |--- default.conf
    |
    |---mysql(ignored)
    |
    |---docker-compose.yml 

3. Environment from laravel & setting some data
    cp .env.example .env

    DB_CONNECTION=mysql
    DB_HOST=database # mysql service in docker-compose
    DB_PORT=3306 # port from container
    DB_DATABASE=laravel # from environment in docker-compose
    DB_USERNAME=laravel # from environment in docker-compose
    DB_PASSWORD=password # from environment in docker-compose

4. Build Docker & Run
    $ docker-compose up -d --build

5. Composer Install Laravel
    $ docker exec -it laravel_php bash
    $ composer install
    $ php artisan key:generate


Enter the following command to start your containers:
$ docker-compose up -d

To stop them, use this:
$ docker-compose down
]]></content>
  <tabTrigger>readme</tabTrigger>
</snippet>
