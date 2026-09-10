FROM nginx:alpine
COPY . /usr/share/nginx/html
RUN if [ -f /usr/share/nginx/html/*.html ]; then cp /usr/share/nginx/html/*.html /usr/share/nginx/html/index.html; fi
EXPOSE 80
