# 画像投稿できる掲示板

画像投稿できる掲示板です。

## 使い方

```
docker compose up
```
で起動します。
起動後別ウィンドウで
```
docker compose exec mysql mysql example_db
```
入力後MｙSQLクライアントが起動するので下記コードを入力
```
CREATE TABLE `bbs_entries` (
    `id` INT UNSIGNED NOT NULL AUTO_INCREMENT PRIMARY KEY,
    `body` TEXT NOT NULL,
    `image_filename` TEXT DEFAULT NULL,
    `created_at` DATETIME DEFAULT CURRENT_TIMESTAMP
);
```
```
http://{ホスト名}/bbstest.php
```
にアクセスすると使える。
