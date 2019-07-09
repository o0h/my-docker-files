# alpine-phpfpm-nginx-mysql
雑多なPHPウェブアプリケーションを作る時に使いたい雛形です

PHPの公式イメージ(PHP-FPM on Alpine Linux) に NGINXとMySQLイメージを足しています。

## About this
- PHPの公式イメージ時、PDO_MySQLやXdebugを追加しています
- その他に、NGINXとMySQLがいて、それらは公式イメージを素のまま利用しています

## Usage
- `cd docker_files && docker-compose up` で、アプリケーション・ウェブ・データベースのサーバーが起動します
- `localhost:9100` にアクセスして、phpinfoが表示された成功です
- NGNIX、Xdebugは`docker_files/volumes` に入っているそれぞれのconfファイルから情報を上書きできます
- MySQLの初期化は、`docker_files/database/init` の中にあるファイルで実行されます
- DocumentRootは `app/` です
