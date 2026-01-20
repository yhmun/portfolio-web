# Use official caddy image
FROM caddy:2-alpine

# Expose build-time domain as runtime env (fallbacks to localhost if not provided)
ARG DOMAIN_NAME=localhost
ENV DOMAIN_NAME=${DOMAIN_NAME}

# Copy caddy config
COPY prod/Caddyfile /etc/caddy/Caddyfile

# Copy static assets
COPY static/ /usr/share/caddy/

# Standard caddy data/config volumes
VOLUME /data
VOLUME /config

# Expose HTTP/HTTPS ports
EXPOSE 80
EXPOSE 443
