# docker-laravel-nuxtjs-nginx-php
docker = laravel + nuxtjs + nginx + php-fpm

## 디렉토리 구조

docker 파일과 volume으로 연결할 docker, database, logs로 각각 폴더로 구분하여 volume 마운트 시킴

* 폴더 성격 별로 상위 디렉터리를 구성하고, 각 컨테이너 기능별로 하위 폴더를 구성.

이러한 접근법을 사용한 디렉토리 구조는 다읍과 같습니다.

    .
    project-root/
    ├── .docker/
    │   ├── laravel/
    │   │   └── Dockerfile
    │   ├── nuxtjs/
    │   │   └── Dockerfile
    │   ├── nginx/
    │   │   └── nginx.conf
    ├── .databases/
    │   ├── mariadb/
    │   └── postgresql/
    ├── .log/
    │   ├── nginx/
    │   ├── mariadb/
    │   └── postgresql/
    ├── .certbot/
    │   ├── conf/
    │   └── www/
    ├── laravel/
    ├── nuxtjs/
    └── docker-compose.yml
    └── .env
