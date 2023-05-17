# docker-laravel9
## このレポジトリの使用方法
レポジトリをクローンする
```
git clone https://github.com/keigo64721/Docker-laravel9.git
```

ディレクトリに移動し、dockerを起動する
```
cd Docker-laravel9
docker compose up -d
```

appコンテナに入る
```
docker compose exec app bash
```

権限の付与とライブラリ群のインストール
```
chmod -R 777 storage bootstrap/cache
composer install
```

.env.exampleのコピー
```
cp .env.example .env
```

キーの生成
```
php artisan key:generate
```

ストレージのリンク(storageを使う場合)
```
php artisan storage:link
```

マイグレーションを実行
```
php artisan migrate
```

appコンテナを抜ける
```
exit
```

コンテナを停止(作業を終える場合)
```
docker compose down
```

## ローカルのURL
```
http://localhost:8080/
```
