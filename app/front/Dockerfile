FROM nginx:alpine

COPY index.html /usr/share/nginx/html/index.html

ENV WS_BACK_URL=http://backend:6000

ENTRYPOINT ["sh", "-c", "sed -i 's#TR_WS_BACK_URL#$WS_BACK_URL#' /usr/share/nginx/html/index.html && nginx -g 'daemon off;'"]

EXPOSE 80
