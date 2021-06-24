FROM nginx:alpine

ADD conf.d/default.conf /etc/nginx/nginx.conf

RUN apk update && \
    apk add nginx
