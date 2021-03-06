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

5. git branch fix/42
　[概要]
　　現在のHEADから、指定したbranchnameを名前として、新しいブランチを作成する。
　
　[補足]
　　・git branch -d <branchname>	：指定したブランチを削除する。
　　・git branch -m <new branchname>	：現在チェックアウトしているブランチ名を変更する。

　[参考URL]
　　https://qiita.com/chihiro/items/e178e45a7fd5a2fb4599

==============================================================================================
6. git checkout -b fix/42; git commit
現在チェックアウトしているブランチから、新しく[fix/42]というブランチを作ったうえでチェックアウトする・・・そしてその後commitする
[5]の後で[2]をした・・・というだけ
==============================================================================================

7．git checkout -b fix/42
ブランチを作成して、作成したブランチへ切り替える
==============================================================================================

9. git merge fix/42
現在チェックアウトしているブランチに[fix/42]コミットをマージする

構文
　[１]git merge ～～
　　　現在チェックアウトしているブランチに[～～]で指定したコミットをマージする
     競合が発生している場合は、競合の解決が必要になる。
     競合を解決した場合は、マージ後にマージコミットが作られる
  [2]git merge --ff-only ～～
  　　現在チェックアウトしているブランチに[～～]で指定されたコミットをマージする
  　　競合が発生しないとわかっている場合に使用できる。
  　　競合が発生しないことが前提なので、マージ後にマージコミットが作られることは無い
  [3]git merge --no-ff ～～
  　　現在チェックアウトしているブランチに[～～]で指定されたコミットをマージする
　　　何がどうあれマージコミットが作られる

==============================================================================================

10．git rebase -i A～E
複数のコミットを一つにまとめる

==============================================================================================

21. git cherry pick [ID]
　[概要]
    他のブランチの特定コミットを反映する。

　[補足]
　　・git addした状態になるため、commitが必要

　[参考URL]
　　https://qiita.com/bossunn24/items/dedb620541d852327934

==============================================================================================

22. git init
　[概要]
    Gitのリポジトリを新たに作成する。
　　このコマンドが実行されると、「.git」と名付けられたサブディレクトリが作成される。

　[補足]
　　・同じリポジトリに対して再度実行されても安全（上書きされない）

　[参考URL]
　　https://eng-entrance.com/git-init

==============================================================================================

23. git clone
　[概要]
    指定されたディレクトリに元のリポジトリと同じものを複製する。
　  リモートリポジトリとディレクトリを指定してコマンドを実行する時は下記のようになる。
　　　$ git clone [repo].git copy [dir]

　[補足]
　　・ディレクトリを指定しないことも可能。

　[参考URL]
　　https://qiita.com/chihiro/items/e178e45a7fd5a2fb4599

