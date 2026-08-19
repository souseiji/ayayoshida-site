# ayayoshida-site

吉田あや公式サイトのHugoソースリポジトリ。

公開先: https://ayayoshida03.github.io/（別リポジトリ `ayayoshida03/ayayoshida03.github.io`）

## 開発

```
hugo server -D
```

`http://localhost:1313/` で確認できます。

## コンテンツの編集

テキストはすべて `data/` 以下のYAMLファイルにあります。HTML/CSSを触らなくても、ここを編集するだけで内容を更新できます。

- `data/site.yaml` — ヒーロー文言、想い、プロフィール年表、応援・お問い合わせ文言
- `data/policies.yaml` — 政策一覧
- `data/news.yaml` — 活動報告・お知らせ
- `data/faq.yaml` — よくある質問

写真は `static/images/` に置きます。

## デプロイ

`main` ブランチにpushすると、GitHub Actionsが自動でビルドし、`ayayoshida03.github.io` リポジトリへ公開します（`.github/workflows/deploy.yml`）。

初回セットアップとして、このリポジトリのSecretsに `DEPLOY_TOKEN`（`ayayoshida03.github.io` へのpush権限を持つトークン）の登録が必要です。
