FROM php:7.4-apache

# tzdata、xdebugのインストール
RUN apt-get update && apt-get install -y \
    tzdata \
 && pecl install xdebug \
 && rm -rf /var/lib/apt/lists/*

# タイムゾーンを設定する環境変数
ENV TZ=Asia/Tokyo

# 作業ディレクトリを変更
WORKDIR /usr/local/etc/php

# ファイルのコピー
COPY php.ini ${PWD}
