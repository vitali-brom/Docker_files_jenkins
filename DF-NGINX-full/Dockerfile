FROM nginx:latest

#RUN mkdir /data
#WORKDIR /data
#RUN echo "Hello from Volume" > test-file    #he auto create
#VOLUME /data
# COPY ./datas /data

 RUN mkdir /usr/share/nginx/html/music && \
     mkdir /usr/share/nginx/html/pics  && \
     rm /etc/nginx/nginx.conf && \     
     cd / 
#     cp /data/music/sample-3s.mp3 usr/share/nginx/html/music/sample-3s.mp3 && \
#     cp /data/pics/pic.jpg usr/share/nginx/html/pics/pic.jpg && \
#     cp /data/nginx.conf /etc/nginx/nginx.conf && \
#     cp /data/conf.d/shit.conf /etc/nginx/conf.d/shit.conf
#
    #cp /data/cerbot/conf/ /etc/nginx/ssl/

COPY ./datas/html/index.html /usr/share/nginx/html/
COPY ./datas/music/sample-3s.mp3 usr/share/nginx/html/music/sample-3s.mp3
COPY ./datas/pics/pic.jpg usr/share/nginx/html/pics/pic.jpg

COPY ./datas/nginx.conf /etc/nginx/nginx.conf
COPY ./datas/conf.d/shit.conf /etc/nginx/conf.d/shit.conf

COPY ./datas/certbot/conf /etc/nginx/ssl/
COPY ./datas/certbot /etc/letsencrypt
    

EXPOSE 80
EXPOSE 443

CMD ["nginx", "-g", "daemon off;"]
