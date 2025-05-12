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
