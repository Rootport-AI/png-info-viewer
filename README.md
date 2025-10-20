# png-info-viewer

ブラウザだけで **PNG の `tEXt` チャンク（例: Stable Diffusion の `parameters`）を読み取る**超軽量ビューア。  
**アップロードなし・完全クライアントサイド**で動作します。

> ⚠️ 本プロジェクトは **AUTOMATIC1111 Stable Diffusion WebUI の「PNG Info」機能に着想**を得ていますが、  
> **WebUI とは完全に独立**しており、ブログ記事などに **そのまま埋め込んで使える**のが特徴です。  
> AUTOMATIC1111 プロジェクトとは非公式・無関係です。

## デモ (GitHub Pages)
- URL: `https://rootport-ai.github.io/png-info-viewer/`

## 使い方
1. [index.html](./index.html) を開く（GitHub Pages のデモでもOK）
2. PNG を「ファイルを選択」またはドラッグ＆ドロップ
3. 先頭の `tEXt`、または `parameters` キーを優先して表示

## 特徴
- HTML + 素の JavaScript のみ
- ブラウザ内で解析（サーバ送信なし）
- ドラッグ＆ドロップ対応

## 既知の制限 / TODO
- `tEXt` のみ対応（`iTXt` や `zTXt` は未対応）
- すべての `tEXt` を一覧表示するUIは最小限
- CRC検証は省略（読み飛ばし）

### 将来拡張アイディア
- `iTXt`（UTF-8）/ `zTXt`（圧縮）のサポート（zlib解凍）
- 複数 `tEXt` のテーブル表示、コピー/JSONダウンロード
- `parameters` 整形（行頭整列・検索）

## ライセンス
MIT © Rootport-AI
