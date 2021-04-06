FROM nginx:1.19

ARG nginx_uid=1001
ARG nginx_git=1001

RUN usermod -u $nginx_uid -o nginx

COPY ./default.conf.template /etc/nginx/templates/default.conf.template
COPY ./app/* /usr/share/nginx/html/

ENTRYPOINT ["nginx", "-g", "daemon off;"]
