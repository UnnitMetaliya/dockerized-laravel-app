<div align="center">
  <h3 align="center">Dockerized cluster for a laravel project</h3>

  <p align="center">
    Project using Laravel, MySQL, Nginx, and Docker.
    <br />
  </p>
</div>

## How to run the appp

- Clone the repo
- Create .env file for laravel environment from .env.example on src folder - ( ```cp ./src/.env.example ./src/.env```)
- Run command ```docker-compose build``` on your terminal
- Run command ```docker-compose up -d``` on your terminal
- Run command ```docker exec -it php /bin/sh``` on your terminal
- Run command ```composer install``` on your terminal after went into php container on docker
- Run command ```chmod -R 777 storage``` on your terminal after went into php container on docker
- Run command ```php artisan key:generate``` on your terminal after went into php container on docker
- Run command ```php artisan migrate:fresh --seed```
- Go to http://localhost:8001 or any port you set to open laravel

## Login and Register

- Run command ```docker exec -it php /bin/sh``` on your terminal
- Run command ```php artisan breeze:install``` on your terminal after going into php container on docker through previous command
- Run command ```php artisan migrate```
- Run command ```npm install``
- On your browser, go to ```localhost:8001/register``` (or click register) for registration page and go to ```localhost:8001/login``` (or click login) for login page


## Some troubleshooting commands

- while in php container, you may run ```php artisan config:cache``` or ```php artisan route:clear``` or ```php artisan optimize``` as debugging commands if you are facing some issues.

**Note: if you got a permission error when running docker, try running it as an admin or use sudo in linux**
