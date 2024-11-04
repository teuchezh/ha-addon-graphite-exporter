ARG BUILD_FROM=ghcr.io/home-assistant/amd64-base:latest
FROM $BUILD_FROM

# Установите необходимые зависимости
RUN apk add --no-cache python3 py3-pip

# Установите Graphite Exporter (или создайте свой скрипт)
RUN pip install graphite-api

COPY rootfs/ /
RUN chmod a+x /etc/services.d/example/run

CMD [ "/etc/services.d/example/run" ]
