## vimの基本操作を振り返る演習

vimの勉強を最近始めた。「実践vim」を読んでいる時に「そんなことできるのか！」と感動した操作方法をまとめる。演習問題も書いているけれど、主に自分があとで読み返すようなので、雑です

### テキスト列の変更

- Ctrl+v, jje: ビジュアルモード
- c: 挿入モード
- componets: 挿入
- <Esc>

感動したポイントとしては、最後に<Esc>を押した時に挿入した内容が全て反映される瞬間

演習:
上記のテキスト操作を使用しながら以下の3行に対して行末に;を入れる

```javascript
var foo = 1
var bar = 'a'
var foobar = foo + bar
```

### テキスト検索

- /text: textで検索をかける
- n: 次の検索結果に移動する
- N: 前の検索結果に移動する

#### 演習
以下のテキストで`var`を検索して、次前の移動を行う

```javascript
var foo = 1
var bar = 'a'
var foobar = foo + bar
```

### 行コピーを行う

- yyp: これで行コピー

### vim画面からシェルプログラムを実行する

- :!ls: `ls`コマンドが実行されたことになる
- :shell : シェルセッションを開始してexitするとvimに戻ってくる

#### 演習

- vimを開く
- :shellでシェルを開始してコマンドを実行
- exitでvimに戻ってくる

### 置換

- :/s/既にあるテキスト/置換するテキスト: テキストを置換

#### 演習
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

のLoremの部分をLORANDに変える

