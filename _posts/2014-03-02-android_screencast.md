---
layout: post
title: Android kitkatで画面録画機能＆ファイルをPCに持ってくるシェルスクリプト
---

## 画面録画の方法

* AndroidをUSBでつないで、下記コマンドで開始
* Ctrl-Cで終了
* Android内に保存される。
* 3分ぐらい録画出来た(--time-limit 指定出来るぽいので公式Document読もう)

```sh
/Applications/android_sdk/platform-tools/adb shell screenrecord --size 720x1280 /sdcard/Movies/moviename.mp4
```

#### 参考
* [【レビュー】KitKatこと「Android 4.4」に搭載された画面録画機能を試す - PC Watch](http://pc.watch.impress.co.jp/docs/topic/review/20131127_625291.html)
* [「Nexus 5」でKitKatの新機能「screenrecord」を実際に試してみた - GIGAZINE](http://gigazine.net/news/20131105-nexus5-2nd-review/)

#### 公式Document
* [Android Debug Bridge | Android Developers](http://developer.android.com/tools/help/adb.html#screenrecord)

## ファイル転送の方法

* AndroidをUSBでつないで、下記コマンドで転送

```sh
/Applications/android_sdk/platform-tools/adb pull /sdcard/Movies/moviename.mp4 ~/Desktop/
```

### サンプル
<iframe width="420" height="315" src="//www.youtube.com/embed/lGey47fJSGU" frameborder="0" allowfullscreen></iframe>
