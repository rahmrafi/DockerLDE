## How to setup for PHP/Laravel Project
1. change the path of PHP volume
```
php:
  volumes:
    - ./www:/var/www/html
```
`./www` where your project path

2. change the path of Nginx volume
```
nginx:
  volumes:
    - ./www:/var/www/html
```
`./www` in this ensure same with project path

3. Adding this in nginx/default.conf
```
root /var/www/html/public;

index index.php index.html;

  location / {
    try_files $uri $uri/ /index.php?$query_string;
  }
```
`try_files $uri $uri/ =404;` if this exist just command or delete & `root /var/www/html;` command or delete to

4. Generate APP_KEY & Clear Cache
```
sudo docker exec -it php_LDE bash

php artisan key:generate
php artisan optimize:clear
```

5. Set the Permission
```
chown -R www-data:www-data storage bootstrap/cache
chmod -R 775 storage bootstrap/cache
```

