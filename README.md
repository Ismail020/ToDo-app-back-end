# ToDo app back-end

## Setup for local development

### First time setup

❗️ Make sure to have the [back-end](https://github.com/Ismail020/ToDo-app-front-end) up and running before running the front-end ❗️

Clone the repository to your device and cd into it
``` bash 
git clone https://github.com/Ismail020/ToDo-app-back-end.git && cd "$(basename "$_" .git)"
```

Copy the .env.example and change the copied file name to .env
```bash
cp .env.example .env
```

Install composer packages with
```bash
composer install
```

Generate an app key (dont use on production or staging)
```bash
php artisan key:generate
```

Add a local database matching DB_DATABASE in .env — default: 'laravel_api'
```bash
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel_api
DB_USERNAME=root
DB_PASSWORD=
```

Migrate and seed the tables to your database
```bash
php artisan migrate:fresh --seed
```

Start environment
```bash
php artisan serve
```
