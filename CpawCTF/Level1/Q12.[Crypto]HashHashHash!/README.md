# 問題文
ハッシュ関数とは、値を入れたら絶対にもとに戻せないハッシュ値と呼ばれる値が返ってくる関数です。  
ですが、レインボーテーブルなどでいくつかのハッシュ関数は元に戻せてしまう時代になってしまいました。  
以下のSHA1というハッシュ関数で作られたハッシュ値を元に戻してみてください！（ヒント：googleで検索）  
  
e4c6bced9edff99746401bd077afa92860f83de3  
  
フラグは  
cpaw{ハッシュを戻した値}  
です。  

# 解答
与えられた文字列はSHA1でハッシュ化されています。  
ハッシュ値は不可逆なのでこの文字列を操作して平文を得る、というよりかは  
別の文字列をSHA1でハッシュ化して、与えられた文字列と一致すればその文字列が
フラグということになります。
WEBにレインボーテーブル（かどうかは分かりませんが）ハッシュ値から平文を返してくれる
サービスがあります。  
今回はそのサービスを使いました。
[hashtoolkit](https://hashtoolkit.com/)

ページにアクセスしてテキスト入力エリアにハッシュ値を入力すると  
各ハッシュ関数の平文を表示してくれますのでSHA1の欄に表示される文字列がフラグとなります。