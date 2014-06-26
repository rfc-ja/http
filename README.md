HTTP RFC 日本語訳
=================

## 翻訳版作成にあたってのルール


文章は「である」調で書いてください。

### HTML の書き方

文書内に英語原文と日本語文を併記し、それぞれ <code>p</code> や <code>span</code> 等でマークアップし、<code>lang</code> 属性を加えてください。
例えば
<pre><code>&lt;p lang=&quot;ja&quot;&gt;これはペンです。&lt;/p&gt;
&lt;p lang=&quot;en&quot;&gt;This is a pen.&lt;/p&gt;
</code></pre>
その際、両方を同時に文書に含んでいてもマークアップとして不自然でないようにしなければなりません。
例えば次のようなマークアップはいけません。
<pre><code>&lt;h1 lang=&quot;ja&quot;&gt;見出し&lt;/h1&gt;
&lt;h1 lang=&quot;en&quot;&gt;Heading&lt;/h1&gt;
</code></pre>
このようにすべきです。
<pre><code>&lt;h1&gt;&lt;span lang=&quot;ja&quot;&gt;見出し&lt;/span&gt;&lt;span lang=&quot;en&quot;&gt;Heading&lt;/span&gt;&lt;/h1&gt;</code></pre>

原文での "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", "OPTIONAL" (これらの意味は [RFC 2119](http://tools.ietf.org/html/rfc2119) を参照) に対応する日本語は <code>em</code> 要素にてマークアップしてください。

### スタイリング

共通のスタイルシートを使用してください。
<pre><code>&lt;link rel=&quot;stylesheet&quot; href=&quot;./rfc.css&quot; /&gt;</code></pre>

### 注意書き

必ず先頭に翻訳物に関する注記を入れてください。
<pre><code>&lt;body&gt;
&lt;div class="translation-note"&gt;
...
&lt;div&gt;
...
</code></pre>
すでにリポジトリにある他の翻訳物を真似するとよいでしょう。

### 翻訳しない部分

下記は日本語訳しないでそのままにしてください。

* 先頭のメタデータ（文書番号、著者など）
* 原文の著作権表示


