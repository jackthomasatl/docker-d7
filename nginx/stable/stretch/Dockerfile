# jackthomasatl/docker-d7-nginx:stable

FROM nginx:stable

ENV DEBIAN_FRONTEND=noninteractive PHP=5.6 USER=www-data

RUN mkdir -p /opt/docker/ssl

# Move configs in
COPY ./config/nginx.conf /etc/nginx/conf.d/default.conf

# Move php sample app
COPY ./phpinfo /app
RUN ln -s /app /opt/docroot

WORKDIR /app
