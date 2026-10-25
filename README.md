# taguchiyuma.github.io/web

個人ホームページのソースです。[Jekyll](https://jekyllrb.com/) で書かれており、
`main` ブランチの `docs/` を GitHub Pages が自動でビルド・公開します（ローカルでのビルドは不要）。

## 更新方法

GitHub 上でファイルを開き、鉛筆アイコン（Edit）から Markdown を編集してコミットするだけです。
数分後にサイトへ反映されます（進行状況はリポジトリの **Actions** タブで確認できます）。

| 更新したい内容 | 編集するファイル |
| --- | --- |
| トップページ（日本語） | `docs/index.md` |
| トップページ（英語） | `docs/en.md` |
| 業績リスト（日英共通） | `docs/publications.md` |
| 名前・SNS リンク・写真 | 各 `index.md` 冒頭の `---` で囲まれた部分 |
| 画像 | `docs/images/` にアップロード |

トップページは `## 見出し` ごとに 1 つのパネルとして表示されます。
新しいセクションを追加したい場合は `## 新しい見出し` を書き足してください。

### ブログ記事を追加する

`docs/_posts/` に `YYYY-MM-DD-任意の英数字.md` という名前でファイルを作成します。

```markdown
---
title: 記事タイトル
date: 2026-10-25
categories: [News]
tags: [タグ1, タグ2]
---

本文を Markdown で書きます。数式は $E = mc^2$ のように書けます。
```

記事は `/posts/YYYYMMDD/` で公開され、一覧は `/posts/` にあります。

## ローカルでプレビューする（任意）

```sh
cd docs
bundle install
bundle exec jekyll serve
# http://localhost:4000/web/ を開く
```
