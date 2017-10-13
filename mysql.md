# mysql

mysql関連 チューニング

## 設定変更

```
# 設定項目確認
SHOW GLOBAL VARIABLES;
```

```
# 設定ファイル
/etc/my.cnf
/etc/mysql/my.cnf
SYSCONFDIR/my.cnf
$MYSQL_HOME/my.cnf
```

```
innodb_buffer_pool_size
```

## 確認ツール

```
# インストール
$ wget https://github.com/KLab/myprofiler/releases/download/0.1/myprofiler.linux_amd64.tar.gz
$ tar xf myprofiler.linux_amd64.tar.gz
$ sudo mv myprofiler /usr/local/bin/
```

* https://github.com/KLab/myprofiler/blob/master/README-ja.md

```
# 使い方 例
myprofiler -host=db1234 -user=dbuser -password=dbpass -interval=0.2 -delay=10 -top=30
```
