FROM nginx:alpine

# Borrar TODO el contenido por defecto de nginx
RUN rm -rf /usr/share/nginx/html/*

# Copiar nuestro HTML
COPY index.html /usr/share/nginx/html/index.html

EXPOSE 80

HEALTHCHECK --interval=30s --timeout=5s \
CMD wget -qO- http://localhost || exit 1
