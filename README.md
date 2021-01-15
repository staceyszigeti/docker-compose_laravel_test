# start Docker containers (php, nginx, mysql)
# on first start the php container (Dockerfile) will be built, it might take some time
docker-compose build 
docker-compose up -d

docker-compose up -d --build

# enter the php container
docker-compose exec php

# db
docker-compose exec php php /var/www/html/artisan migrate
