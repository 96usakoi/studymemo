# studymemo
Winに開発環境整える

## 環境整える

### インストールする物
- git
- xampp
- nodist
- node.js
- gulp
- WordPress
- Atom

***
#### nodist
- Nodeのバージョン管理ツール
- 今回 ver4.4.7
- [参照：nodistでNode.jsをバージョン管理](http://qiita.com/satoyan419/items/56e0b5f35912b9374305)


#### gulp
gulpが入ってない場合はインストール
##### グローバルの設定
``` npm install -g gulp ```
-g（グローバル：全体で使えるようにする。-g無しだと今いる階層にインストール）

##### ローカルディレクトリの設定
WordPressのthemesの開発用テーマの中にpackade.jsonがある場合

``` npm install ```

（テーマ名＞node_modulesの中身がインストールされる）

##### gulpの設定

``` gulp/config.default.js ```

修正する箇所
```
proxy: 'http://hsa.localhost/', //自身のローカル環境に合わせて書き換えてください。
```
（人それぞれ開発環境のURLが異なっていても見れるように偽装）

## Gitの使い方
開発ディレクトリ

例）
``` C:\xampp\htdocs ```

MS-DOS起動

``` cmd ```

フォルダ移動

``` cd ***/*** ```

### gitコマンド
クローン

``` git clone URL ```

ブランチ作成、移動

``` git checkout -b *** ```

ブランチ切り替え

``` git checkout ブランチ名 ```

ブランチの確認

``` git branch ```

#### 実際の作業

1. 編集をかけたファイルの追加準備
```
git add . //編集をかけた全ファイル
```
```
git add *** //準備したいファイル名
```

2. 何が準備できたか確認をする
```
git status
```

3. コミットする
```  
git commit -m "メッセージ（英語のほうがよい）"
```

4. プッシュ
```
git push origin master //マスターの場合
```
```
git push origin iori //マスター以外
```

## コーディングルール

srcの中身触る

### FLOCSS
[https://github.com/hiloki/flocss](https://github.com/hiloki/flocss)

CSSのクラス名
- --→属性（カラーとか）
- __→子要素（）
- p→プロジェクト（例：メインビジュアル）
- c→コンポーネント（使いまわせるやつ）
- l→レイアウト

【例】
```
<dl class="c-block">
  <dt class="c-block__h"></dt>
  <dd class="c-block__data">
    <img src="" alt="" class="c-block__img--big">
  </dd>
  <dd class="c-block__data">
    <img src="" alt="" class="c-block__img--small">
  </dd>
</dl>
```

## Atomについて
### パッケージリスト

[参照：packagelist.txt](https://github.com/yat8823jp/atomcy/blob/master/packagelist.txt)

### マークダウンプレビュー
``` Ctrl + Shift + m ```
