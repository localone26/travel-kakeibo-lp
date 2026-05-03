# Claude Code 設定

## ⚠️ 最重要ルール: ツール前に必ずテキストを出力すること

**ツールを呼び出す前に必ず1文以上のテキストを出力すること。**
テキストなしでツールのみを実行すると、空のテキストブロックが生成され
`API Error: messages: text content blocks must be non-empty` が発生します。

**良い例:**
```
ファイルを確認します。
[Read ツール呼び出し]
```

**悪い例:**
```
[Read ツール呼び出し]  ← テキストなしは禁止
```

## プロジェクト概要

- **名称**: travel-kakeibo-lp
- **用途**: 旅マネーアプリのApp Store申請・AdMob審査用ページ
- **スタック**: 純粋なHTML/CSS（フレームワーク不使用）
- **ホスティング**: GitHub Pages

## ファイル構成

```
index.html    # プライバシーポリシーページ
app-ads.txt   # Google AdMob審査用（削除・変更禁止）
```

## 開発ルール

1. **ツール呼び出し前に必ず1文以上テキストを出力すること**（最重要）
2. 「最終更新日」は変更のたびに更新する
3. `app-ads.txt` はAdMob審査に必要なため削除・変更しない
4. デザイン: #007AFF（iOSブルー）、max-width 800px、font: -apple-system
5. 日本語コンテンツで統一
6. 変更はfeatureブランチで行い、mainへはPR経由でマージ

## ローカルプレビュー

```bash
python3 -m http.server 8080
# → http://localhost:8080 で確認
```
