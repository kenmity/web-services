# web-services
嘗試使用docker架設一個本機測試開發環境


1.製作nginx image (也可以直接用官方image)
```
cd nginx-docker-image
docker build -t self-nginx . --no-cache 
```
2.製作php image
```
php7.4-docker-image (這邊使用了php的套件安裝支援 https://github.com/mlocati/docker-php-extension-installer)
docker build -t self-php7.4 . --no-cache
```

3.執行docker-compose.yml
```
docker-compose up -d web php mariadb myadmin memcached  
```

> 資料庫位置這邊會需要先建立空的資料夾


`config/mariadb/data/db`

> 參考來源

https://github.com/nanoninja/docker-nginx-php-mysql

> 使用套件

https://github.com/mlocati/docker-php-extension-installer
