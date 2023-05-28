# 二十一代集本文テキストのjson化と検索
## # nijuichidaishu

『日本古典籍データセット』の「本文」
https://researchmap.jp/blogs/blog_entries/view/75174/a64a27fb1d38ca51f0c47b9645e347f9?frame_id=653770
のデータを使用し、二十一代集本文をjson化し、検索可能にする。

# 方法
+ データのjson化にはpythonを使用
+ 検索には、javascriptを使用

# 検索
https://wonox.github.io/nijuichidaishu/array_search.html

+ ローマ字で検索すると、母音（aiueo）のみで検索します。

# レーベンシュタイン距離を測って、似ている和歌を抽出する
+ 結果は test1.json
+ 編集距離　1以上15以下のものを抽出
+ 手順は、wakashu.ipynb に記載
+ 編集距離 １とか２は、単に異同がほとんど

# 母音のみでレーベンシュタイン距離を測る
+ 結果は、vowel.json
+ 編集距離 9以下のものを抽出
+ たとえば、以下が似ていることが分かる
++ "auauiaeuaiuoioioooiooaaiuiauiuu", 春霞／たてるやいつこ／みよしのゝ／吉野の山に／雪はふりつゝ￥Ａ古今和歌集￥Ｎ００００３
++ "auaaaaeuaiuoioioooiooaaaauioeuu" 桜花／さけるやいつこ／御吉野の／よしのゝ山は／かすみこめつゝ￥Ａ新後拾遺和歌集￥Ｎ０００７７ 
