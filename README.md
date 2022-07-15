# SPA practice(2022/04-2022/07)
## 概要
Docker環境でReact,Laravelを用いてSPA開発することをゴールとする。
</br>Docker環境構築は以下を使用
</br>https://github.com/ucan-lab/docker-laravel

## コンテナ構成

```bash
├── app
├── web
└── db
```

### app コンテナ

- Base image
  - [php](https://hub.docker.com/_/php):8.1-fpm-bullseye
  - [composer](https://hub.docker.com/_/composer):2.2

### web コンテナ

- Base image
  - [nginx](https://hub.docker.com/_/nginx):1.22

### db コンテナ

- Base image
  - [mysql/mysql-server](https://hub.docker.com/r/mysql/mysql-server):8.0

## コミットルール
コード修正は必ずブランチを切って対応
</br>なお、コミット時、コミットメッセージには以下の接頭辞から対応するものをつけてコミットすること。

```bash
追加:（機能・ファイルなどを）追加する
修正:（コードなどを）修正する
改善:（コードなどを）改善する
更新:（パッケージやドキュメントなどを）更新する
削除:（ファイル名やコードを）除去する
改名:（ファイル名を）変更する
移動:（AをBに）移動する
交換:（AをBに）変更する
```

テンプレート
```bash
【更新】README.md内容更新
```

## ブランチ運用ルール
ブランチ名は以下のルールに従い命名し、運用していく。

```bash
main: プロダクトとしてリリースするためのブランチ。
develop: 開発ブランチ。コードが安定しリリース準備ができたら main へプルリクエストし、マージする。このブランチが最新バージョンとなる。
feature/xxxxxxxx: 機能の追加。 develop から分岐し develop にプルリクエストし、マージする。
fix/xxxxxxxx: リリース後のクリティカルなバグフィックスなど、 現在のプロダクトのバージョンに対する変更用。
```
