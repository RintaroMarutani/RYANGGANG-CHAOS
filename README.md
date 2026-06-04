# RYANGGANGCHAOS — LP

> **2026.06.05 改名:** SHANHAI DISTRACTION → **RYANGGANGCHAOS**（旧ブランド素材は `assets/legacy-shanhai-*.png` に保管）

eスポーツ組織「RYANGGANGCHAOS」のランディングページ。
ダーク × レッドの戦術的ゲーミング美学。完全レスポンシブ・静的サイト（依存ライブラリなし）。

> **DELETE THE NOISE.** — 勝利を阻む全てを削除する。

## 構成

```
TEAM_LP/
├── index.html          # 1ページLP（全セクション）
├── css/
│   └── style.css       # スタイル（レスポンシブ含む）
├── js/
│   └── main.js         # ナビ開閉・スクロール出現・ヘッダー縮小
├── assets/
│   ├── logo-horizontal.png  # 横型ロゴ（ヘッダー/フッター・透過済）
│   ├── logo-emblem.png      # 円形エンブレム（ヒーロー/哲学・透過済）
│   ├── favicon-32.png / favicon-180.png
│   ├── og-image.png         # SNSシェア用OG画像
│   └── design-reference.png # 元デザインカンプ（参考用）
├── .nojekyll
└── README.md
```

## セクション

1. **Header** — 固定ナビ（スクロールで縮小／モバイルはハンバーガー）
2. **Hero** — DELETE THE NOISE ／ CTA ／ 座標 31.2304°N, 121.4737°E
3. **WHO WE ARE** — 組織紹介
4. **MISSION / VISION** — 2カラムカード
5. **HISTORY** — 2024〜2026 タイムライン
6. **DIVISIONS** — VALORANT / CREATORS / COMMUNITY
7. **PHILOSOPHY** — NO EXCUSES. NO FEAR. NO DISTRACTION
8. **JOIN** — X / YouTube / Discord
9. **Footer**

## ローカル確認

ビルド不要。ブラウザで `index.html` を直接開くだけ。
（フォントはGoogle Fonts CDN利用のためネット接続が必要）

簡易サーバーで見る場合:

```bash
python -m http.server 8000
# → http://localhost:8000
```

## GitHub Pages へ公開

1. GitHubで新規リポジトリを作成（例: `team-lp`）
2. このディレクトリをプッシュ:

   ```bash
   git init
   git add .
   git commit -m "Initial commit: SHANHAI DISTRACTION LP"
   git branch -M main
   git remote add origin https://github.com/<ユーザー名>/<リポジトリ名>.git
   git push -u origin main
   ```

3. リポジトリの **Settings → Pages** を開く
4. **Source** を `Deploy from a branch`、**Branch** を `main` / `/ (root)` に設定して Save
5. 数分後、`https://<ユーザー名>.github.io/<リポジトリ名>/` で公開

## カスタマイズ

| 項目 | 場所 |
|------|------|
| 配色 | `css/style.css` 冒頭の `:root` 変数（`--red` `--cream` など） |
| SNSリンク | `index.html` の `.social` / フッター `href` |
| 各セクション文言 | `index.html` |
| 写真差し替え | ヒーロー背景は `.hero__figure` 等のCSSグラデーション。実写真を使う場合は `assets/` に追加し、該当要素に `background-image` を指定 |

## ライセンス / 素材

ロゴ・テキスト等のブランド素材は SHANHAI DISTRACTION に帰属。
