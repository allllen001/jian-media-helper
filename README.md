# 影音下載小幫手

搭配「萬用影音下載器」網頁使用的本機程式。網頁只負責操作介面，實際的下載在你自己的電腦上執行，檔案存到這台電腦的「下載」資料夾。

適用 Windows 10／11（64 位元），免安裝。

## 下載

到 [Releases](https://github.com/allllen001/jian-media-helper/releases/latest) 下載 `jian-media-helper-v版本.zip`。

同一頁的 `.sha256` 檔是壓縮包的 SHA-256，想確認檔案完整可以在 PowerShell 執行：

```powershell
Get-FileHash .\jian-media-helper-v0.1.1.zip -Algorithm SHA256
```

## 使用

1. 把壓縮包**整個解壓縮**到自己的電腦（例如「文件」），不要直接在壓縮檔裡執行。
2. 按兩下「啟動小幫手.cmd」。第一次執行 Windows 可能會詢問，選「其他資訊」→「仍要執行」。
3. 視窗會顯示 6 位數配對碼。用 Chrome 或 Edge 開啟「萬用影音下載器」，輸入配對碼。
4. 貼上影片網址，選擇影片或音檔後下載。

視窗開著才能下載，關掉視窗小幫手就停止。

## 安全

- 小幫手只在這台電腦上聽 `127.0.0.1`，不對區域網路或網際網路開放。
- 只接受指定網站的網頁連線，而且要先用視窗上的配對碼配對。
- 不收帳號、密碼或 cookie，不下載需要登入才能觀看的內容。

## 使用提醒

下載內容僅供課堂教學使用，請遵守著作權法與各平台的使用條款。

## 內含的軟體

壓縮包原樣附帶下列軟體的官方執行檔，沒有修改：

| 軟體 | 授權 | 來源 |
|---|---|---|
| [Node.js](https://nodejs.org/) | MIT 及其相依套件各自的授權 | https://github.com/nodejs/node |
| [yt-dlp](https://github.com/yt-dlp/yt-dlp) | The Unlicense | https://github.com/yt-dlp/yt-dlp |
| [FFmpeg](https://ffmpeg.org/) | GPLv3 | 建置來自 https://github.com/yt-dlp/FFmpeg-Builds ，原始碼 https://github.com/FFmpeg/FFmpeg |

各版本號與 FFmpeg 授權全文在壓縮包內的「第三方軟體授權.txt」與 `app/bin/FFmpeg-LICENSE.txt`。小幫手本身的程式在壓縮包的 `app/` 資料夾，是純文字的 JavaScript，可以直接打開檢視。
