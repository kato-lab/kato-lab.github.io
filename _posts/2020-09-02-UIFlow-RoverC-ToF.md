---
layout: post
title: UIFlow で RoverCとToFセンサを動かす．
date: 2020-09-02 14:27
category: 
author: Takekazu KATO
tags: [M5Stack, M5StickC, RoverC, ToF, UIFlow]
summary: 
---
なかなか大変だったのでメモ書き．

M5Stack(M5SickC)のプログラムをMakecode風にビジュアルに開発できる[UIFlow](https://m5stack.github.io/UIFlow_doc/ja/)を試しています．これはM5StickCのHATやGroveのUnit用のライブラリが組み込まれていて大変便利です．

迷路探索ロボットの実験のために[RoverC](https://www.switch-science.com/catalog/6206/)と[ToF距離センサユニット](https://www.switch-science.com/catalog/5219/)を組み合わせて使おうとしたのですが，"I2C bus error (19)"と出て同時に使えません．距離センサの読み取りとRoverCへの動作命令の間に50ミリ秒程度のウェイトをいれるとうまくいく場合はありますが，エラーが出ることもあり，どうにも不安定です．

調べてみても，なかなか同じような問題に当たっている人がいないようです．そこで[こちらに](https://github.com/m5stack/UIFlow-Code/blob/master/units/_tof.py)にToFセンサのモジュールのソースコードがあるのでみてみると，70ミリ秒ごとのタイマー割り込みで値の取得をしているようです．どうもこのタイマー割り込みが怪しそうということで，tof0.deinit()でタイマーをとめて，tof0._update()をしてから値を取得するようにすると．．．ビンゴ！．エラーが出なくなり，またセンサの値の更新も高速になりました．