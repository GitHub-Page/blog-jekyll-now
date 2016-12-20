---
layout: post
title: Xcode Error Does not contain bitcode
tags: Xcode8 Error ENABLE_BITCODE disable bitcode for this target. for architecture arm64
---


Xcode Error does not contain bitcode！

```
ld: '/Users/***/***/***/Fabric.framework/Fabric(FABObfuscator.o)' does not contain bitcode. You must rebuild it with bitcode enabled (Xcode setting ENABLE_BITCODE), obtain an updated library from the vendor, or disable bitcode for this target. for architecture arm64
clang: error: linker command failed with exit code 1 (use -v to see invocation)
```

bitcodeオプションについては、以下の記事で解説されています。
◆ LLVM bitcode基礎知識
http://qiita.com/gamako/items/f37dbb05de9d3832ce6b

## ENABLE_BITCODEをNOにする

「Build Settings」から「Enable Bitcode」の項目を検索し、NOにしましょう。
基本的にはこれでビルドが通るはずです。

![ss.png](https://github.com/MMizogaki/blog-jekyll-now/blob/master/Resouce/2016-12-20-ENABLE_BITCODE.png)
