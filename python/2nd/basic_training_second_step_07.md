###### tags: `Python_2nd_Step`
# 7　1月から12月まで表示させるプログラム（for文を使う場合）

|要　点|説　明|
|---|---|
|プログラムの機能|1月から12月まで、文字列を画面に表示するスマートな方法を知る。|
|得られる知識|for文の使い方|
|手順|（1） 繰り返し文を使う。<br/>（2）表示させる。|

ファイル名は2_7_month.py
```python=
# 1月から12月までループ文で表示させるプログラム
for i in range(12):
    print(i+1, '月')
```

## コードの解説
|No|行|対象|説明|
|---|---|------------|---|
|1|2|`for i in range(12):`|**for文**です。書き方に決まりがあります。<br/>構造　for 変数 in 繰り返し反復処理:<br/>iは変数名です。<br/>range()関数が反復処理して、一つずつ取り出される値を受け取ります。|
|2|2|`range(12)`|**range()関数**と言います。<br/>引数が12なので、range()関数は 0, 1, 2, 3, 4, 5, 6, 7, 8, 7, 9, 10, 11を取り出します。|
|3|3|□□□□`print(i+1, '月')`|print()関数の引数が二つあります。<br/>i+1は、range() 関数が 0, 1, 2, 3・・・と順に取り出して i に代入した値に毎回1を足すという意味です。|
