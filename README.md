# mypkg
* ROS2関係のノードをまとめたリポジトリ

[![test](https://github.com/Daisuke-joho/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/Daisuke-joho/mypkg/actions/workflows/test.yml)

## トピック
* ノードのデータを連結する流路のこと
## 各ノードの説明　
### talker
* 16ビットの符号付き整数をカウントして/countupと名前の付いたトピックでデータを送る
### listener
* talkerからトピックを通して受け取ったデータを出力する
## 実行までの手順
### インストール
  ```
  $ git clone https://github.com/Daisuke-joho/mypkg.git
  ```
### talkerを動かす
  ```
  $ ros2 run mypkg talker
  ```
* 何も出力されない
### listenerを動かす
　``   
  $ ros2 run mypkg listener
  ```

## 必要なソフトウェア
* Python
  * テスト済み: 3.7~3.10

## テスト環境
* Ubuntu 20.04

## ライセンスと著作権
* このソフトウェアパッケージは,３条項BSDライセンスの下,再頒布および使用が許可されます.

* このパッケージは,Ryuichi Uedaのコード（© 2023 Ryuichi Ueda）を基に作られています.
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
  * [ryuichiueda/my_slides robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
* © 2023 Daisuke Shioda
