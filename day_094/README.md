# Day 94

この記事はQuine Advent Calendar 2014の94日目です。古屋兎丸の「ライチ☆光クラブ」を買ってしまいました。期待を裏切らない面白さで買ってよかったと思います。

今日はCrocでQuineを書きました。CrocというのはMiniD（D言語で実装されたスクリプト言語）からの流れで開発されているスクリプト言語ですが、どうやら今はC++で書かれているらしいです。Lua、D、Squirrel、Ioなどの影響を受けているそうです、と聞くと組み込み向けっぽいのですが、module宣言が必要だったりするので単体でアプリケーションを作るのかもしれません。ともかく、今一狙いが分からないです。

Quineはなんかformatとか使いました。一番のコードsampleは`croc.cpp`の中に生文字リテラルで埋め込まれたソースコードだと思います。

```console
$ diff quine.croc <(croc quine.croc)
```