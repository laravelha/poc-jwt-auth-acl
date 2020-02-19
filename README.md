#  Laravelha POC ACL
Proof of concept to preset-api and jwt-auth-acl

## Screenshots

![Swagger](/public/images/swagger.png)

## How to reproduce?
1. install laravel fresh app
```shell script
composer create-project --prefer-dist laravel/laravel poc-jwt-acl && cd poc-jwt-acl
```
2. Install laravelha/preset-api
```shell script
composer require laravelha/preset-api
```
3. Run preset
```shell script
php artisan preset ha-api
```
4. Install and run assets
```shell script
npm install && npm run dev
```

5. Install laravelha/generator
```shell script
composer require laravelha/jwt-auth-acl
```

6. Publish laravelha generator config file
```shell script
php artisan vendor:publish --tag=jwt-auth-acl-config
```

7. Run migrations
```shell script
php artisan migrate
```

8. Populate permissions
```shell script
php artisan db:seed --class=PermissionsTableSeeder
```
