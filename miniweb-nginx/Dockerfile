FROM nginx:alpine

# Setting a WORKDIR
WORKDIR /app

#copying html file from source to nginx html destination
COPY miniweb-nginx/index.html /usr/share/nginx/html

# port for my container to listen on
EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]





