## JavascriptでDroneを飛ばそう

* parrotのRolling Spiderに対応
* 内容はMacで確認

## 手順

### 準備

```
$ git clone git@github.com:n0bisuke/drone-handson.git
$ cd drone-handson
$ npm i
```

### Droneを探す

PCのBluetoothをオンにしましょう。

```
$ node find
1: RS_yyyyy (xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx), RSSI -61
```

xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxとなっている部分が識別子になります。

## Droneを飛ばす

先ほどの識別子を使いコマンドを実行します。

```
$ node app xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Configured for Rolling Spider!  RS_yyyyy
RS_yyyyy => SESSION START
```

こうなったら成功です。PCとDroneがBluetoothで接続されました。

※SESSION STARTが表示されない場合は一度Droneを再起動して再実行してみましょう。

この後はキーボードでキーを押せばOkです。

- t: 離陸 (takeoff)
- l: 着陸 (landing)
- 矢印キー: キーの方向に進む
- u: 上昇(up)
- d: 下降(down)
- f: 前回転(frontFlip)
- b: 後回転(backFlip)
- x: 接続解除

などが基本になります。
