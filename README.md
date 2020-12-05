# raspi4_led_driver

## 概要
ロボットシステム学の課題。RaspberryPi4用のデバイスドライバを作成。<br>
0～9、A～Fまでの入力値に応じて、2進数表現で4つのLEDが点灯する。

## 使用環境および部品
### 環境
* OS : ubuntu20.04
 
### 部品リスト
* RaspberryPi4 ModelB 4GB<br>
* RaspberryPi用電源アダプタ<br>
* ブレッドボード<br>
* LED　4個<br>
* 抵抗300Ω　4個<br>
* ジャンパーワイヤ　適宜<br>

## 配線図
配線図は図のとおりである。GPIO22が1桁目、GPIO23が2桁目、GPIO24が3桁目、GPIO25が4桁目。
![配線図](https://github.com/IGC8810/raspi4_led_driver/blob/main/robosys_schema.PNG)

## 実行コマンド
raspi4_led_driver内のsrcディレクトリに移動
$ make
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0
$ echo F > /dev/myled0
$ echo 0 > /dev/myled0
$ sudo rmmod myled
