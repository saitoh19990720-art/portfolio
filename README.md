# portfolio

しずくの母艦ポートフォリオ LP（1枚もの）。

**公開先:** https://shizuku-portfolio.vercel.app

## ファイル構成

| ファイル | 役割 |
|---|---|
| `index.html` | LP本体（`{{PLACEHOLDER}}` 形式） |
| `style.css` | ダークテーマ・CSS変数トークン設計 |
| `og.svg` | OG画像 |
| `robots.txt` | クローラー設定 |
| `sitemap.xml` | サイトマップ |
| `.env.example` | 環境変数サンプル |
| `replace-placeholders.sh` | `.env` → `dist/` 生成スクリプト |

## セットアップ

```bash
# 1. .env を作成
cp .env.example .env
# .env を編集して実URLを記入

# 2. dist/ を生成
bash replace-placeholders.sh

# 3. ローカル確認
npx serve dist
```

## デプロイ

```bash
# ~/work/deploy.sh で一発
bash ~/work/deploy.sh
```

内部でやること: `replace-placeholders.sh` → `vercel --prod` → `alias set shizuku-portfolio.vercel.app`

## .env の変数

| 変数 | 値 |
|---|---|
| `PORTFOLIO_URL` | https://shizuku-portfolio.vercel.app |
| `OSHI_LOG_URL` | https://oshi-log-shizuku.vercel.app |
| `OSHI_LOG_REPO` | https://github.com/saitoh19990720-art/oshi-log |
| `GITHUB_URL` | https://github.com/saitoh19990720-art |
| `OG_IMAGE_URL` | https://shizuku-portfolio.vercel.app/og.svg |
| `CROWDWORKS_URL` | https://crowdworks.jp/public/employees/saitoh19990720 |
| `LANCERS_URL` | https://www.lancers.jp/profile/saitoh19990720 |
