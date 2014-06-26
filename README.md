HTTP RFC 日本語訳
=================

## 翻訳版作成にあたってのルール


文章は「である」調で書いてください。

### HTML の書き方

文書内に英語原文と日本語文を併記し、それぞれ `p` や `span` 等でマークアップし、`lang` 属性を加えてください。
例えば

    <p lang="ja">これはペンです。</p>
    <p lang="en">This is a pen.</p>

その際、両方を同時に文書に含んでいてもマークアップとして不自然でないようにしなければなりません。
例えば次のようなマークアップはいけません。

    <h1 lang="ja">見出し</h1>
    <h1 lang="en">Heading</h1>

このようにすべきです。

    <h1><span lang="ja">見出し</span><span lang="en">Heading</span></h1>

原文での "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", "OPTIONAL" (これらの意味は [RFC 2119](http://tools.ietf.org/html/rfc2119) を参照) に対応する日本語は `em` にてマークアップしてください。そのとき `title` 属性に元の語を入れるとなお良いです。

    <p lang="ja"> ... を送信し<em title="MUST">なければならない</em>。</p>

しばしば現れる、用例や値一覧、構文定義など、等幅を前提とした表現は、そのまま `pre` で書くのが簡便でよいです。


### スタイリング

共通のスタイルシートを使用してください。

    <link rel="stylesheet" href="./rfc.css" />

### 注意書き

必ず先頭に翻訳物に関する注記を入れてください。

    <body>
    <div class="translation-note">
    ...
    </div>
    ...

すでにリポジトリにある他の翻訳物を真似するとよいでしょう。

### 翻訳しない部分

下記は日本語訳しないでそのままにしてください。

* 先頭のメタデータ（文書番号、著者など）
* 原文の著作権表示


