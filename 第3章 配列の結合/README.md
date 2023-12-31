### 練習問題3.1
#### 1.前置演算と後置演算のち外について説明してください。
前置演算と後置演算とは、加算（減算）してから値を代入するか、値を代入してから加算（減算）するかという点で異なります。<br>
3.1.2項の例参照<br>
#### 2. PHPで次の演算を実行した場合の結果を答えてください。
①15 - '0x10'<br>
②2**3<br>
③$i++($i = 'z'の場合)<br>
④10 + '1.5e1'<br>
⑤17 % 8<br>
<br>
①15<br>
②8<br>
③AA<br>
④25<br>
⑤1<br>
<br>
①のコードは「Anonnumericvalueencounteredin～」のような警告が発生するので、そもそも書くべきではありません(PHP8の挙動)<br>
PHP7.4以前は「Notice」が表示される。<br>
### 練習問題3.2
#### 1.変数$xが1の場合に0、そうでない場合は-1を、変数$flagにセットするような式を条件演算子（三項演算子）を利用して書いてみましょう。
```PHP
$flag = ($x === 1 ? 0 : -1);
```
### 2.PHPで次の式を評価した場合の結果を答えてください。
①'1.44E2' == 144<br>
②'1.44E2' === 144<br>
③'0x10' == '16'<br>
④[1, 5] > [1, 2, 3]<br>
<br>
①true<br>
②false<br>
③false<br>
④false<br>
<br>
「==」演算子は左辺右辺の内容をなんとか等しいとみなせないかを試みる演算子です。<br>
一見便利に思えますが、文字列と数値の比較では思わぬ結果を引き起こす原因にもなります。<br>
可能な限り、「===」演算子を優先して利用することをお勧めします。<br>
### この章の理解度チェック
#### 1.次の表はPHPの演算子についてまとめたものです。空欄①〜⑥を補って表を完成させてください。ただし、②は３つ以上挙げてください。
| 種類  | 演算子 |
| ------------- | ------------- |
| ① | +, -, *, /, %, ++, -- など |
| 比較演算子 | ②など |
| ③ | &&, and, ||, or, xor, ! など |
| ④ | &, |, ^, <<, >> など |
| ⑤ | 文字列演算子（⑤）, キャスト演算子, 実行演算子（&grave;）, エラー制御演算子（⑥） |
<br>
①代入演算子 または 算術演算子<br>
②==, ===, !=, <>, !==, <, >, <=, >=, ?: など<br>
③論理演算子<br>
④ビット演算子<br>
⑤.<br>
⑥@<br>

#### 2.次のコードは、代入演算子と参照を利用したスクリプトです。スクリプトを終了したときの変数$a、$bの値を答えてください。
```PHP
<?php
$a = 1;
$b = &$a;
$a++;
```
$a 2<br>
$b 2<br>
$bには$aの参照が代入されているので、$aへの演算結果は$bにも反映されます。<br>
#### 3.条件演算子（省略構文）を使って、$errorの値が空なら「正常です。」、空でないなら$errorの値を、それぞれ表示するコードを書いてください。
```PHP
$error = '';
print $error ?: '正常です。';
```
#### 4.次の文章は、演算子の処理についてまとめたものです。空欄①～⑤を補って文章を完成させてください。
式の中に複数の演算子が含まれているときに、どのような順序で処理するのかを定義したものが ① と ② です。「$a+$b*$c」では、「$a+$b」よりも「$b*$c」のほうが ① が ③ ので、「$b*$c」が先に計算されます。<br>
また、「$a+$b－$c」では、「+」「－」演算子の ① は同じで、かつ、左→右の ② を持つので、「$a+$b」が先に計算されます。<br>
ちなみに、「$a==$b==$c」のような記述は ④ となります。これは「==」演算子が ⑤ の性質を持つためです。<br>
<br>
①優先順位<br>
②結合則<br>
③高い<br>
④エラー<br>
⑤非結合<br>
