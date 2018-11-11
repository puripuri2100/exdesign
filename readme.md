# 概要

カスタマイズができるよう、開発した[SATySFi](https://gfngfn/SATySFi)のクラスファイルです。
SATySFiに付属するstdjaやstdjabook等のクラスファイルをかなり参考にして作成しました。

さらに、このクラスファイルに付属する補助パッケージを使用することで、楽にカスタマイズできるようになっています。

# 動作する環境

[SATySFi v0.0.3](https://github.com/gfngfn/SATySFi/releases/tag/v0.0.3)と、[SATySFi for Windows Version 20180708](https://github.com/qnighy/satysfi-cross-windows/releases/tag/20180708)での動作を確認しています。

ただし、近い将来SATySFi for Windowsではまだ提供されていない機能を用いたコマンド等を提供する予定ですので、SATySFi for Windows版も出そうと考えています。

# 導入のしかた

`exdesign.satyh`と補助パッケージをSATySFiの読み込める場所においてください。

開発の関係上、補助パッケージでは`exdesign.satyh`の読み込みを`@import`によって行っているため、ファイル関係には十分注意してください（**今後、きちんと対応していく予定です**）。

# 使い方

~~~
@require: exdesign
@import: article-ja

document (|
        title = {title;
        author = {puripuri2100};
        date = {2018/11/04};
        show-title = true;
        show-toc = true;
        style = ArticleJa.a4paper;
        design = ArticleJa.article;
        header-footer = ArticleJa.normalHF;
|) '<
    +p{test}
>
~~~

などのようにすれば使うことができます。

stdjaを使用するのに対して、`style`と`design`、`header-footer`が追加されています（`date`も追加されていますが割愛します）。
ここには本来ならばレコード型が書かれるはずですが、`@import: article-ja`によって読み込まれている、補助パッケージであるarticle-jaパッケージによって事前に値が定められているため、短い文字で容易に指定することが可能になっています。

この補助パッケージは今後増やしていく予定です。

この補助パッケージは自分で書くことができますが、それについてはマニュアルを読んでください。

# 開発に関して

バグ報告や、プルリクエストは歓迎しています。

---

(c) Naoki Kaneko and T. Suwa 2018

https://github.com/puripuri2100/exdesign