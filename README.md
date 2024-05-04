# laravel-docker-sample
laravel_dir にlaravelを置く
ポートは空いてるとこに変える

## ビルド
```
docker-compose build
docker-compose up -d --build
```
## ログイン
```
docker exec -it container_name bash
```

## DocumentRoot書き換え
```
vim /etc/apache2/sites-available/000-default.conf
/etc/init.d/apache2 restart
```
## docker起動時DB接続できない時
```
alter user 'root'@'%' identified with mysql_native_password by 'root';
```
https://motomotosukiyaki.com/mysql-from-php-server-requested-authentication-method-unknown-to-the-client
## sql通す
```
mysql -u root -proot db_name < /usr/local/etc/mysql.sql
```
