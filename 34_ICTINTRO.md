---
layout: page
title: 情報通信概論
permalink: /ICTINTRO/
---

# 情報通信概論

# 第１回　ガイダンス，プログラムとは
* [情報通信概論１](https://sistkanri-my.sharepoint.com/:b:/g/personal/kato_takekazu_sist_ac_jp/Eb1GDnuVCblBkT1XboCY1zsBJxlkDRCmsEGnxpudTAE-Nw?e=4plhhy)
  * リンク先はOffice365アカウント（大学のメールアカウント，パスワード）でログインしてアクセスします．
* 課題
  * 次の計算をするTD4のマシン語プログラムを作成しなさい．
    * スライド23ページの例題プログラム（３個）
      * LEDを4回だけ点滅させるプログラムに間違いがありました．正しくは
        * 意味　　アセンブラ　　マシン語
        * PC←12  MOV A,12 00111001
        * O/P←15 OUT 15   10111111
        * O/P←0  OUT 0    10110000
        * A←A+1  ADD A,1  00000001
        * PC←1   JNC      11100001
        * PC←5   JMP 5    11110101 
 
    * できた人はやってみよう
      * １から５まで足し算をするプログラム
      * ~~１から16-(I/Pに指定した数)まで足し算するプログラム~~
      * 16-(I/Pに指定した数)の回数だけLEDを点滅させるプログラム
  * 計算結果をOUTPUT（O/P）に出力すること
  * 結果をOUTPUTに出力している状態で，全画面のスクリーンショットを取って提出すること
    * スクリーンショットの取り方
    * https://support.microsoft.com/ja-jp/help/13776/windows-use-snipping-tool-to-capture-screenshots
  * iLearnで提出（4月18日まで），iLearnのアカウントが間に合わない人はメールで提出
    * kato.takekazu@sist.ac.jp
    
# 第２回　プログラミング言語，C言語の基本的な構造
* 復習：
  * 前回のスライド資料を見ながら課題をする
  * 教科書5.2章を読む
* 予習：
  * 教科書第２章を読む
  * 103ページから105ページの演習問題をやってくる
