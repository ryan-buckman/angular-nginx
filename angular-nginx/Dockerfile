# Stage 1
FROM node:12.14-alpine as node

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

# Stage 2
FROM nginx:1.13.12-alpine

COPY --from=node /usr/src/app/dist/angular-nginx /usr/share/nginx/html

COPY ./nginx/ssl/localhost.crt /etc/nginx/localhost.crt
COPY ./nginx/ssl/localhost.key /etc/nginx/localhost.key

COPY ./nginx/nginx.conf /etc/nginx/conf.d/default.conf
