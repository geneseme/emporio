docker run -d --name db postgres
docker build -t efforia .
docker run -d --name efforia -v ${root}/efforia-store:/var/www/efforia efforia
docker run -d --name nginx -p 80:80 -v ${root}/certificate:/etc/nginx/conf -v ${root}/config:/etc/nginx/conf.d nginx
