# Objective

This script is intended for finding the hidden treasure,
A scraping challenge by digikala for 2021 black Friday


# Prerequisites

* Php
* mysql
* redis

# How to install

after cloning, in the project base dir run:

```
composer install
cp ./.env.example ./.env
```

fill the required fields in the `.env` file, like:
```
DB_DATABASE=digikala_scrap
DB_USERNAME=root
DB_PASSWORD=
QUEUE_CONNECTION=redis
```
create the database accordingly & provide redis password if its needed any.
then, migrate the tables:
```
php artisan migrate
```

# How to run
go to the treaseure hunting page, and find the **page counts**. (it was always 47)

you can run the project using this command:

```
php artisan scrap:digikala 47 && php artisan horizon

```

you can see the running queue, if you want that, you have to serve the http kernel using:
```
php artisan serve

```
then visit the horizon dashboard page (usually served under localhost:8000 ) :
```
localhost:8000/horizon
```
