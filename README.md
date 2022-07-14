# SPA practice(2022/04-2022/07)
## 概要
Docker環境でReact,LaravelをSPA開発をゴールとする。
Docker環境構築は以下を使用
https://github.com/ucan-lab/docker-laravel

## 使用方法

1. Click [Use this template](https://github.com/ucan-lab/docker-laravel/generate)
2. Git clone & change directory
3. Execute the following command

```bash
$ make create-project # Install the latest Laravel project
$ make install-recommend-packages # Optional
```

http://localhost

## ヒント

- Read this [Makefile](https://github.com/ucan-lab/docker-laravel/blob/main/Makefile).
- Read this [Wiki](https://github.com/ucan-lab/docker-laravel/wiki).

## コンテナ構成

```bash
├── app
├── web
└── db
```

### app コンテナ

- Base image
  - [php](https://hub.docker.com/_/php):8.1-fpm-bullseye
  - [composer](https://hub.docker.com/_/composer):2.2

### web コンテナ

- Base image
  - [nginx](https://hub.docker.com/_/nginx):1.22

### db コンテナ

- Base image
  - [mysql/mysql-server](https://hub.docker.com/r/mysql/mysql-server):8.0

### mailhog コンテナ

- Base image
  - [mailhog/mailhog](https://hub.docker.com/r/mailhog/mailhog)
