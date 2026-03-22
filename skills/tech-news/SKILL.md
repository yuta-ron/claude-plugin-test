---
name: tech-news
description: HackerNews・Reddit・国内メガベンチャーのテックブログから最新情報を収集し、日本語で要約して返す。最新技術トレンドを知りたいときに使用する。
user-invocable: true
context: fork
agent: general-purpose
allowed-tools: WebFetch, WebSearch
---

以下のソースから最新のテック記事を収集し、日本語で要約してください。

## 収集ソース

### 海外メディア
1. HackerNews Top Stories API: https://hacker-news.firebaseio.com/v0/topstories.json
   - 上位10件のIDを取得し、各記事の詳細を https://hacker-news.firebaseio.com/v0/item/{id}.json で取得
2. Reddit r/programming: https://www.reddit.com/r/programming/hot.json?limit=5
3. Reddit r/MachineLearning: https://www.reddit.com/r/MachineLearning/hot.json?limit=5

### 国内テックブログ（各1〜2件）
4. LINEヤフー: https://techblog.lycorp.co.jp/ja
5. Mercari Engineering: https://engineering.mercari.com/
6. ZOZOTech: https://techblog.zozo.com/
7. DevelopersIO (クラスメソッド): https://dev.classmethod.jp/

## 出力フォーマット

各記事について以下の形式でまとめてください：

### 🌐 海外トレンド (HackerNews / Reddit)

1. **[記事タイトルの日本語訳]**
   - 元タイトル: [原文タイトル]
   - 要約: [2〜3文で日本語要約]
   - URL: [リンク]

### 🇯🇵 国内テックブログ

1. **[記事タイトル]**
   - 媒体: [ブログ名]
   - 要約: [2〜3文で要約]
   - URL: [リンク]

最後に「## 今日のまとめ」として全体のトレンドを3行で締めくくってください。
