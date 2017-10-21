# starter

開始してから最初に行なうこと

## デプロイ関連

### 最初のソースを そのまま git管理にする

```
# 共有リポジトリ作成
$ mkdir ~/src
$ cd ~/src_test/
$ mkdir src.git
$ cd src.git
$ git --bare init --shared
```

```
# ローカルリポジトリ作成
$ cd ~/
$ git clone ~/src_test/src.git
$ git add ./
$ git commit -m '初期化'
$ git push origin master
```

* 各々 で 共有リポジトリをclone する
* デプロイはブランチ変えたりしながら pull で行なう

## スペック確認

### CPU

```
$ grep processor /proc/cpuinfo
processor	: 0
```

### メモリ

```
$ free -mh
             total       used       free     shared    buffers     cached
Mem:          2.0G       499M       1.5G         0B        16M       278M
-/+ buffers/cache:       204M       1.8G
Swap:         1.4G         0B       1.4G
```

### 動作しているプロセス

```
$ ps afux
```

競技に不要そうなプロセスがあれば kill する

### ネットワーク統計確認

```
$ netstat
```

* オプション
  * l
    * LISENポート
  * t
    * tcp
  * a
    * all
  * n
    * ポート番号表示
  * p
    * プログラム名

どこにコネクション貼ってあるとか確認する
