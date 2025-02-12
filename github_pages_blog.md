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

以下のエラーが出てデプロイに失敗した
```
Current runner version: '2.322.0'
Operating System
Runner Image
Runner Image Provisioner
GITHUB_TOKEN Permissions
Secret source: Actions
Prepare workflow directory
Prepare all required actions
Getting action download info
Download action repository 'actions/checkout@v4' (SHA:11bd71901bbe5b1630ceea73d27597364c9af683)
Download action repository 'withastro/action@v1' (SHA:9a7959a16949e620a22e74f81c10cb7ce3b76924)
Getting action download info
Download action repository 'pnpm/action-setup@v2' (SHA:eae0cfeb286e66ffb5155f1a79b90583a127a68b)
Download action repository 'oven-sh/setup-bun@v1' (SHA:f4d14e03ff726c06358e5557344e1da148b56cf7)
Download action repository 'actions/setup-node@v4' (SHA:1d0ff469b7ec7b3cb9d8673fde0c81c44821de2a)
Download action repository 'actions/upload-pages-artifact@v2' (SHA:a753861a5debcf57bf8b404356158c8e1e33150c)
Getting action download info
Error: This request has been automatically failed because it uses a deprecated version of `actions/upload-artifact: v3`. Learn more: https://github.blog/changelog/2024-04-16-deprecation-notice-v3-of-the-artifact-actions/
```

-> 非推奨のバージョンを使っているのがエラーの理由みたいだ。

→同じエラーでデプロイに失敗した人がいた。修正ポイントは2点。
 withastro/action@v1をv2へ、actions/deploy-pages@v1をv4へ
　https://craftgear.github.io/posts/20250201/


## 全体的な振り返り

## 参考
https://docs.github.com/ja/pages/getting-started-with-github-pages/about-github-pages
https://kakaku-techblog.com/entry/create-website-with-astro
https://docs.astro.build/ja/guides/deploy/github/



