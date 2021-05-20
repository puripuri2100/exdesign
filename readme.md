# 概要

カスタマイズができるよう、開発した[SATySFi](https://gfngfn/SATySFi)のクラスファイルです。
SATySFiに付属するstdjaやstdjabook等のクラスファイルをかなり参考にして作成しました。

さらに、このクラスファイルに付属する補助パッケージを使用することで、楽にカスタマイズできるようになっています。

# 動作する環境

[SATySFi v0.0.6](https://github.com/gfngfn/SATySFi/releases/tag/v0.0.6)での動作を確認しています。

# 導入のしかた

opamとsatyrographosをインストールした状態で

```
opam update
opam install satysfi-class-exdesign
satyrographos install
```

を実行します。

# 使い方

~~~
@require: class-exdesign/exdesign
@require: class-exdesign/article-ja

document (|
        title = {title};
        author = {puripuri2100};
        date = {2018/11/04};
        show-title = true;
        show-toc = true;
        style = ArticleJa.a4paper;
        design = ArticleJa.article;
        header-footer = ArticleJa.normalHF;
        fonts = ArticleJa.fonts;
|) '<
    +p{test}
>
~~~

などのようにすれば使うことができます。

stdjaを使用するのに対して、`style`・`design`・`header-footer`・`fonts`が追加されています（`date`も追加されていますが割愛します）。
ここには本来ならばレコード型が書かれるはずですが、`@require: class-exdesign/article-ja`によって読み込まれている、補助パッケージであるarticle-jaパッケージによって事前に値が定められているため、短い文字で容易に指定することが可能になっています。

この補助パッケージは今後増やしていく予定です。

この補助パッケージは自分で書くことができますが、それについてはマニュアルを読んでください。

# 開発に関して

バグ報告や、プルリクエストは歓迎しています。

# Version歴

- 2018/11/11 v0.1
- 2018/11/18 v0.2

---

(c) Naoki Kaneko and T. Suwa 2018-2021

https://github.com/puripuri2100/exdesign
