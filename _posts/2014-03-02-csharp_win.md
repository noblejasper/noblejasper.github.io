---
layout: post
title: UnityC#をWin/Macで共有→UTF-8 with BOM
---

```sh
nkf -w8 —overwrite $f
```

要するにBOM付きのUTF-8にしないとWinでException出ちゃう
