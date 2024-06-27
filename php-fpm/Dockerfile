FROM php:8.3.8-fpm
RUN docker-php-ext-install mysqli
ADD https://raw.githubusercontent.com/jarrodkim/IaC-1th/main/www.conf /
RUN ["mv","/usr/local/etc/php-fpm.d/www.conf","/usr/local/etc/php-fpm.d/www.conf.bak"]
RUN ["cp","/usr/local/etc/php/php.ini-development", "/usr/local/etc/php/php.ini"]
RUN ["echo","session.save_path = \"/var/lib/php/sessions\"",">>","/usr/local/etc/php/php.ini"]
RUN ["cp","/www.conf","/usr/local/etc/php-fpm.d/www.conf"]
CMD ["php-fpm"]
