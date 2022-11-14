FROM php:8.0-apache
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli
RUN apt-get update && apt-get upgrade -y
COPY apache.conf /etc/apache2/sites-available/ajimtor.conf
RUN a2dissite 000-default.conf
RUN a2ensite ajimtor.conf
COPY bd/* /var/www/ajimtor/