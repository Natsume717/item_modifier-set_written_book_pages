# item_modifier-set_written_book_pages
item_modifierの1項目であるset_written_book_pagesのサンプルになります。

詳しくはブログ記事『[【マイクラ】set_written_book_pagesでページを挿入【item_modifier】](https://natsumake.com/item_modifier-set_written_book_pages/)』を参考にしてください。

<h3>概要</h3>
記入済みの本に対して、文章（ページ）の追加を行えるものです。

<h3>使い方</h3>

データパック導入後、ワールドに入り```/reload```と入力し実行してください。

sample_textという文章が５ページ分記述された記入済みの本が付与されます。

それをメインハンドに持って、以下のコマンドを実行することで、文面を変更できます。

```copy
/item modify entity @s weapon.mainhand sample:append
```

```copy
/item modify entity @s weapon.mainhand sample:insert
```

```copy
/item modify entity @s weapon.mainhand sample:replace_all
```

```copy
/item modify entity @s weapon.mainhand sample:replace_section
```

挿入規則については、[set_writable_book_pages](https://github.com/Natsume717/item_modifier-set_writable_book_pages)と同じです。

|項目|挿入の規則|
|-|-|
|append|最後のページに挿入|
|insert|指定したページに当てはまるよう挿入|
|replace_all|内容をすべて上書き|
|replace_section|指定したページからsizeで指定した分のページをまとめて上書き|

replace_sectionについて補足。<br>
offsetが0、sizeが1だとした場合は、1ページ目と2ページ目の計2ページが指示したテキストへと変更される。<br>
offsetが0ではあるが、1ページを0としてカウントし始めるので、初めの2ページが上書きされるということ。
