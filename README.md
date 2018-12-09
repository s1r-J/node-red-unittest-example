node-red-unittest-example
====

Node-REDのユニットテスト(単体テスト)の基本的な実行方法の例です。  
[公式サイト](https://nodered.org/docs/creating-nodes/first-node#testing-your-node-in-node-red)に記載されていたことを実行して確かめられるようにしました。（公式サイトはコードが微妙に間違っていて、そのままだと実行できない。）

ユニットテストの作成方法・実行方法は、[Qiita](https://qiita.com/s1r/items/11f1f1821d223bb2b61d)に記載しました。

## Description

[Node-RED公式サイト](https://nodered.org/docs/creating-nodes/first-node#testing-your-node-in-node-red)にて説明されていたことを試しました。なのでソースコードの中身自体は、先述のサイトからおおよそコピペしました。
ただし、公式サイトのコードが微妙に間違っていて、そのままだと実行できないため、そのへんを直してあります。

masterブランチはプルしたあと、mochaがインストールされていればすぐにテストできます。

また、[Node-RED日本ユーザ会のサイト](https://nodered.jp/docs/creating-nodes/first-node)には、ユニットテストの項目は書かれていなかったので、一応邦訳らしきものを[Qiita](https://qiita.com/s1r/items/11f1f1821d223bb2b61d)につけました。

## Requirement

- npm
- [mocha](https://www.npmjs.com/package/mocha)

## Usage

### ユニットテストの作成方法

[Qiita](https://qiita.com/s1r/items/11f1f1821d223bb2b61d)に記載したので、そちらを参照してください。

### ユニットテストの実行方法（プルしてすぐに実行したいなら）

- masterブランチ

 ユニットテストのファイルがついているブランチです。
 
 プルしたあと、フォルダの中に移動し、コマンドプロンプトなどで以下を実行します。
 <details><summary>テストの実施には前述のmochaが必要です</summary>
 <p>
    インストール方法は以下のとおりです。
     
    ```
     npm i -g mocha
    ```
 </p>
 </details> 
 
 ```
 npm test
 ```

 すると、以下のように表示され、テストが通過したことがわかります。
 ```
 > node-red-contrib-example-lower-case@1.0.0 test \path\node-red-contrib-example-lower-case
 > mocha test/lower-case_spec.js

   lower-case Node
     √ should be loaded
     √ should make payload lower case

   2 passing (45ms)
 ```

- beforeブランチ

 ユニットテストのファイルが無い状態のブランチです。ノードを作成し終わって、これからテストをするぞ！という状況です。
ここからユニットテストを作成してmasterブランチのようにするというものです。

## Author

[s1r-J](https://github.com/s1r-J)