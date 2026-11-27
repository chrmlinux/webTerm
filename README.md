# webTerm

Web Serial API を使うブラウザ版シリアル端末です。単一の `index.html` のみで動作し、インストールやサーバは不要です。

A browser serial terminal using the Web Serial API. A single `index.html`, no install and no server needed.

## 使う / Use

https://chrmlinux.github.io/webTerm/

Chrome / Edge で開き、シリアルデバイスへ接続します。ローカルで使う場合は `index.html` をダウンロードして直接開くこともできます。

Open the URL above in Chrome / Edge and connect to a serial device. To use it locally, download `index.html` and open it directly.

## 機能 / Features

- 直接入力（既定 ON）：ログ画面へフォーカスし、Enter は実際の改行を送信します。
- ローカルエコー（既定 OFF）：接続先が自身でエコーする場合の二重表示を防ぎます。
- ボーレート選択（カスタム入力可）。
- 日本語 / English 切り替え：ヘッダーのボタンで切り替え、全 50 項目が対象です。選択はブラウザに保存されます。
- HEX 表示：ON の間、受信バイトをオフセット付き 16 進ダンプ（16 バイト + ASCII 表示）で表示します。
- バイナリ保存：HEX 表示の間、「ログを保存」は「バイナリ保存 (.bin)」に変わり、受信した生バイトそのものを保存します。生バイトは最大 8 MiB まで保持します。
- テキスト表示の間もログ保存は `.log` として保存できます。受信バッファは 256 KiB です。

- Direct input (default ON): focus the log view; Enter sends a real newline.
- Local echo (default OFF): avoids double display when the device echoes by itself.
- Baud rate selection, including a custom value.
- Japanese / English toggle: the header button switches all 50 UI items. The choice is saved in the browser.
- HEX view: while ON, received bytes are shown as an offset hex dump (16 bytes + ASCII).
- Binary save: while HEX view is ON, "Save log" becomes "Save binary (.bin)" and writes the received raw bytes as-is. Raw bytes are kept up to 8 MiB.
- In text view, the log can be saved as `.log`. The receive buffer is 256 KiB.

## 注意 / Notes

- Web Serial が使えるブラウザ（Chrome / Edge など）が必要です。
- 公開ページは誰でも開くことができます。秘密情報は含めないでください。
- Web Serial requires a supporting browser (Chrome / Edge, etc.).
- The published page is public. Do not put private information in it.
