# 問題文
暗号には大きく分けて、古典暗号と現代暗号の2種類があります。  
特に古典暗号では、古代ローマの軍事的指導者ガイウス・ユリウス・カエサル（英語読みでシーザー）が初めて使ったことから、名称がついたシーザー暗号が有名です。  
これは3文字分アルファベットをずらすという単一換字式暗号の一つです。次の暗号文は、このシーザー暗号を用いて暗号化しました。暗号文を解読してフラグを手にいれましょう。

暗号文: fsdz{Fdhvdu_flskhu_lv_fodvvlfdo_flskhu}

# 解答
問題文にある通りシーザー暗号です。  
暗号文中に出現するアルファベットを三文字分ずらすことで復号できます。
+3ずらすか-3ずらすかの可能性がありますが、今回は-3ずらすことでフラグが取得できました。

# ソルバ
#### solver.py
```python
c = 'fsdz{Fdhvdu_flskhu_lv_fodvvlfdo_flskhu}'

for char in c:
  # {}とか_はずらさないでそのまま出力する
  if char.isalpha():
    print(chr(ord(char) - 3),end='')
  else:
    print(char, end='')
```