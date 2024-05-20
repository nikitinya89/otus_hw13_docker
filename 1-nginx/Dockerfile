FROM alpine
RUN apk add --no-cache nginx \
    && mkdir /usr/share/nginx/html \
    && mkdir /etc/nginx/conf.d
ADD nginx.conf /etc/nginx/nginx.conf
ADD default.conf /etc/nginx/conf.d/
ADD index.html /usr/share/nginx/html/
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
