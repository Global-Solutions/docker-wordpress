FROM gsol/wordpress:4.9.4-php7.2-fpm-alpine-1

RUN echo -e "\n\
    \n\
    remove_action('wp_head', 'wp_resource_hints', 2); \n\
    " \
  >> /usr/src/wordpress/wp-content/themes/twentysixteen/functions.php \
 && echo -e "\n\
    \n\
    body, \n\
    .site { \n\
        background: none !important; /* Brute force since user agents all print differently. */ \n\
    } \n\
    \n\
    .site-info, .widget { \n\
            display: none; \n\
    } \n\
    " \
  >> /usr/src/wordpress/wp-content/themes/twentysixteen/style.css
