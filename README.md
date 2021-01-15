# start Docker containers (php, nginx, mysql)
# on first start the php container (Dockerfile) will be built, it might take some time
```docker-compose build```
```docker-compose up -d```

```docker-compose up -d --build```

# enter the php container
```docker-compose run --rm composer require aschemelyun/larametrics```
```docker-compose run --rm npm install```
```docker-compose run --rm artisan migrate```

# db
```docker-compose exec php php /var/www/html/artisan migrate```

## Laravel Install

<a href="https://www.positronx.io/how-to-properly-install-and-use-bootstrap-in-laravel/">Tutorial</a>

```composer create-project laravel/laravel --prefer-dist laravel-bootstrap```

```cd laravel-bootstrap/src```

```docker-compose run --rm composer update```

```docker-compose run --rm composer require laravel/ui```

```docker-compose run --rm artisan ui bootstrap```

```docker-compose run --rm artisan ui bootstrap --auth```

```docker-compose run --rm npm install```

```docker-compose run --rm npm run dev```

```docker-compose run --rm npm run watch```