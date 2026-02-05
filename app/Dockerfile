FROM nginx:alpine

# Copiamos el HTML
COPY index.html /usr/share/nginx/html/index.html

# Healthcheck para Kubernetes / CI
HEALTHCHECK --interval=30s --timeout=5s \
  CMD wget -qO- http://localhost || exit 1
