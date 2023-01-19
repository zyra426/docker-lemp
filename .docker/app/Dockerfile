FROM php:8.1-fpm-alpine

# Install extensions
RUN docker-php-ext-install pdo_mysql bcmath mysqli && docker-php-ext-enable pdo_mysql bcmath mysqli

# Install Composer
COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer

RUN apk -U upgrade