ARG PHP_VERSION=8.3

FROM php:${PHP_VERSION}-apache

RUN apt-get update \
	&& apt-get install -y --no-install-recommends \
		libzip-dev \
		libpng-dev \
		libonig-dev \
		unzip \
	&& docker-php-ext-install pdo_mysql mbstring zip exif bcmath \
	&& a2enmod rewrite \
	&& sed -ri -e 's!/var/www/html!/var/www/html/public!g' /etc/apache2/sites-available/*.conf \
	&& sed -ri -e 's!AllowOverride None!AllowOverride All!g' /etc/apache2/apache2.conf \
	&& rm -rf /var/lib/apt/lists/*

WORKDIR /var/www/html
