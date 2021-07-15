# React cognito認証写経

## はじめに

Reactでcognito認証をするサンプルです。以下サイトを参考に、サンプルを作りました。


参考サイト
https://qiita.com/saki-engineering/items/b327f93fe7f027913bd7


## ローカル環境での動かし方

### 前提条件

1. 以下ソフトウェアがインストールされていること
  * node.js(v14.16.0以上)
  * npm(6.14.11以上)
2. AWS congnitoでユーザプールを作成する
3. 2.に以下の認証フローを持つアプリクライアントを追加する
  * ALLOW_USER_SRP_AUTH
  * ALLOW_REFRESH_TOKEN_AUTH

### 動かし方(初回)

```shell
cd <本リポジトリをcloneした場所>

cp .env.template .env.local
# .env.localに必須項目を記入する
vim .env.local

npm ci
# ブラウザでlocalhost:3000が自動的に開かれる
npm start
```

### 動かし方(2回目以降)

```shell
cd <本リポジトリをcloneした場所>

# ブラウザでlocalhost:3000が自動的に開かれる
npm start
```