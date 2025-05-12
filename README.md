# 始めにやること

- `docker compose exec ~ に入っておく`
以下まとめて実行
- `chmod -R guo+w storage`
- `php artisan storage:link`
- `php artisan migrate`
- `npm install`
- `npm run dev`
- `composer install`

- .env.exampleの内容を.envに貼り付け(同じ階層でOK)

## docker

- `docker compose up -d`
- `docker compose exec laravel-app bash`

## アクセス

- web:`http://localhost`
- phpMyAdmin:`http://localhost:3001`

## 説明

### 動作フロー

1. Laravelサーバーが起動 (localhost:80)
2. Viteサーバーが起動 (localhost:5173)
3. LaravelのBladeテンプレートに `@vite()` ディレクティブがあると `vite.config.js` にしたがってVite開発サーバーにアクセスするようにHTMLを書き換える
4. ブラウザが `localhost:5173` に接続してJS/CSSを読み込む

### 本番環境

- 本番環境ではNode.jsサーバーは使用せず事前にビルドされたアセットをLaravelが返す形になる (npm run build)