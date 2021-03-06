### Recert

- Built on laravel ```v5.1.*```

##### Installation
- change .env file for mysql credentials

Run below commands before running Server

```shell
> composer install
> composer dump-autoload
> php artisan optimize
> php artisan migrate
> php artisan db:seed
> php artisan route:cache
> php artisan config:cache
```

#### Development

- Create a pre-commit script for error check and save it under .git/hooks/pre-commit

```shell
#!/bin/sh
jscs client/**/*.js
jshint client/**/*.js
phpcs --standard=psr2 app/
exec 1>&2
```
- Give executable permission


##### Running Server

```shell
> php artisan serve --port=8002
```

##### Running Client

Run below commands before publishing Client

```shell
> npm install -g gulp bower
> npm install
> bower install
> gulp && gulp watch
```

#### Production

```shell
> npm install -g gulp bower
> npm install
> bower install
> gulp
```

use `public` folder for apache to use the application.

