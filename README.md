# gitbootcamp-20181213

==============================================================================================

1.git add
ファイルやディレクトリをインデックスに登録。

==============================================================================================
No.2 [git commit] Written by J.S
なんだか基本的なコマンド過ぎるのか、「コミットする」という説明以外見つけられん。orz
追加・変更したファイルをgitに登録する・・・ということ。
とはいえ、このコマンドだけでは完結せず・・・。
何を登録するのか・・・という指示を逐一行う必要がある。
でっ、何を登録するか・・はgit addにて指定する模様
==============================================================================================

3. git commit -a（git commit -all）
　[概要]
　　現在、Gitの管理対象にあるファイルの変更全てをコミットする（git addを省略できる）
　
  [注意]
　　このコマンドは、新規作成されたファイルがステージされることはないため、
　　新規の追加ファイルは、明示的にgit add する必要がある。
　　.gitignore に記載されたファイルは無視される。

　[参考URL]
　　http://www-creators.com/archives/2106#-a_w_hyphenall

<<<<<<< HEAD
==============================================================================================

4. git commit -amend
　[概要]
　　直前のコミットを修正し、そのコミットと置き換えるように新しくコミットする。
    コミット著者や、日付は維持される。
　
　[注意]
　　これにより作られるコミットの識別子（Sha-1）は以前のものとは異なる新しいものとなる。
　　もし修正前のコミットをpushしてしまっていれば、訂正したコミットを改めてpushしたとき、
　　異なる履歴として、コンフリクトが生じる。

　[参考URL]
　　http://www-creators.com/archives/2106#-a_w_hyphenall

==============================================================================================

4. git branch fix/42
　[概要]
　　現在のHEADから、指定したbranchnameを名前として、新しいブランチを作成する。
　
　[補足]
　　・git branch -d <branchname>	：指定したブランチを削除する。
　　・git branch -m <new branchname>	：現在チェックアウトしているブランチ名を変更する。

　[参考URL]
　　https://qiita.com/chihiro/items/e178e45a7fd5a2fb4599

==============================================================================================
=======

7．git checkout -b fix/42
ブランチを作成して、作成したブランチへ切り替える

==============================================================================================

