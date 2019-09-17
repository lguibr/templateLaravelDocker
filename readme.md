# TemplateDockerLaravelMySql

simple template to bootstrap projects with laravel framework in docker containers.

### To build the containers

docker-compose up -d

### To edit .env

docker-compose exec app nano .env

DB_HOST will be your db database container.
DB_DATABASE will be the laravel database.
DB_USERNAME will be the username you will use for your database. In this case, we will use laraveluser.
DB_PASSWORD will be the secure password you would like to use for this user account.

### To auto set key for the laravel app

docker-compose exec app php artisan key:generate

### To exec the app

docker-compose exec app php artisan config:cache

#### visit http://your_server_ip

### To exec a terminal on DB container

docker-compose exec db bash

### To acess mysql

mysql -u root -p your_mysql_root_password

### To see databases

show databases;

### To create a user

GRANT ALL ON laravel.\* TO 'laraveluser'@'%' IDENTIFIED BY 'your_laravel_db_password';

FLUSH PRIVILEGES;

EXIT;

exit

### RUN MIGRATIONS

docker-compose exec app php artisan migrate

### ACESS TINKER SQL SHELL HELPER

docker-compose exec app php artisan tinker

Start to play !
