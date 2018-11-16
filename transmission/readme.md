docker create --name=transmission \
-v /root/dockerfile/php-nginx-compose/html/transmission-config:/config \
-v /root/dockerfile/php-nginx-compose/html/downloads:/downloads \
-v /root/dockerfile/php-nginx-compose/html/torrent:/watch \
-e PGID=0 -e PUID=0 \
-e TZ=Asia/Shanghai \
-p 9091:9091 -p 51413:51413 \
-p 51413:51413/udp \
linuxserver/transmission
