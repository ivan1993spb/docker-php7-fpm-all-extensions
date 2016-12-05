
# Docker PHP7 fpm all extensions [![Docker Repository on Quay](https://quay.io/repository/ivan1993spb/php7-fpm-all-extensions/status "Docker Repository on Quay")](https://quay.io/repository/ivan1993spb/php7-fpm-all-extensions)

## Pull docker image

```
docker pull quay.io/ivan1993spb/php7-fpm-all-extensions
```

## Installed extensions

- bz2
- curl
- iconv
- imap
- intl
- gd
- json
- mbstring
- mcrypt
- mysqli
- opcache
- pdo
- pdo_mysql
- pdo_pgsql
- pdo_sqlite
- pgsql
- readline
- soap
- xml
- xmlrpc
- xsl
- zip

## Nginx server config example

```
server {
    listen 80;

    root /var/www;

    server_name localhost;

    error_log /var/log/nginx/localhost.error.log;
    access_log /var/log/nginx/localhost.access.log;

    location / {
        fastcgi_index index.php;
        include fastcgi_params;
        fastcgi_pass 127.0.0.1:9000;
        fastcgi_param SCRIPT_FILENAME $document_root/$fastcgi_script_name;
    }
}
```
