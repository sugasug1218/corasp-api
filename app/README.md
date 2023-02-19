## 実行環境

    macOS:
    Laravel:
    MySQL:
    nginx:

## APIサーバー環境構築手順

リポジトリのクローン
```
git clone {URL} .
```

dockerビルド
```
docker compose build --no-cache
```

コンテナ起動
```
docker compose up -d
```

コンテナの状態確認
```
docker ps
# app, nginx, mysqlが３つ表示されれば成功してます
```

appサーバーに入る
```
docker compose exec app bash
```

ルートディレクトリに移動してLaravelインストール
```
cd app
composer create-project laravel/laravel .
```

## nginxの動作確認
[http://localhost:8090](http://localhost:8090)にアクセスする。
Laravelのウェルカムページが出たら構築成功
