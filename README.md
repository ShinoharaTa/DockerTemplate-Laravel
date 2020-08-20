# DockerTemplate-Laravel

これはLaravelを使用するためのDockerTemplateです。

## 構成

以下のコンテナが内包されます。

1. PHP 7.3 (php7.3-fpm)
2. Nginx (Official Image)
3. MySQL 5.7

## 使い方

1. `.env.exsample`をコピーし、`.env`ファイルを生成します。
2. `.env`の内容を変更します。
    ```
# アプリケーション名
APP_NAME=[アプリケーション名]

# Laravel root directory
LARAVEL_DIR=[ソースディレクトリを指定]
# ../src, ../laravelなど、別ディレクトリも指定可能

# Nginx port
NGINX_USE_PORT=[ポート番号(default:8000)]

# Mysql DB Set
DB_NAME=[DB名]
DB_USER=[DBユーザー]
DB_PASS=[DBパスワード]
```

## 実行

# ビルド

```BASH
docker-copose build --no-cache
```
# 起動

```BASH
docker-copose up -d
```

# 終了

```BASH
docker-copose down
```

# コンテナに入る

```BASH
# win
winpty docker exec -it [アプリケーション名]-php bash
# other
docker exec -it [アプリケーション名]-php bash
```
