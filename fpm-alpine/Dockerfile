FROM wordpress:4.9.4-php7.2-fpm-alpine

RUN apk add --no-cache --virtual .deps wget unzip \
 && mkdir /tmp/wp-plugins && cd /tmp/wp-plugins \
 && wget https://downloads.wordpress.org/plugin/simply-static.2.1.0.zip \
 && wget https://downloads.wordpress.org/plugin/amazon-web-services.1.0.5.zip \
 && wget https://downloads.wordpress.org/plugin/amazon-s3-and-cloudfront.1.3.2.zip \
 && wget https://downloads.wordpress.org/plugin/ga-google-analytics.20180303.zip \
 && unzip './*.zip' -d /usr/src/wordpress/wp-content/plugins \
 && chown -R www-data:www-data /usr/src/wordpress/wp-content \
 && cd \
 && apk del .deps \
 && rm -rf /tmp/wp-plugins \
 && echo "66.155.40.202 api.wordpress.org" >> /etc/hosts
