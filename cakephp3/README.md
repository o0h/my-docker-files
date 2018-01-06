# php-app-docker-skelton
PHP(CakePHP3)環境を立ち上げる時に使いたい雛形です

## About this
- コンテナをcakeの立ち上げるとビルトインサーバーが起動します
- PHPUnitのコンテナが別に出されています
    - PHPStormでdocker-composeから利用しやすく

## Usage
1. `./cake` というディレクトリにcakephp/appプロジェクトを作成します
    - ex) `composer create-project --dev --prefer-dist cakephp/app cake`
3. コンテナを起動します
    - `docker-compose up -d web db`

## ToDo
- cakeのビルトインサーバー使うのやめて、ちゃんとhttpd使う
- test dbの作成も自動的にやらせる

## Ref.
- [shin1x1/phpstorm\-with\-docker\-for\-mac\-sample](https://github.com/shin1x1/phpstorm-with-docker-for-mac-sample)
    - [PhpStorm \+ Docker for Mac（docker\-compose）での PHPUnit と Remote Debug の設定 \- Shin x Blog](http://blog.shin1x1.com/entry/setup-test-and-debug-on-phpstorm-and-docker-for-mac)
- [Dockerの公式MySQLイメージの使い方を徹底的に解説するよ · DQNEO起業日記](http://dqn.sakusakutto.jp/2015/10/docker_mysqld_tutorial.html)
- [docker\-composeでMySQLに接続する \- Qiita](https://qiita.com/M_Nagata/items/120831bb4e4a3deace13)
