ARG BUILD_FROM=ghcr.io/hassio-addons/base:14
# Alpine + Python 3.12
FROM $BUILD_FROM
# Installs Synapse, Element, PostgreSQL deps
COPY rootfs/ /
RUN apk add --update --no-cache python3 py3-pip
# Builds Matrix-Server
WORKDIR /matrix
CMD ["/usr/bin/with-contenv", "bash", "/matrix/run.sh"]
