node-red-unittest-example
====

Node-REDのユニットテストの基本的な実行方法の例です。  
[公式サイト](https://nodered.org/docs/creating-nodes/first-node#testing-your-node-in-node-red)に記載されていたことを実行して確かめられるようにしました。

## Description

[Node-RED公式サイト](https://nodered.org/docs/creating-nodes/first-node#testing-your-node-in-node-red)にて説明されていたことを試しました。  
masterブランチはプルしたあとにテストがすぐできます。
Node-RED日本ユーザ会のサイトには、ユニットテストの項目は書かれていなかったので、一応邦訳らしきものをつける予定です。

## Requirement

- npm

## Usage

- masterブランチ

 ユニットテストのファイルがついているブランチです。
プルしたあと、フォルダの中に移動し、コマンドプロンプトなどで以下を実行します。
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