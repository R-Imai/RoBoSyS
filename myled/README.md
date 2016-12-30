# myled
led点灯のデバイスドライバ

## 付属のbashファイル
`myled.bash` 引数が1でLED点灯，0で消灯<br>
`led_flash.bash` 第一引数の数点滅を繰り返す．点滅間隔は第二引数で指定

## 配線
Raspberry piのGPIO25にLEDを接続する

## 使用方法(例)
```bash
$ make                      #myled.cのコンパイル
$ sudo insmod myled.ko      #デバイスドライバの実行
$ ./myled.bash 1            #ledを点灯
$ ./myled.bash 0            #ledを消灯
$ ./led_flash.bash 10 0.5   #ledを0.5秒ずつ10回点滅
$ sudo rmmod myled          #デバイスドライバ解除
$ make clean                #ディレクトリをきれいに
```
