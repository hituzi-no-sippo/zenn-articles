---
title: "Neovimメモ 2023年1月26日"
emoji: "🌕"
type: "Idea"
topics: ["neovim"]
published: true
---

この記事を読んでも

- Neovimが画期的に使いやすくなる
- 新しいプラグインを導入できる

はないです。

明記しない限り、nightly (`v0.9.0-dev`)は、
[2023年1月26日のnightly(`v0.9.0-dev-810+gb8288df99`)](https://github.com/neovim/neovim/commit/b8288df99be8df701308167e4b0b497f003f25e9)のことです。

## コミュニティ

### Neovim Conf 2022のアーカイブ

#### Neovim Conf開催したときの開発環境

- Neovim Confの開催日時
  2022年12月9日と10日
- 最新リリース
  [v0.8.1 (2022年11月14日リリース)](https://github.com/neovim/neovim/releases/tag/v0.8.1)です。
  [Neovim v0.8.2(2022年12月30日リリース)](https://github.com/neovim/neovim/releases/tag/v0.8.2)
  の少し前の状態です。
- [lazy.nvim](https://github.com/folke/lazy.nvim)
  人気なプラグインマネージャーのlazy.nvimがまだ広まっていなかった印象があります。
  Neovim Conf後の[2022年12月20日のRedditの投稿](https://www.reddit.com/r/neovim/comments/zqk5ds/lazynvim_a_new_plugin_manager_for_neovim/)で広まった印象があります。
  [issueを古い順](https://github.com/folke/lazy.nvim/issues?q=is%3Aissue+sort%3Acreated-asc+)にすると、1番古いのは12月22日です。

#### 全体

- Day1
  - [Youtube](https://youtu.be/z9SuyhSHOWs)
  - [Twitch](https://www.twitch.tv/videos/1674533770)
- Day2
  - Youtubeは公式のアーカイブを見つけることができませんでした
  - Twitchは途中で放送が切れたせいか、2つに分かれていました
    [Part 1](https://www.twitch.tv/videos/1675449848)
    [Part 2](https://www.twitch.tv/videos/1675788481)

#### プレゼン

- Neovimコア
  - [State of Neovim](https://youtu.be/IFACLbpqRB4) - [justinmk(Justin M. Keyesk)](https://github.com/justinmk)
    Neovimの現状を話しています。
    2014年、初期からのメンテナーの方が発表者です。
    今のNeovimの開発のリーダーという印象を私は持っています。

- プラグイン
  - [vmux: neovim as term multiplexer](https://youtu.be/CxYBBnYsY0Y) - [yazgoo](https://github.com/yazgoo/)
    vim/neovimを端末のマルチプレクサにする[vmux](https://github.com/yazgoo/vmux)の紹介をしています。

- プラグイン開発
  - [Writing Plugins - It's Never Been Easier](https://youtu.be/PdaObkGazoU) - [Dr. David A. Kunz](https://github.com/David-Kunz)
    Luaを使ったNeovimのプラグイン書き方を教えてくれます。
    発表者はNeovimの新機能やプラグインの紹介動画を投稿しています。
    Redditで、紹介動画のスレッドが上がっているのをよく見ます。

- キーマップ
  - [Mapping your way to productivity](https://youtu.be/XyCRvk-VcXU) - [Ben Frain](https://benfrain.com/)
    生産性を高めるマッピングについて話しています。
    [使用しているスライド](https://nv2022.benfrain.com/)

- 他のテキストエディタ
  - [Why I Use Neovim From Within VS Code](https://youtu.be/7ff3GAwSPWg) - [Joe Previte](https://joeprevite.com)
    発表者がVS Code内からNeovimを使用する理由を説明しています。
    [使用しているスライド](https://neovim-within-vscode.vercel.app)

発表者のプロフィールは
[Neovim Confの公式サイト](https://www.neovimconf.live)を参考してください。

**発表内容などのタイムテーブル**

- [Day 1](https://tomdeneire.medium.com/neovim-conference-2022-day-1-b65099ce3391)
- [Day 2](https://tomdeneire.medium.com/neovim-conference-2022-day-2-24820d8226e)

### Neovimのニュースレター "This Week in Neovim" がなくなるかもしれない

["This Week in Neovim"](https://this-week-in-neovim.org)(以後、TWiN)は、1週間の

- Neovim Coreの変更内容
- 新規プラグイン
- 既存プラグインのアップデート内容

などを日本時間だと毎週月曜日の夕方あたりに投稿しています。

TWiNを立ち上げたphaazon(Dimitri Sabadie)は

- [TWiNを維持することに大変疲れている](https://phaazon.net/blog/editors-in-2022#:~:text=I%E2%80%99m%20really%20tired%20of%20maintaining%20TWiN.)
- [人々は読むだけで、TWiNに投稿して協力してくれないのにうんざりしている](https://phaazon.net/blog/editors-in-2022#:~:text=So%2C%20people%20started%20to%20mention%20that%20I%20should%20slow%20down%20or%20I%20will%20burn%20out.%20And%20I%E2%80%99m%20honestly%20pretty%20fed%20up%20with%20this%20read%2Donly%20relationship%3A%20people%20consume%20/%20read%3B%20they%20rarely%20contribute%2C%20even%20when%20they%20could%20contribute%20their%20own%20update%20for%20their%20own%20plugins!)
- [TWiNへ投稿して、TWiN作成の協力をして欲しい](https://phaazon.net/blog/editors-in-2022#:~:text=What%20I%20need%20is%C2%A0contributions.)

と[ブログ記事](https://phaazon.net/blog/editors-in-2022)で書きました。

[プラグイン作者がTWiNへ投稿して](https://phaazon.net/blog/editors-in-2022#:~:text=while%20what%20I%20thought%20would%20happen%20was%20that%20many%20plugin%20authors%20would%20contribute%20once%20every%20two%20months%20a%20very%20small%20text%20to%20explain%20their%20new%20plugins%20/%20change.)、その投稿を組み合わせてTWiNにする。
これがphaazonの理想のように私は印象を持ちました。

コミュニティが協力して、TWiNを作成し、TWiNをコミュニティのものにしたいんだと感じました。
TWiNをコミュニティのものにして、コミュニティ主導で管理して、phaazonがいなくてもTWiNを運用するのが目標なんだと思います。
phaazonの個人ブログではなく、Zennのように複数の人が投稿するものにTWiNをしたかったんだと思います。

現状のphaazon一人が頑張って殆ど作成するのは、phaazonの理想とはかけ離れています。
TWiNを公開し、続けていけば、読んだ人が投稿してくれると考えていたようです。
しかし、投稿してくれる人は少なかったようです。

投稿しやすいように大きなリファクタリングをして、Redditに投稿しても、[TWiNへの投稿は増えなかったようです。](https://phaazon.net/blog/editors-in-2022#:~:text=And%20even%20with%20the%20exposure%20of%20TWiN%2C%20people%20still%20do%20not%20contribute.%20Even%20after%20the%20big%20refactoring%20to%20ease%20contribution%20I%20announced%20on%20Reddit.)
この[Redditの投稿](https://www.reddit.com/r/neovim/comments/yeo89j/twin_gets_a_new_collaboration_process_to_ease/)でphaazonは
"プラグイン作者がTWiNを考え、自分たちのニュースを自分たちで提供するようにしたかった" の様なことをコメントしています。

[TWiNへの投稿方法はREADMEに記載しています。](https://github.com/phaazon/this-week-in-neovim-contents#how-to-contribute)

#### 記事への反応

この記事への反応は大いにありました。
TWiNのことだけではなく、次の2点についても書いているからだと思います。

- phaazonが考えている[Neovimのプラグインの問題点](https://phaazon.net/blog/editors-in-2022#:~:text=Why%20I%20think%20it%E2%80%99s%20bad)
- Rust製の[Helix](https://helix-editor.com)とNeovimの比較

Redditのスレッド

- [Neovim](https://www.reddit.com/r/neovim/comments/1007z1z/my_thoughts_about_editors_in_2022/)
- [Programming](https://www.reddit.com/r/programming/comments/1007yq5/my_thoughts_about_editors_in_2022/)

この記事への反応の効果で、[行き詰まっていた、NeovimのコアチームとのTWiNプロジェクトの話し合い](https://phaazon.net/blog/editors-in-2022#:~:text=I%20discussed%20the%20project%20with%20some%20people%20from%20the%20Neovim%20core%20team%2C%20and%20I%E2%80%99m%20a%20bit%20stuck.)が、 良い方向へ進めばいいと願っています。

私も[ブログ記事](https://phaazon.net/blog/editors-in-2022)を読みましたが、多分1番多くのNeovimプラグインを見てきた人が考えているNeovimのプラグインの問題点は面白く、考えさせられました。

#### mind.nvim と hop.nvim の今後について

ブログ記事では、phaazonが開発している次の2つのプラグインの開発方針についても書いています。

- [mind.nvim](https://github.com/phaazon/mind.nvim)
  メモやタスク、考えを整理しやすくするプラグイン
  (使ってないので合っているのか分かりません)
  Neovimのプラグインではなくして、Neovim以外のエディタでも使えるようにする。
- [Hop.nvim](https://github.com/phaazon/hop.nvim)
  指定した文字へ高速で移動するプラグイン
  活発な活動はしない。暇がないため。
  メンテナンスとバグ修正を続ける予定です。

### プラグインのメタデータ仕様のドラフトの開発は止まっている

[The Neovim package specification](https://github.com/nvim-lua/nvim-package-specification)

2022年3月以降、コミットがありません。
[メインコントリビュータがNeovimの開発から離れたせいかもしれません。](https://www.reddit.com/r/neovim/comments/vd0vim/anyone_know_whats_going_on_with_mjldach/)

## Neovim Core

### Neoevimがv1.0を宣言するための条件リスト

[Path to version 1.0 #20451](https://github.com/neovim/neovim/issues/20451)

リンク先に書かれていますが、"Path to version 1.0" と "[Roadmap](https://neovim.io/roadmap/)" は違います。

["justinmk" がRedditで投稿したコメントを読み](https://www.reddit.com/r/neovim/comments/zm24r1/comment/j08wd7g)、
自分なりに日本語に解釈したところ、次の通りになりました。

- Path to version 1.0 :: version 1.0 になるために必要な条件のリスト
- Roadmap :: Neovimの開発の方向性を説明するためのテーマ一覧。
             テーマはいつでも変更・中止される。

### Vim9ScriptをLuaにするトランスパイラ

[トランスパイラのvim9jit](https://github.com/tjdevries/vim9jit)

[開発者による紹介動画](https://youtu.be/zPQSST-M3fM)

Rustで実装しています。
次の2つのマージされたプルリクエストで使用されています。

- [vim9script->lua: generated version of ccomplete.vim](https://github.com/neovim/neovim/pull/21623)
- [dist: add cfilter.vim -> lua](https://github.com/neovim/neovim/pull/21662)
- [vim9Jitで作成されたファイル](https://github.com/neovim/neovim/blob/master/runtime/lua/_vim9script.lua)

[これを使えば、全てではないですがVim9ScriptのプラグインをNeovimに移植できるようです。](
https://www.reddit.com/r/neovim/comments/109xyf3/comment/j41chcr)

### Neovimコアへの追加機能と類似プラグイン

特定のプラグインと同じような機能をNeovimコアに追加、もしくは開発中みたいです。
プラグインの全ての機能ではなく、一部の機能だけを追加する場合もあります。

[justinmkがRedditでコメントしていました。](https://www.reddit.com/r/neovim/comments/101omgs/comment/j2p62tq)
返答しているプラグインの選択理由は分かりませんでした。

#### 実装済

- [visual modeで `*` と `#` をすると選択した範囲で検索する](https://github.com/neovim/neovim/pull/18538)
  [v0.8.0](https://github.com/neovim/neovim/releases/tag/v0.8.0)から使えます
  類似するプラグイン: [vim-asterisk](https://github.com/vim-scripts/vim-asterisk)
- [editorconfigを元にファイルを修正する](https://github.com/neovim/neovim/pull/21633)
  nightlyでしか使えません。
  [editorconfig.nvim](https://github.com/gpanders/editorconfig.nvim)をluaで書き直したもの
- [読みこむファイルが信頼できるかをユーザに問い合わせる(`vim.secure.read()`)](https://github.com/neovim/neovim/pull/20956)
  nightlyでしか使えません。
  類似するプラグイン: [vim-localvimrc](https://github.com/embear/vim-localvimrc)

#### 開発中

- [プロジェクトに関するディレクトリを追加する](https://github.com/neovim/neovim/issues/8610)
  類似する機能を持つプラグイン: [vim-rooter](https://github.com/airblade/vim-rooter)
- [ウィンドウを閉じずにバッファを削除する](https://github.com/neovim/neovim/issues/2434)
  類似する機能を持つプラグイン: [vim-bbye](https://github.com/moll/vim-bbye)
- [ファイルを開く時、そのファイルの最後のカーソル位置へ移動する](https://github.com/neovim/neovim/issues/16339)
  類似する機能を持つプラグイン: [nvim-lastplace](https://github.com/ethanholz/nvim-lastplace)
- 便利なマッピングを追加する
  "improved defaults" で動いていると書いていますが、発見できませんでした。
  類似するプラグイン: [vim-unimpaired](https://github.com/tpope/vim-unimpaired)

#### Neovimコアに追加しないプラグイン機能と理由

- インデントの表示を変更する
  見た目は変わるが役にたつものではなく、表示速度が遅くなるため
  類似するプラグイン: [indent-blankline.nvim](https://github.com/lukas-reineke/indent-blankline.nvim)
- オートペア (`[` を入力したら `]` が自動で挿入される)
  オートペアのプラグインがあっても、実際の仕事が減るのを見たことない
  類似するプラグイン: [auto-pairs](https://github.com/jiangmiao/auto-pairs)

### オプションのデフォルト値の変更案

オプションの値に関するアンケートがRedditであり、
227人の回答が集められました。

デフォルトではない値が80%以上のオプションは、
その値をデフォルトにしようという話が進まれており、
回答の80%以上である次のオプションのデフォルト値が変更される可能性があります。

- termguicolors: true
- number: true
- ignorecase: true
- smartcase: true
- expandtab: true

[アンケート結果を話題にしているissue](https://github.com/neovim/neovim/issues/21342)と[デフォルト変更に関するissue](https://github.com/neovim/neovim/issues/19354)
では次のようなコメントがあります。

- termguicolors: true
  [検討する価値はあり。ただ、いくつか作業が必要になる可能性あり](https://github.com/neovim/neovim/issues/21342#issuecomment-1343296366)
- number: true
  - [単なる人の好み](https://github.com/neovim/neovim/issues/21342#issuecomment-1343240405)
  - [ヘルプドキュメントの改善が必要な目じるし。
     `number` のヘルプの先頭に、行番号を表示する `ruler` オプションと `g ctrl-g` の説明を追加する。デフォルト値の変更は必要ない。](https://github.com/neovim/neovim/issues/21342#issuecomment-1343296366)
- ignorecase & smartcase: true
  - [大・小文字を無視するのはユーザが最も自然に思えない、驚き最小の原則に反するため反対です。
     検索を行うgrepやlessなどの検索を行うツールも、デフォルトで大文字小文字を無視するわけではありません。](https://github.com/neovim/neovim/issues/21342#issuecomment-1343240405)
  - [議論がもっと必要](https://github.com/neovim/neovim/issues/19354#issuecomment-1185492221)
- expandtab: true
  [filetypeプラグインで設定されるから、変更する意味が殆どありません](https://github.com/neovim/neovim/issues/21342#issuecomment-1343240405)

テストやドキュメント生成、テキストの整列などの沢山の便利ツールが入っている[mini.nvim](https://github.com/echasnovski/mini.nvim)の開発者が、アンケートの作成者です。

- [アンケート結果に対するRedditのスレッド](https://www.reddit.com/r/neovim/comments/zg44mm/results_of_neovim_builtin_options_survey_more_in/)

### 画面左の行番号部分をカスタマイズできるようになった

[画面左の行番号部分をカスタマイズするオプション `statuscolumn` が実装されました。](https://github.com/neovim/neovim/pull/20621)

- [機能内容を説明する動画があるRedditのスレッド](https://www.reddit.com/r/neovim/comments/107k0cv/new_feature_statuscolumn_merged/)
- [`:help statuscolumn`](https://neovim.io/doc/user/options.html#'statuscolumn')

2023年1月26日現在、 nightlyにしかない機能です。

これにより、ステータスラインの様に行番号部分を自分好みに変更できます。

`statuscolumn` 用の[プラグイン](https://github.com/luukvbaal/statuscol.nvim)もあります。
プラグインの開発者は `statuscolumn` のPRを作成した人です。

### EditorConfigの対応が追加された

[editorconfig.nvim](https://github.com/gpanders/editorconfig.nvim)のようなプラグインがなくても、[標準でEditorConfigが適応されるようになりました。](https://github.com/neovim/neovim/pull/21633)

2023年1月26日現在、 nightlyにしかない機能です。

editorconfig.nvimの開発者が、PRの作成者です。

- [EditorConfigに関するLuaファイル](https://github.com/neovim/neovim/blob/master/runtime/lua/editorconfig.lua)
- [`:help editorconfig`](https://neovim.io/doc/user/editorconfig.html)

`.editorconfig` があると、自動でEditorConfigは適用されます。

次のようになります。

```shell
# 行末までの空白を削除する機能を有効にします
$ echo -e "[*.txt]\ntrim_trailing_whitespace = true" > .editorconfig
# 行末までの空白があるファイルを作成します
$ echo "trim_trailing_whitespace   " > test.txt
$ cat --show-ends test.txt  # 行末が `$` で表示されます
trim_trailing_whitespace   $

# 書き込みをして、editorconfigを動かし、行末の空白を削除します。
$ nvim --headless --clean -c "wq" test.txt
"test.txt" "test.txt" 1L, 25B written

$ cat --show-ends test.txt  # 行末が `$` で表示されます
trim_trailing_whitespace$   # 行末の空白が削除されている
```

見やすくするため、一部出力変更しています。

`$ nvim --headless --clean -c "wq" test.txt` ですが、
最後に改行がないので、

```shell
$ nvim --headless --clean -c "wq" test.txt
"test.txt" "test.txt" 1L, 28B written$ cat --show-ends test.txt
```

になる可能性もあります。
しかし、見にくいので上のコンソール結果では改行しています。
この後もコンソール結果を出力しているものでは、同じことをしています。

**`nvim --clean` について**

`--clean` で、設定やプラグインは読みこまず、新規インストール時のNeovimと極力同じ環境にします。
editorconfigはビルドインプラグインなので、 `-u NONE` にはしません。
`-u NONE` にすると、editorconfigが動きません。

[`:Man` コマンドもビルドインプラグイン](https://github.com/neovim/neovim/blob/master/runtime/lua/man.lua)なので、 `-u NONE` にするとできません。
ヘルプファイル時に目次を表示する、 `gO` も動きません。

#### `.editorconfig` とカレントディレクトリ

`.editorconfig` は、カレントディレクトリになくても適用されます。

```shell
$ echo -e "[*.txt]\ntrim_trailing_whitespace = true" > .editorconfig
$ mkdir sub
$ cd sub # ディレクトリを移動する

$ echo "trim_trailing_whitespace   " > test.txt
$ cat --show-ends test.txt  # 行末が `$` で表示されます
trim_trailing_whitespace   $

$ nvim --headless --clean -c "wq" test.txt
"test.txt" "test.txt" 1L, 25B written

$ cat --show-ends test.txt  # 行末が `$` で表示されます
trim_trailing_whitespace$   # 行末の空白が削除されている
```

`.editorconfig` がカレントディレクトリにあっても、 `.editorconfig` があるディレクトリ配下にないファイルには適応されません。

```shell
$ mkdir sub
# サブディレクトリに `.editorconfig` を作成する
$ echo -e "[*.txt]\ntrim_trailing_whitespace = true" > sub/.editorconfig

$ echo "trim_trailing_whitespace   " > test.txt
$ cat --show-ends test.txt  # 行末が `$` で表示されます
trim_trailing_whitespace   $

$ nvim --headless --clean -c "wq" test.txt
"test.txt" "test.txt" 1L, 25B written

# `.editorconfig` が適用されていないので、行末までの空白は削除されない
$ cat --show-ends test.txt   # 行末が `$` で表示されます
trim_trailing_whitespace   $ # 行末の空白が削除されています
```

#### `.editorconfig` の内容を変更したら

Neovim内で `.editorconfig` の内容を変更しても、すでに開いているバッファには適用されません。
`edit` コマンドを使用して開き直すと、変更後の設定が適用されます。

#### `insert_final_newline = false` の動作について

[変更される可能性があります。](https://github.com/neovim/neovim/issues/21648)

2023年1月26日現在、nightlyでは、 `insert_final_newline = false` で最後に改行がある場合、改行を削除します。

なので、次のようになります。

```shell
$ echo -e "[*.txt]\ninsert_final_newline = false" > .editorconfig
$ echo "insert_final_newline = false" > insert.txt  # 改行あり
$ echo -n "insert_final_newline = false" > no.txt   # 改行なし

$ nvim --headless --clean -c "wq" insert.txt
"insert.txt" "insert.txt" [noeol] 1L, 28B written
$ nvim --headless --clean -c "wq" no.txt
"no.txt" "no.txt" [noeol] 1L, 28B written

$ diff insert.txt no.txt  # 差分はなし
```

これは[editorconfig-vim](https://github.com/editorconfig/editorconfig-vim)と動作が違います。
editorconfig-vimの場合、`insert_final_newline = false` で最後に改行がある場合、何もしません。改行を削除しません。

[仕様](https://editorconfig-specification.readthedocs.io/#supported-pairs)の書き方が悪く、[改行を削除するのが正しいのか、改行をそのままにするのが正しいのか、editorconfig公式でも決まっていません。](https://github.com/editorconfig/editorconfig/issues/475)
改行をそのままにするのが正しいなら、Neovimの標準のeditorconfigの動作も変更になります。

#### `editorconfig` の値を取得する

[editorconfigの "properties" テーブルにコールバック関数を追加すれば](https://neovim.io/doc/user/editorconfig.html#editorconfig-custom-properties)、編集しているファイルに対する `editorconfig` の値を取得できます。

**editorconfig.lua**

```lua
require('editorconfig').properties.trim_trailing_whitespace = function(bufnr, val, opts)
  print("バッファ番号: " .. bufnr)
  -- プロパティの値が `properties.trim_trailing_whitespace` の場合、
  -- `trim_trailing_whitespace` の値を参照します。
  print("プロパティの値: " .. val)
  print("編集中のファイルに適用されているeditorconfigの値全て")
  vim.pretty_print(opts)
end
```

**.editorconfig**

```ini
[*.txt]
trim_trailing_whitespace = true
```

**`nvim --headless --clean -u editorconfig.lua test.txt -c quit` の結果**

```
バッファ番号: 1
プロパティの値: true
編集中のファイルに適用されているeditorconfigの値全て
{
  trim_trailing_whitespace = "true"
}
```

プロパティの値がないとコールバック関数は実行されません。
そのため、 次のように編集しているファイルに対して、`trim_trailing_whitespace` が設定されていないとコールバック関数は実行されません。

**上で設定したコールバック関数が実行されない `.editorconfig` の例**

```ini
[*.txt]
insert_final_newline = false
```

```ini
[*.txt]
insert_final_newline = false

[*.adoc]
trim_trailing_whitespace = true
```

##### editorconfigにはないプロパティも設定できます

**editorconfig.lua**

```lua
require('editorconfig').properties.apple = function(bufnr, val, opts)
  print("バッファ番号: " .. bufnr)
  print("プロパティの値: " .. val)
  print("編集中のファイルに適用されているeditorconfigの値全て")
  vim.pretty_print(opts)
end
```

**.editorconfig**

```ini
[*.txt]
trim_trailing_whitespace = true
apple = banana
```

**`nvim --headless --clean -u editorconfig.lua test.txt -c quit` の結果**

```
バッファ番号: 1
プロパティの値: banana
編集中のファイルに適用されているeditorconfigの値全て
{
  apple = "banana",
  trim_trailing_whitespace = "true"
}
```

##### optsには編集中のファイルのみに適用されている値が入ります

**editorconfig.lua**

```lua
require('editorconfig').properties.format = function(bufnr, val, opts)
  print("バッファ番号: " .. bufnr)
  print("プロパティの値: " .. val)
  print("編集中のファイルに適用されているeditorconfigの値全て")
  vim.pretty_print(opts)
end
```

**.editorconfig**

```ini
root = true

[*]
end_of_line = lf
charset = utf-8

[*.txt]
trim_trailing_whitespace = true
format = editorconfig-checker

[*.norg]
trim_trailing_whitespace = true
insert_final_newline = true
indent_style = tab
max_line_length = 80

[*.dj]
trim_trailing_whitespace = true
insert_final_newline = true
indent_style = space
indent_size = 2
max_line_length = 80
```

**`nvim --headless --clean -u editorconfig.lua test.txt -c quit` の結果**

```
バッファ番号: 1
プロパティの値: editorconfig-checker
編集中のファイルに適用されているeditorconfigの値全て
{
  charset = "utf-8",
  end_of_line = "lf",
  format = "editorconfig-checker",
  root = true,
  trim_trailing_whitespace = "true"
}
```

##### プロパティが格納されている引数の値は文字列です

**editorconfig.lua**

```lua
require('editorconfig').properties.boolean = function(bufnr, val, opts)
  print("バッファ番号: " .. bufnr)
  print("プロパティの値: " .. val)
  print("編集中のファイルに適用されているeditorconfigの値全て")
  vim.pretty_print(opts)

  print("プロパティの値の引数は文字列に変換されます")
  print("引数のbufnrの型は" .. type(bufnr))
  print("引数のvalの型は" .. type(val))
  print("引数のopts.booleanの型は" .. type(opts.boolean))

  if val then
    print("`val` は文字列になるので、プロパティの値が `false` の場合でも、" ..
          "`if val then some() end` の `some()` は実行されます")
  end
end
```

**.editorconfig**

```ini
[*.txt]
trim_trailing_whitespace = true
boolean = false
number = 1
string = str
space = no quote
underscore = no_quote
key = no-quote
single_quote = 'apple'
double_quote = "apple"
japanese = 日本語
array = {1,2,3}
array_string = "{1,2,3}"
dict = {a = 1}
dict_string = "{a = 1, b = 2}"
key-name = kebab
```

**`nvim --headless --clean -u editorconfig.lua test.txt -c quit` の結果**

```
バッファ番号: 1
プロパティの値: false
編集中のファイルに適用されているeditorconfigの値全て
{
  array = "{1,2,3}",
  array_string = '"{1,2,3}"',
  boolean = "false",
  dict = "{a = 1}",
  dict_string = '"{a = 1, b = 2}"',
  double_quote = '"apple"',
  japanese = "日本語",
  key = "no-quote",
  ["key-name"] = "kebab",
  number = "1",
  single_quote = "'apple'",
  space = "no quote",
  string = "str",
  trim_trailing_whitespace = "true",
  underscore = "no_quote"
}
プロパティの値の引数は文字列に変換されます
引数のbufnrの型はnumber
引数のvalの型はstring
引数のopts.booleanの型はstring
`val` は文字列になるので、プロパティの値が `false` の場合、`if val then some() end` の `some()` は実行されます
```

### ディレクトリを作成する write の `++p` フラグ

`:write ++p sub/apple/banana.txt` コマンドを実行した際、 `sub/apple` ディレクトリがなくても、ファイルは作成されます。
`++p` フラグのおかげで、 `sub/apple` ディレクトリを作成してくれるからです。

- [実装されたPR](https://github.com/neovim/neovim/issues/19884)
- [`:help ++p`](https://neovim.io/doc/user/editing.html#%2B%2Bp)

2023年1月27日現在、 nightlyにしかない機能です。

```shell
$ ls sub sub/apple  # ディレクトリがないことを確認する
ls: cannot access 'sub': No such file or directory
ls: cannot access 'sub/apple': No such file or directory

# `sub/apple` ディレクトリがないためエラーになる
$ nvim --headless -u NONE -c "write sub/apple/banana.txt" -c "quit"
"sub/apple/banana.txt"
Error detected while processing command line:
E212: Can't open file for writing: no such file or directory
$ file sub/apple/banana.txt
sub/apple/banana.txt: cannot open `sub/apple/banana.txt' (No such file or directory)
# ファイルは作成されていない

# `++p` フラグがあるため、 `sub/apple` ディレクトリを作成してくれる
$ nvim --headless -u NONE -c "write ++p sub/apple/banana.txt" -c "quit"
"sub/apple/banana.txt" "sub/apple/banana.txt" [New] 0L, 0B written
$ file sub/apple/banana.txt
sub/apple/banana.txt: empty # ファイルは作成されている
```

## 設定

### TJとThePrimeagenのNeovim設定構築動画

Neovim Conf 2022の司会者2人の設定構築動画が投稿されました。

LSPの設定もしています。
パッケージマネージャは[Packer.nvim](https://github.com/wbthomason/packer.nvim)を使用しています。
[Lazy.nvim](https://github.com/folke/lazy.nvim)ではありません。

- [TJ DeVries](https://youtu.be/stqUbv-5u2s)
  [Kickstarter.nvim](https://github.com/nvim-lua/kickstart.nvim)を使用しています。
- [ThePrimeagen](https://youtu.be/w7i4amO_zaE)
  [動画で構築した設定のリポジトリ](https://github.com/ThePrimeagen/init.lua)

[Migrating from Packer.nvim to Lazy.nvim](https://youtu.be/aqlxqpHs-aQ)
などを参考にして、Packer.nvimからLazy.nvimに移行してください。

### パッケージマネージャーのLazy.nvim専用のスタータキット LazyVim v1リリース

[LazyVim](https://lazyvim.github.io)

パッケージマネージャー([Lazy.nvim](https://github.com/folke/lazy.nvim))と開発者が同じです。

Redditのスレッドで開発者が次のようなコメントをしています

- [Lazy.nvimのために作られたのが、LunarvimやAstroNvimなどとの主な違い](https://www.reddit.com/r/neovim/comments/10gyw6c/comment/j56pxao)
- [lazy.nvimの便利な使い方を得られるかもしれないので、LazyVimを使わなくても、設定内容を見てみるといいよ](https://www.reddit.com/r/neovim/comments/10gyw6c/comment/j55eay0/)
- [GitHub Sponsorsなどの寄付は必要ないよ](https://www.reddit.com/r/neovim/comments/10gyw6c/comment/j57cnkd/?utm_source=share&utm_medium=web2x&context=3)

---

LazyVimも含め、次のような設定済みのNeovim設定の名称が分かりません。
上ではスタータキットと書いていますが、合っている可能性低いです。

- [nvim-lua/kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim)
- [nvim-basic-ide](https://github.com/LunarVim/nvim-basic-ide)
- [Lunarvim](https://www.lunarvim.org/)
- [AstroNvim](https://astronvim.github.io/)
- [NvChad](https://nvchad.github.io/)

## プラグイン

### ドキュメント生成・自動リリースがあるプラグインテンプレート

[Neovim plugin boilerplate](https://github.com/shortcuts/neovim-plugin-boilerplate)

**特徴**

- ドキュメント生成
- 自動リリース
- テスト
- フォーマットチェック
- リンター(luacheck)はなし

[ドキュメント生成と自動リリースのGitHub Actionsを参考にしたRedditのスレッド](https://www.reddit.com/r/neovim/comments/103d9on/releases_docs_tests_for_plugins/)

### ターミナルバッファの操作を改善するプラグイン

[term-edit.nvim](https://github.com/chomosuke/term-edit.nvim)

ノーマルモードのカーソル位置を、ターミナルモードのカーソル位置にするプラグインです。

現在のnightly、ターミナルモードとノーマルモードでカーソル位置は共有されません。

そのため次のようになります。 `|` がカーソル位置です。

1. ターミナルモードで `donut` の後にカーソルを移動する
   `apple banana donut|`
1. ノーマルモードにして `banana` の後にカーソルを移動する
   `apple banana|donut`
1. ターミナルモードにすると、1の `donut` の後がカーソルの位置になる
   `apple banana donut|`
1. ターミナルモードで ` cake`を入力する
   `apple banana donut cake|`

term-edit.nvimを使うと、次のように変更されます。

1. ターミナルモードで `donut` の後にカーソルを移動する
   `apple banana donut|`
1. ノーマルモードにして `banana` の後にカーソルを移動する
   `apple banana|donut`
1. `i` でターミナルモードにすると、`banana` の後がカーソルの位置になる。
   ノーマルモードのカーソル位置が、そのままターミナルモードのカーソル位置になる
   `apple banana|donut`
1. ターミナルモードで ` cake`を入力する
   `apple banana cake|donut`

Neovimに標準搭載されるかもしれないです。
["justinmk" がRedditで "間違いなくNeovimのコアに欲しいもの" とコメントしています。](https://www.reddit.com/r/neovim/comments/10h01dw/comment/j5iubpu)

### Open AIを使用するプラグイン

- [ChatGPT.nvim](https://github.com/jackMort/ChatGPT.nvim)
  [紹介動画](https://youtu.be/sHXQczQHbDk)
- [Neural](https://github.com/dense-analysis/neural)

2つの違いは分かりませんでした。

## ドキュメント

### Neovim内でv0.8からv0.9の変更点を見る

[`:help news`](https://neovim.io/doc/user/news.html)をやると、v0.8かv0.9までの変更点が見れます。
破壊的変更や新機能で章が分かれてて、見やすいです

nightlyでしかできません。 `v0.8.2` ではできませんでした。

### nvim-lua-guideがアーカイブになった

[nvim-lua-guide](https://github.com/nanotee/nvim-lua-guide)をベースとして、[大幅に作り直したものがヘルプファイルに追加されたからです。](https://github.com/neovim/neovim/pull/21137#issue-1456918552)

[`:help lua-guide`](https://neovim.io/doc/user/lua-guide.html)

nvim-lua-guideの和訳をしている[nvim-lua-guide-ja](https://github.com/willelz/nvim-lua-guide-ja/blob/master/README.ja.md)も、今後は更新されないと思います。

## その他

### Neovimのプラグイン&カラースキームを探せるWebサイト

- [NeoLand](https://neoland.dev/)
  - プラグインとカラースキームが分かれている
- [neovimcraft](https://neovimcraft.com)
  - プラグインとカラースキームは分かれていない
  - [ターミナルで検索できる](https://github.com/neurosnap/nvim.sh)
  - リポジトリにある[jsonファイル](https://github.com/neurosnap/neovimcraft/blob/main/data/resources.json)に書かれているプラグインを表示している
    [GitHub Actionsを使用して、自動で追加・変更している](https://github.com/neurosnap/neovimcraft/pull/224)
- [vimcolorschemes](https://vimcolorschemes.com)
  - プレビュー付きでカラースキーム一覧が見れます
  - 2023年1月26日現在、検索機能は使えません。[バグ修正中らしいです。](https://github.com/vimcolorschemes/vimcolorschemes/issues/833)

### スターかフォークの多さ順に並べる検索サイト

[Neovimmm](https://tomdeneire.github.io/neovimmm/)

Neovimに関するリポジトリをスターかフォークの多さ順に表示します。

プラグイン専門ではありません。
そのため、Neovim自体やfzf、awesome-neovim、dotfilesも含まれます。

検索もありますが、こちらはスターかフォークの多さ順に並びません。
並び順も分かりません。

### ローカル内のカラースキームのプレビューを見れるプラグイン

- [telescope.nvim](https://github.com/nvim-telescope/telescope.nvim/issues/1961)
- [colorscheme-preview.vim](https://github.com/mnishz/colorscheme-preview.vim)

### Neovim使用者が使っているターミナルエミュレータ

[Kittyとwezの比率が予想より大きかったです。](https://neovim.discourse.group/t/poll-which-terminal-emulator-do-you-use/2319)
