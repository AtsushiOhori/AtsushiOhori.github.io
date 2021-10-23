---
translated: true
---
教科書の主なコードを
[本書サポートgithubレポジトリ](https://github.com/AtsushiOhori/compiler-text)
にて提供する．

githubレポジトリは以下の手順で利用できる．
1. [本書サポートgithubレポジトリ](https://github.com/AtsushiOhori/compiler-text)をブラウザでアクセス
2. 「Code」ボタンを左クリックすると現れるCloneメニュのHTTPSを選択し，以下の何れかを実行
- URLの右側のコピーボタンを左クリックし，URLをクリップボードにコピーし，shellコマンド`git clone <URL>`を実行
- Download ZIPをクリックしZIPファイルをダウンロード

githubレポジトリは，以下の内容が含まれます．
- `README.md` 簡単な説明
- examples/chap2/ 〜 examples/chap8/ の各ディレクトリ．

これらのディレクトリの中で chap2/はそれ自信がプログラムのメインディレクトリである．
それ以外のディレクトリは，教科書での解説に従い，サブディレクトリに分割されており，それらの中でmainがメインディレクトリである．
各メインディレクトリには，すでにMakefileが用意されている．
smlsharpコマンドがインストールされていれば，以下のようにしてプログラムを実行できるはずである．
```shell-session
$ cd examples/chap2
$ make
smlsharp -O2 -o TM.o -c TM.sml
smlsharp -O2 -o Eval.o -c Eval.sml
smlsharp -O2 -o Main.o -c Main.sml
smlsharp  -o Main Main.smi 
$ ./Main
{T = ([I, I, I], I, []), r = ([], B, [I, O, O, O, O])}
```


