# Dockerを使う

## 機能
機能はシンプルなCRUD。Docker実験用

## Rails

Rails6.0ではYarnのインストールが必要<br>
Dockerfileにて

~~~
RUN curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - \
    && echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list
~~~

~~~
RUN apt get instal -y ~~~~~~ + yarn
~~~ 
yarnを追記

## MySQL

Dockerfileは作らず、docker-compose.ymlに記載<br>
enviroment: でパスワードなど設定可
## nginx

nginxコンテナ用のディレクトリを作り、<br>
Dockerfileを作成<br>
nginx.confを作成しておきコンテナ内にコピー

## docker-compose.yml

ports: <br>
\- ホストのポート:コンテナのポート <br>
depends_on: <br>
  コンテナの起動の順序を制御
