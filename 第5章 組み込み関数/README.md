### 5.1練習問題
#### 1.mb_substr関数を使って、文字列「サーバーサイド技術」から「サイド」という文字列を切り出してみましょう。
```PHP
<?php
$str = 'サーバーサイド技術';
print mb_substr($str, 3, 3);
?>
```
mb_substr関数では、開始位置、抽出する長さを文字数で指定します。<br>

#### 2.mb_convert_kana関数を使って、「ｻｰﾊﾞｰｻｲﾄﾞ技術」に含まれる半角カタカナを全角カタカナに変換してみましょう。
```PHP
<?php
$str = 'ｻｰﾊﾞｰｻｲﾄﾞ技術';
print mb_convert_kana($str, KV);
?>
```
mb_convert_kana関数の第2引数(KV)は規定値なので、省略しても正解です。<br>

#### 3.explode関数を利用して、「鈴木\t太郎\t男\t50歳\t広島県」のようなテキストをタブ文字で分割してみましょう。
```PHP
<?php
$data = "鈴木\t太郎\t男\t50歳\t広島県";
print_r(explode("\t", $data));
?>
```
エスケープシーケンスを利用する場合には、文字列はダブルクォートで括ります。<br>

### 練習5.2
#### 1.スタックとキューについて説明してみましょう。また、スタックとキューを実装するのに利用できる関数を答えてください。
スタックは後入れ先出し（LIFO）と呼ばれる構造で、最後に格納した要素を最初に取り出します。<br>
キューは先入れ先出し（FIFO）と呼ばれ、最初に格納した要素を最初に取り出すデータ構造です。<br>
スタックはarray_push/array_pop関数の組み合わせで、<br>
キューはarray_push/array_shift関数の組み合わせでそれぞれ実装できます。<br>
<br>
今日は、sort関数を勉強したつもりになってた。
やべえ、やる気ない😑
今日もやってない😿
寝よう、そう寝よう
やばい、そろそろ
なにしとん、俺