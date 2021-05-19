# angular-nginx

A simple example of running an Angular application with NGINX and Docker 

## Technologies

- [angular 12](https://angular.io/)
- [Docker 19.03.13](https://www.docker.com/get-started)

## SSL Setup

To access the application over ssl we need to create a self signed SSL certificate. In the app nginx/ssl folder run the following command:

``openssl req -newkey rsa:2048 -nodes -keyout localhost.key -x509 -days 365 -out localhost.crt``

Make sure you have two new files in your nginx/ssl dir

##  Quick Start

1. Make sure you have Docker installed from [Docker Official Page](https://docs.docker.com/get-docker/)
2. In your app root directory run the following command ``docker-compose build``
3. In your app root directory run the following command  ``docker-compose up``

