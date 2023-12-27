# mypkg
* ROS 2関係のノードをまとめたリポジトリ

[![test](https://github.com/Daisuke-joho/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/Daisuke-joho/mypkg/actions/workflows/test.yml)

## 各ノードの説明　
### talker
* パブリッシャを持つノードであり16ビットの符号付き整数をカウントして/countupと名前の付いたトピックでデータを送る.
### listener
* パブリッシャを持つノードからトピックを通して受け取ったデータを出力する.
### talk_listen.launch.py
* talkerとlistenerを同時に実行する.
### トピックについて
* パブリッシャも持つノードのデータを，サブスクライバを持つノードとつなぐ役割をしている.
このパッケージの中ではトピックに/countupと名前を付けて，メッセージの型を16ビットの符号付き整数としている.
## 実行までの手順
### talkerを動かす
  ```
  $ ros2 run mypkg talker
  ```
* 何も出力されない
### listenerを動かす
* talkerとは別の端末で行う
  ```
  $ ros2 run mypkg listener
  ```
* 実行結果
 ```
[INFO] [1703560288.398308876] [listener]: Listen: 7
[INFO] [1703560288.889001055] [listener]: Listen: 8
[INFO] [1703560289.389719868] [listener]: Listen: 9
[INFO] [1703560289.889399952] [listener]: Listen: 10
[INFO] [1703560290.390007552] [listener]: Listen: 11
[INFO] [1703560290.890068284] [listener]: Listen: 12
[INFO] [1703560291.388953017] [listener]: Listen: 13
[INFO] [1703560291.890267991] [listener]: Listen: 14
[INFO] [1703560292.390324538] [listener]: Listen: 15
[INFO] [1703560292.889139874] [listener]: Listen: 16
[INFO] [1703560293.390363416] [listener]: Listen: 17
[INFO] [1703560293.890191701] [listener]: Listen: 18
[INFO] [1703560294.390514872] [listener]: Listen: 19
[INFO] [1703560294.889643834] [listener]: Listen: 20
[INFO] [1703560295.390466142] [listener]: Listen: 21
[INFO] [1703560295.890198152] [listener]: Listen: 22
[INFO] [1703560296.390416623] [listener]: Listen: 23
  ```
## talk_listen.launch.pyを使って実行する方法
 ```
  $ ros2 launch mypkg talk_listen.launch.py
  ```
* 実行結果
 ```
[INFO] [launch]: All log files can be found below /home/daisuke/.ros/log/2023-12-26-12-31-41-030731-LAPTOP-STA8A1L5-26629
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [26631]
[INFO] [listener-2]: process started with pid [26633]
[listener-2] [INFO] [1703561501.817035533] [listener]: Listen: 0
[listener-2] [INFO] [1703561502.309299793] [listener]: Listen: 1
[listener-2] [INFO] [1703561502.808054410] [listener]: Listen: 2
[listener-2] [INFO] [1703561503.309610758] [listener]: Listen: 3
[listener-2] [INFO] [1703561503.808927261] [listener]: Listen: 4
[listener-2] [INFO] [1703561504.308859136] [listener]: Listen: 5
[listener-2] [INFO] [1703561504.809080681] [listener]: Listen: 6
[listener-2] [INFO] [1703561505.308904479] [listener]: Listen: 7
[listener-2] [INFO] [1703561505.809291654] [listener]: Listen: 8
[listener-2] [INFO] [1703561506.308698577] [listener]: Listen: 9
[listener-2] [INFO] [1703561506.809484381] [listener]: Listen: 10
  ```
## 必要なソフトウェア
* Python
  * テスト済み: 3.7~3.10

## テスト環境
* Ubuntu 20.04
* ROS 2 Foxy

## ライセンスと著作権
* このソフトウェアパッケージは,３条項BSDライセンスの下,再頒布および使用が許可されます.
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
  * [ryuichiueda/my_slides robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
* © 2023 Daisuke Shioda
