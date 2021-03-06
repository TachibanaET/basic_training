###### tags: `Python_2nd_Step`
# 4　複雑な条件判断処理

|要　点|説　明|
|---|---|
|プログラムの機能|現在の室内温度・湿度が快適かどうかを判断する。|
|得られる知識|論理演算子 and の使い方|
|手順|（1） ユーザに室内の温温と湿度を入力してもらう。<br/>（2） 入力値を表1と比較し、快適な室内温度・湿度かそうでないかを判定する。<br/>（3） 判定の結果を表示する。|

表1　快適な室内の温度・湿度
|季節|快適な室内温度|快適な室内湿度|
|---|---|---|
|冬|18~22℃|45~60%|
|夏|25~28℃|55~65%|

ファイル名は2_4_temperature.py
```python=
# and を使った複雑な条件判断処理の練習
temperature = int(input('室温を入力してください： '))
humidity = int(input('湿度を入力してください： '))
if 18 <= temperature <= 22 and 45 <= humidity <= 60:
    print('快適です')
elif temperature < 18 and humidity < 45:
    print('寒くて乾燥ぎみです')
elif 22 < temperature and 60 < humidity:
    print('温度が高すぎで多湿ぎみです')
elif 22 < temperature and humidity < 45:
    print('温度が高すぎで乾燥ぎみです')
else:
    print('快適にするためエアコンで調整してください')
```

## コードの解説
|No|行|対象|説明|
|---|---|------------|---|
| 1| 2|`temperature`|変数名のtemperatureは「温度」という意味です。|
| 2| 3|`humidity`|変数名のhumidityは「湿度」という意味です。|
| 3| 4|`18 <= temperature <= 22 and 45 <= humidity <= 60`|快適な温度と湿度の範囲をandで結んでいます。<br/>両方がTrueだと、andがTrueになります。|
| 4| 5|□□□□`print('快適です')`|この温湿度ゾーンで快適と表示させます。|
| 5| 6|`temperature < 18 and humidity < 45`|温度が18度を下回り、湿度が45％を下回る場合です。|
| 6| 7|□□□□`print('寒くて乾燥ぎみです')`|温度が下がると飽和水蒸気量も下がるので、必然的に低湿度になります。|
| 7| 8|`22 < temperature and 60 < humidity`|温度が22度を上回り、湿度も60％を上回る場合です。|
| 8| 9|□□□□`print('温度が高すぎで多湿ぎみです')`|温度が上がると飽和水蒸気量も上がるので高湿度になりがちと表示させます。|
| 9|10|`22 < temperature and humidity < 45`|温度が22度を上回る一方で湿度が45％を下回る場合です。|
|10|11|□□□□`print('温度が高すぎで乾燥ぎみです')`|湿度が高すぎるため加湿が不必要であると表示させます。|
|11|12|`else:`|他の場合は無視して全てelse以下を表示させます。|
|12|13|□□□□`print('快適にするためエアコンで調整してください')`|違うことを入力したユーザへの注意です。|
