# 一磚一瓦

個人的存房手帳：每月記錄實際存款，對照計畫看達成率、年度累積、資產配置與里程碑；用砌磚的房子顯示進度，並有一鍵記錄、多目標、情境模擬、智能提醒與 AI 顧問。

## 使用方式

1. 把 `index.html`、`manifest.webmanifest`、`sw.js`、`icon-192.png`、`icon-512.png` 放進 GitHub repo 的根目錄。
2. 到 repo 的 **Settings → Pages**，Source 選 `main` branch、`/ (root)`，儲存。
3. 幾分鐘後用 `https://<你的帳號>.github.io/<repo 名稱>/` 打開。

不需要安裝或建置。

### 加到手機主畫面

- iPhone：用 Safari 打開網址 → 分享 → 加入主畫面。
- Android：用 Chrome 打開 → 選單 → 安裝應用程式。

加入後會像 App 一樣全螢幕開啟，沒網路也能打開記錄（AI 功能需要網路）。

## 資料存在哪裡

- 在 GitHub Pages 上開啟時，所有紀錄只存在**你自己這台裝置的瀏覽器**（localStorage），不會上傳到 GitHub。
- 換手機、換瀏覽器或清除網站資料，紀錄就不會跟著走。請定期在「資料」分頁下載**完整備份（JSON）**，換裝置時再用「匯入」還原。
- 「資料」分頁也有每日自動快照（保留 14 份，只在本機）與 CSV 匯出（可用 Excel 開啟）。
- 在 Claude 裡開啟時，資料會存在 Claude 雲端，並在本機留一份。

## AI 顧問

在「AI 顧問 → AI 連線設定」選擇：

- **Anthropic API（Claude）**：填入 API 金鑰，模型預設 `claude-sonnet-5-5`。
- **Google Gemini API**：填入 Gemini API 金鑰，模型預設 `gemini-3.6-flash`。
- **OpenAI 相容 API**：填入 API 位址、金鑰與模型名稱。

金鑰只存在瀏覽器的 localStorage，不會寫進備份檔。**請勿把 API 金鑰寫進程式碼或提交到 GitHub。** 若 repo 是公開的，任何人都能看到 `index.html` 的內容，但看不到你瀏覽器裡的金鑰與紀錄。

> 從瀏覽器直接呼叫 API 代表金鑰會存在這台裝置上，建議為這個用途建立一把專用金鑰，並在供應商後台設定用量上限。

## 提醒

手帳內建提醒（記錄日、獎金、定存到期、進度落後、超支等）會在打開時顯示在「總覽」。網頁本身無法在背景推播，建議搭配手機的提醒事項設定每月記錄日。
