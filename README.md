<img src="assets/LightView.png" width="64" alt="LightView アイコン">

# LightView 📄

Windows向けの、軽快なPDF・Markdown・テキスト・表・HTMLビューワです。

**[最新版をダウンロード](https://github.com/mezon-web/LightView-Releases/releases/latest)**

## はじめに

1. リリースページの **Assets** から `LightView-v0.2.4-win-x64.zip` をダウンロードします。
2. ZIPを展開し、`LightView` フォルダ内の **LightView.exe** を起動します。
3. 「開く」またはファイルのドラッグ＆ドロップで文書を開きます。

インストーラーはありません。フォルダごと保存して使うポータブル版です。
使い方は右端の **「？」／F1** または [操作説明](docs/操作説明.md) で確認できます。

## 必要な実行環境

- **Windows x64** と **.NET 10 Desktop Runtime x64**。導入済みなら追加のインストールは不要です。[Microsoft公式ダウンロード](https://dotnet.microsoft.com/ja-jp/download/dotnet/10.0) の「.NET デスクトップ ランタイム」から取得できます。
- **Markdown・HTMLの表示**にはMicrosoft Edge WebView2 Runtimeが必要です。[Microsoft公式ページ](https://developer.microsoft.com/ja-jp/microsoft-edge/webview2/) から取得できます。未導入の場合はアプリ内で導入先と再試行を案内します。

.NETとWebView2 RuntimeはZIPに同梱していません。PDF・TXT・LOG・CSV・TSVの利用ではWebView2を起動しません。

## 対応形式と主な機能

| 形式 | 主な機能 |
| --- | --- |
| PDF | 連続スクロール、ページ移動、文字選択・コピー、検索、しおり目次、文書内リンク |
| Markdown | 表、コードの色分け・コピー、ローカル画像、Mermaid、数式、見出し目次 |
| TXT・LOG | 行番号、検索・コピー、大きな文書の仮想化表示、LOGの追記追従 |
| CSV・TSV | 表表示、見出し固定、列幅変更、全セル検索、セルコピー |
| HTML | ローカルの静的HTML、見出し目次、検索・コピー |

全形式でファイル履歴10件、拡大縮小、検索結果の一覧を利用できます。PDF以外は保存時の自動更新とF5更新に対応します。複数の文書は別ウィンドウで開きます。

対応する斜めのテキスト透かしがあるPDFでは「斜め透かしを非表示」を利用できます。Windows標準OCRが利用できる環境では、画像PDFの現在のページを認識して検索・コピーできます。元のPDFファイルは変更しません。

Markdown・HTMLの埋め込みスクリプトを実行せず、外部画像を自動取得しません。閲覧専用です。

## 画面

![LightViewの起動画面](assets/viewer.png)

![アプリ内ヘルプ](assets/help.png)

## 更新と確認

アプリを終了し、新しいZIPを展開して配布フォルダを更新してください。ファイル履歴は引き継ぎます。
各リリースにZIPの **SHA-256チェックサム** を添付しています。

v0.2.4はWindows 11の隔離デスクトップで651項目を検査しました。Windows 10実機では未検証です。
[変更履歴](CHANGELOG.md) / [第三者ソフトウェアの表記](THIRD-PARTY-NOTICES.md)

このリポジトリは配布版と利用者向け文書を管理します。第三者ソフトウェアのライセンスは配布ZIP内の `licenses` フォルダに同梱しています。
