# laravel-docker
Laravel + Docker Compose (PHP-FPM, Nginx, MySQL, Redis)

## Requirements

- Laravel
- Docker Compose
- PHP-FPM
- Nginx
- MySQL
- Redis

## Quick Start

```
docker-compose up -d
docker exec -it laravel-docker_php-fpm_1 bash

composer install
```

## Command

```shell
# コンテナーの生成
# -d: デタッチモード。コンテナーをバックグラウンド起動します。
docker-compose up -d

# Dockerfileからコンテナーを生成
# --build: コンテナー起動前にイメージをビルドします。
docker-compose up -d --build

# コンテナーの一覧表示
# -a: コンテナーすべてを表示します。
docker ps -a

# コンテナーの停止＆削除
docker-compose down

# コンテナーに入る
# PHPのコンテナー上において、対話形式のbashシェルを起動します。
# -i: アタッチされていなくても STDIN は開放し続けます。
#     →標準入力（キーボード）を受け付けることを示すオプションです。
# -t: 擬似 TTY を割り当てます。
#     →標準入出力となっている端末デバイス（TTY→ターミナル）を割り当てるオプションです。
docker exec -it laravel-docker-php-fpm-1 bash

# コンテナーの停止
docker-compose stop

# コンテナーの起動
docker-compose start

# コンテナーの再起動
docker-compose restart
```

## Link

- [Docker CLI](https://matsuand.github.io/docs.docker.jp.onthefly/engine/reference/run/)
- [Docker Compose CLI](https://matsuand.github.io/docs.docker.jp.onthefly/compose/reference/)
