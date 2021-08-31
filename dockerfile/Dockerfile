# this shows how we can extend/change an existing official image from Docker Hub

FROM nginx:latest
# It will work on nginx server

WORKDIR /usr/share/nginx/html
# changing working directory to root of nginx webhost

COPY index.html index.html

# I don't have to specify EXPOSE or CMD because they're in my FROM and the ports have already defined.
