FROM php:7.2-fpm-alpine

RUN apk upgrade --update && apk --no-cache add \
    dom gmagick SimpleXML ssh2 xml xmlreader curl date exif filter ftp gd \
    hash iconv imagick json libxml mbstring mysqli openssl pcre posix sockets \
    SPL tokenizer zlib\
    && docker-php-ext-install -j$(nproc) iconv mysqli pdo pdo_mysql curl bcmath mcrypt mbstring json xml zip opcache \
	&& docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
	&& docker-php-ext-install -j$(nproc) gd

CMD ["php-fpm"]
