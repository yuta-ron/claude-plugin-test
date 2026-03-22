# greeting plugin

時間帯に応じた挨拶を返すClaude Codeスキルです。

## インストール

```
/plugin marketplace add yuta-ron/claude-plugin-test
/plugin install greeting-plugin@greeting-plugin-marketplace
```

## 使い方

```
/greeting
```

名前を指定することもできます：

```
/greeting 田中
```

## 挨拶パターン

| 時間帯 | 挨拶 |
|--------|------|
| 5〜11時 | おはようございます！☀️ |
| 12〜17時 | こんにちは！😊 |
| 18〜21時 | こんばんは！🌙 |
| 22〜4時 | 夜遅いですね！🌃 |

---

## /tech-news

HackerNews・Reddit・国内メガベンチャーのテックブログから最新情報を収集し、日本語で要約します。

```
/tech-news
```

### 収集ソース

**海外**
- HackerNews Top Stories
- Reddit r/programming, r/MachineLearning

**国内テックブログ**
- LINEヤフー / Mercari / ZOZO / DevelopersIO (クラスメソッド)

### 出力例

```
### 🌐 海外トレンド (HackerNews / Reddit)
1. **RustのWebAssembly対応が大幅強化**
   - 元タイトル: Rust WASM support major update
   - 要約: ...

### 🇯🇵 国内テックブログ
1. **Kubernetes移行で学んだ5つの教訓**
   - 媒体: DevelopersIO
   - 要約: ...

## 今日のまとめ
...
```

> このスキルは `context: fork` + `general-purpose` subagentで動作します。
