# Linuxコマンドについて

目次

- [Linuxコマンドについて](#linuxコマンドについて)
  - [リンク集](#リンク集)
  - [読んでおきたい記事](#読んでおきたい記事)
  - [次調べたいコマンドリスト](#次調べたいコマンドリスト)
  - [その他調べてみたいこと](#その他調べてみたいこと)
  - [ToDo](#todo)
  - [ファイル 及び ディレクトリの操作](#ファイル-及び-ディレクトリの操作)
    - [pwd | 現在のディレクトリ(カレントディレクトリ) を表示](#pwd--現在のディレクトリカレントディレクトリ-を表示)
    - [cd | ディレクトリの移動](#cd--ディレクトリの移動)
    - [ls｜ディレクトリやファイルの参照](#lsディレクトリやファイルの参照)
      - [ディレクトリの扱い方](#ディレクトリの扱い方)
    - [alias](#alias)

## リンク集

| タイトル                                       | URL                                                     |
| :--------------------------------------------- | :------------------------------------------------------ |
| Linux のエミュレータ                           | <https://bellard.org/jslinux/>                          |
| 世の中のエンジニアのalias設定                  | <https://qiita.com/reireias/items/d906ab086c3bc4c22147> |
| Linux導入／運用を支援する情報フォーラム - ＠IT | <https://atmarkit.itmedia.co.jp/ait/subtop/linux/>      |
| フューチャースピリッツのエンジニアブログ       | <https://blog.future.ad.jp/>                            |

## 読んでおきたい記事

| タイトル                                                                      | URL                                                           |
| :---------------------------------------------------------------------------- | :------------------------------------------------------------ |
| CLIを布教するために会社でプレゼンしてきたのでそのまとめ                       | <https://qiita.com/lighttiger2505/items/0f61b8fcd790bab0f3c9> |
| ようこそdotfilesの世界へ                                                      | <https://qiita.com/yutkat/items/c6c7584d9795799ee164>         |
| Linuxで処理をバックグラウンドに切り替えて安全にログアウトする方法             | <https://blog.future.ad.jp/linuxcmd_bg>                       |
| 初心者向け】Linuxコマンドの練習ってどうやったらいいの？効果的な練習方法とは？ | <https://qiita.com/ryu235464345/items/0710a7f77382f67add28>   |
| 環境変数にパスを通すとコマンドが認識されるワケ                                | <https://qiita.com/_mi/items/1e1f1aa9e40ef6cfb935>            |
| インフラエンジニアとしてよく使うコマンド集                                    | <https://qiita.com/sion_cojp/items/04a2aa76a1021fe77079>      |
| Linux いちりのテクの部屋                                                      | <https://ichiri.biz/tech/category/linux/>                     |

## 次調べたいコマンドリスト

| コマンド | 簡略的な内容                               |
| :------- | :----------------------------------------- |
| which    | 実行コマンドのフルパスを表示               |
| grep     | 特定の文字を含む行を抽出する               |
| df       | ディスクの使用率、空き状況を確認           |
| rm       | ファイル 及び ディレクトリの削除           |
| psacct   | サーバー上の全てのコマンド実行のログを取得 |
| history  | コマンドの実行履歴の取得                   |
| less     | テキスト内容を確認                         |
| vi       | テキスト編集                               |
| chmod    | パーミッションの変更                       |
| chown    | ファイルやディレクトリの所有者を変更する   |

## その他調べてみたいこと

- サーバーの環境構築時に設定しておきたいこと
  - またそれをまとめて実行できるスクリプトの作成
- 主なバージョン確認のコマンド
- IPアドレスの確認方法

## ToDo

- [ ] コマンドを調べる
- [ ] Linuxのrootディレクトリ直下にあるディレクトリの意味

## ファイル 及び ディレクトリの操作

| コマンド | 略                      | 内容                                 |
| :------- | :---------------------- | ------------------------------------ |
| pwd      | print working directory | 現在のディレクトリを表示             |
| cd       | change directory        | ディレクトリの移動                   |
| ls       | list                    | ファイル及びディレクトリの一覧を表示 |

### pwd | 現在のディレクトリ(カレントディレクトリ) を表示

```shell
# 構文
pwd
```

### cd | ディレクトリの移動

```shell
# 構文
cd [/path/directory_name/]

# ホームディレクトリに移動
cd ~

# ルートディレクトリに移動
cd /

# 親ディレクトリに移動
cd ../
cd ..

# 2階層上に移動
cd ../..
```

### ls｜ディレクトリやファイルの参照

```shell
# 構文
ls [-option] [file_name or directory_name]

<<COMMENT
デフォルトではカレントディレクトリに関する情報が一覧表示される
COMMENT

# 特定の文字列(textfile)から始まるものだけを表示
ls textfile*

# 特定の拡張子(.zip)だけを表示
ls *.zip

# .で始まる隠しファイル等もすべて表示
ls -a

# 詳細情報をリスト形式で表示
ls -l

# ディレクトリ名 (ファイル名) のみでリスト形式で表示
ls -1

# サイズを人が読みやすい形式に表示
ls -h

# ディレクトリ(サブ)を再帰的に表示
ls -R

# ソートの順番を逆順にする
ls -r

# ディレクトリの内容ではなく、ディレクトリ自体の情報を表示
ls -d

# ファイルの大きい順にソート
ls -S

# 最終更新時刻が新しい順にソート
ls -t
```

```shell
# ディレクトリのみ表示
ls -lad */
ls -la | grep ^d

# ファイル・ディレクトリのサイズを分かりやすく表示
ls -lh

# 最終更新日時順に表示
ls -lt

# 最終更新時刻のスタイルを変更
ls -l --time-style=+'%Y/%m/%d %H:%M:%S'
ls -l --time-style=+'%Y/%m/%d %H:%M'
```

#### ディレクトリの扱い方

各コマンドに共通するが、ディレクトリを指定しない場合、現在いるカレントディレクトリ内を基準(デフォルト)で実行される

```text
# 現在いるカレントディレクトリを示す
./

# 一階層上のディレクトリを示す
../

# 二階層上のディレクトリを示す
../../

# ホームディレクトリを示す ※ ~ だけでもOK
~/
```

▽ ルートディレクトリで `ls -l` を実施したときのサンプル

```text
drwxr-xr-x    2 root     root          1552 Sep  9  2018 bin
drwxr-xr-x    3 root     root         12180 Jan  1  1970 dev
drwxr-xr-x   13 root     root           808 Sep 10  2018 etc
drwxr-xr-x    2 root     root            37 May 25  2017 home
drwxr-xr-x    5 root     root           679 Sep  9  2018 lib
lrwxrwxrwx    1 root     root             3 Aug 19  2018 lib64 -> lib
lrwxrwxrwx    1 root     root            11 Aug 19  2018 linuxrc -> bin/busybox
drwxr-xr-x    2 root     root            37 Jan  9  2017 media
drwxr-xr-x    2 root     root            37 Jan  9  2017 mnt
drwxr-xr-x    2 root     root            37 Jan  9  2017 opt
dr-xr-xr-x   30 root     root             0 Jan  1  1970 proc
drwxr-xr-x    5 root     root           323 Sep 19  2019 root
drwxr-xr-x    3 root     root           120 Apr 16 00:28 run
drwxr-xr-x    2 root     root          1261 Sep 10  2018 sbin
dr-xr-xr-x   11 root     root             0 Jan  1  1970 sys
drwxrwxrwt    4 root     root           143 Jan 30  2020 tmp
drwxr-xr-x   10 root     root           256 Aug 19  2018 usr
drwxr-xr-x    5 root     root           221 Aug 20  2018 var
```

▽ `ls -l` の出力結果の見方

| ファイルの種類 / 許可属性 | ハードリンク数 | 所有者名 / グループ名 | ファイルサイズ(B) | 最終更新日時 | ファイル名 |
| :------------------------ | :------------- | :-------------------- | :---------------- | :----------- | :--------- |
| drwxrwxrwx                | 4              | root root             | 143               | Jan 30 2020  | tmp        |

▽ ファイルの種類 / 許可属性

| ファイルの種類 | 所有ユーザー | グループ | 他ユーザー |
| :------------- | :----------- | :------- | :--------- |
| d              | rwx          | rwx      | rwx        |

▽ ファイルの種類

| 種類 | 略            | 内容                         |
| :--- | :------------ | :--------------------------- |
| d    | directory     | ディレクトリ                 |
| -    | file          | ファイル                     |
| l    | symbolic link | シンボリックリンク           |
| c    | character     | キャラクタ型デバイスファイル |
| b    | block         | ブロック型デバイスファイル   |

▽ 許可属性

| 属性 | 権限番号 | 略      | 内容         |
| :--- | :------- | :------ | :----------- |
| r    | 4        | reading | 読み出し     |
| w    | 2        | write   | 書き込み     |
| x    | 1        | execute | 実行する     |
| -    | 0        | -       | 許可されない |

▽ 表示の色

| 色         | 内容                                                         |
| :--------- | :----------------------------------------------------------- |
| 青         | ディレクトリ                                                 |
| 緑         | 実行可能ファイル(exe,bin,sh等)又は、認識されたデータファイル |
| 水色       | シンボリックリンク                                           |
| 黄色       | ブロック型(キャラクタ型)デバイスファイル                     |
| ピンク     | イメージファイル                                             |
| 赤         | アーカイブ                                                   |
| 赤で黒背景 | リンク切れ                                                   |

▽ 月名の英語表記

| 月   | 英語表記  | 省略形      |
| :--- | :-------- | :---------- |
| 1月  | January   | Jan.        |
| 2月  | February  | Feb.        |
| 3月  | March     | Mar.        |
| 4月  | April     | Apr.        |
| 5月  | May       | May         |
| 6月  | June      | Jun.／June  |
| 7月  | July      | Jul.／July  |
| 8月  | August    | Aug.        |
| 9月  | September | Sep.／Sept. |
| 10月 | October   | Oct.        |
| 11月 | November  | Nov.        |
| 12月 | December  | Dec.        |

### alias

コマンドを別名で登録

```shell
# 登録されているエイリアスを表示
alias

# エイリアスに登録
alias mycommand='command'
```

```shell
# 登録されているエイリアスを削除
unalias mycommand

# 永続的に利用するためには、設定ファイル（例えば.bashrcや.bash_profile）にaliasの定義を追加
echo alias mycommand='command' >> ~/.bashrc
```

```shell
# 現在のディレクトリ以下のディレクトリ構造をtreeコマンドのような形式で表示
alias tree='find . -print | sed -e "s;[^/]*/;|____;g;s;____|; |;g"'
```
