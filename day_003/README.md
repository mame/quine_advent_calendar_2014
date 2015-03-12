#Day 03

[Quine Advent Calendar](http://www.adventar.org/calendars/645)の3日目です。

1日目、2日目はかなり手を抜いたし、明日からはテストがはじまってしまいさすがに勉強すべきなので、3日目はそれなりに気合を入れて作りました。

「Adventar Quine」です。

これがどのようなものなのかというと、簡単に説明すれば、実行するとQuineとして自身のソースコードを出力することに加えて、Adventarに登録されているカレンダー一覧を取得してきて、表示します。ついでに、ソースコードがAdventarのロゴの形になっています。

つまり、Quineの内部でWebスクレイピング（HTTPリクエスト→HTML解析）を行っているわけですね。

最初はRubyで書こうと思ったのですが、`REXML`モジュールがHTMLのパースに対応していなかったので、くっついてきてるライブラリでHTMLのパースのできるPythonに書き変えた、という経緯があります。

微妙にロゴの形が崩れていたり、最初と最後に余計なものがくっついていたりするのでボクとしては完全に満足のいくものではないのですが（ボクのPython力は5です。ゴミめ‥）、そこを作り込みはじめたら勉強時間どころか睡眠時間まで失ってしまいそうだった、と言い訳しておきます。

```
$ diff <(python3 quine.py) <(python3 quine.py | python3)
```