# Собираем Docker-образ с тегом my-site
```
docker build -t my-site .
```
# Запускаем контейнер
```
docker run -d \
  --name my-static-site \
  -p 80:80 \
  -p 443:443 \
  -v caddy_data:/data \
  -v caddy_config:/config \
  --restart unless-stopped \
  my-site
```
