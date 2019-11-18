FROM php:7.3-apache
WORKDIR ./
COPY ./  /var/www/html
COPY .docker/vhost.conf /etc/apache2/sites-available/000-default.conf

EXPOSE 80
EXPOSE 81
RUN chown -R www-data:www-data /var/www && a2enmod rewrite

CMD /usr/sbin/apache2ctl -D FOREGROUND
