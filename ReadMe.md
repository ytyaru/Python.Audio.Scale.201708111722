# このソフトウェアについて

メジャースケールにおける各キーごとの構成音を算出した。

ただし変化記号はすべて`#`で表現している。

# 対象ファイル名

ファイル名|説明
----------|----
testScale.py|実行ファイル
MusicTheory/Scale.py|変化記号の定義

# 実行

```sh
$ cd src
$ python testScale.py
```
```sh
$ python testToneFrequency.py 
$ python testScale.py 
0 [0, 2, 4, 5, 7, 9, 11, 0] C ['C', 'D', 'E', 'F', 'G', 'A', 'B', 'C']
1 [1, 3, 5, 6, 8, 10, 0, 1] C# ['C#', 'D#', 'F', 'F#', 'G#', 'A#', 'C', 'C#']
2 [2, 4, 6, 7, 9, 11, 1, 2] D ['D', 'E', 'F#', 'G', 'A', 'B', 'C#', 'D']
3 [3, 5, 7, 8, 10, 0, 2, 3] D# ['D#', 'F', 'G', 'G#', 'A#', 'C', 'D', 'D#']
4 [4, 6, 8, 9, 11, 1, 3, 4] E ['E', 'F#', 'G#', 'A', 'B', 'C#', 'D#', 'E']
5 [5, 7, 9, 10, 0, 2, 4, 5] F ['F', 'G', 'A', 'A#', 'C', 'D', 'E', 'F']
6 [6, 8, 10, 11, 1, 3, 5, 6] F# ['F#', 'G#', 'A#', 'B', 'C#', 'D#', 'F', 'F#']
7 [7, 9, 11, 0, 2, 4, 6, 7] G ['G', 'A', 'B', 'C', 'D', 'E', 'F#', 'G']
8 [8, 10, 0, 1, 3, 5, 7, 8] G# ['G#', 'A#', 'C', 'C#', 'D#', 'F', 'G', 'G#']
9 [9, 11, 1, 2, 4, 6, 8, 9] A ['A', 'B', 'C#', 'D', 'E', 'F#', 'G#', 'A']
10 [10, 0, 2, 3, 5, 7, 9, 10] A# ['A#', 'C', 'D', 'D#', 'F', 'G', 'A', 'A#']
11 [11, 1, 3, 4, 6, 8, 10, 11] B ['B', 'C#', 'D#', 'E', 'F#', 'G#', 'A#', 'B']
```

ドレミファソラシの12音を数値による絶対値(識別値)として内部表現を持たせた。

調号、変化記号についてはすべて`#`に統一することで簡易表示した。これは楽譜上の表示と異なる。

# 課題

楽譜上の表示に合わせるなら、五度圏表からスケールの構成音を生成すべき。しかし未実装である。

* 調号と変化記号について
    * 各キーのときにどの幹音にどの変化記号(`♯`,`♭`)を付与するか決っている
        * 五度圏表から算出できる
            * 五度圏表を実装すべき

# 開発環境

* Linux Mint 17.3 MATE 32bit
* [libav](http://ytyaru.hatenablog.com/entry/2018/08/24/000000)
    * [各コーデック](http://ytyaru.hatenablog.com/entry/2018/08/23/000000)
* [pyenv](https://github.com/pylangstudy/201705/blob/master/27/Python%E5%AD%A6%E7%BF%92%E7%92%B0%E5%A2%83%E3%82%92%E7%94%A8%E6%84%8F%E3%81%99%E3%82%8B.md) 1.0.10
    * Python 3.6.1
        * [pydub](http://ytyaru.hatenablog.com/entry/2018/08/25/000000)
        * [PyAudio](http://ytyaru.hatenablog.com/entry/2018/07/27/000000) 0.2.11
            * [ALSA lib pcm_dmix.c:1022:(snd_pcm_dmix_open) unable to open slave](http://ytyaru.hatenablog.com/entry/2018/07/29/000000)
        * [matplotlib](http://ytyaru.hatenablog.com/entry/2018/07/22/000000)
            * [matplotlibでのグラフ表示を諦めた](http://ytyaru.hatenablog.com/entry/2018/08/05/000000)

# 参考

感謝。

## 音名

* https://ja.wikipedia.org/wiki/%E9%9F%B3%E5%90%8D%E3%83%BB%E9%9A%8E%E5%90%8D%E8%A1%A8%E8%A8%98

## 音階

* https://ja.wikipedia.org/wiki/%E9%9F%B3%E9%9A%8E

### 五度圏

* http://dn-voice.info/music-theory/godoken/

## 音高の算出

* http://www.asahi-net.or.jp/~HB9T-KTD/music/Japan/Research/DTM/freq_map.html
* http://www.nihongo.com/aaa/chigaku/suugaku/pythagoras.htm

## サイン波のスピーカ再生

* http://www.non-fiction.jp/2015/08/17/sin_wave/
* http://aidiary.hatenablog.com/entry/20110607/1307449007
* http://ism1000ch.hatenablog.com/entry/2013/11/15/182442

# ライセンス

このソフトウェアはCC0ライセンスである。

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed.ja)

Library|License|Copyright
-------|-------|---------
[pydub](https://github.com/jiaaro/pydub)|[MIT](https://github.com/jiaaro/pydub/blob/master/LICENSE)|[Copyright (c) 2011 James Robert, http://jiaaro.com](https://github.com/jiaaro/pydub/blob/master/LICENSE)
[pygame](http://www.pygame.org/)|[LGPL](https://www.pygame.org/docs/)|[pygame](http://www.pygame.org/)

