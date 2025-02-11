# Github Pagesにブログを構築するまで

## 概要

## 想定読者
- Github Pagesにブログを開設したいと考えている人

## なぜGithub Pagesなのか
- デプロイが容易
- 無料
- Githubに触れる機会を増やせる
- 普段触れることがないフロントエンド技術を使える

## 構築の大方針
- 静的なブログサイトを構築する
- 未経験の技術を経験する

## アーキテクチャ検討
- 制約事項
  - 技術的な制約として、Github Pagesを利用すること
- 品質
  - 目次の充実などによる外部品質は考慮するが、無料のホスティングサービスのため内部品質は考慮しない

## 技術選定
- 言語/フレームワーク
  - TypeScript/Astro
    静的サイトなのでJavaScriptの読み込みは不要としたい。
- DB
  - なし
- インフラ
  - ホスティングサービスとしてGithub Pagesを利用する
- コード管理
  - Github
- CI/CD
  - Github Actions
- 監視ツール
  - なし

## ざっくりとした流れ

- [Astroのチュートリアル](https://docs.astro.build/ja/tutorial/0-introduction/)
でブログを作る
  - [チュートリアルではNetlifyを使っているが、ここでGitHub Pagesへのデプロイもやっておく](https://docs.astro.build/ja/guides/deploy/github/)

- TypeScriptを導入して再度デプロイしてみる

- コンテンツを拡充する

## 開発

ハマりポイントがあれば。すんなりいけばその旨記載する。

## デプロイ

ハマりポイントがあれば。すんなりいけばその旨記載する。


## 全体的な振り返り

## 参考
https://docs.github.com/ja/pages/getting-started-with-github-pages/about-github-pages
https://kakaku-techblog.com/entry/create-website-with-astro
https://docs.astro.build/ja/guides/deploy/github/



