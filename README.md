default-web-stack
=================

A new default web stack - using docker

Loosely based on Simon Willison's presentation at [A New Default Web Stack](https://www.youtube.com/watch?v=P68zXJ_ACCE)

This is still experimental, try cloning the repo and running:

    cat >> mydomain.yml << EOF
    varnish:
        environment:
            - VIRTUAL_HOST=mysite.mydomain.com
            - LETSENCRYPT_HOST=mysite.mydomain.com
            - LETSENCRYPT_EMAIL=webmaster@mydomain.com
    EOF
    docker-compose up -f docker-compose.yml -f mydomain.yml up
