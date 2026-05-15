# Tide

一個專注「水位感」的個人記帳 prototype。把月費和主動消費都化成一顆會起伏的水球，月初滿、月底降，幫你看見錢正在流去哪。

> 還是早期 prototype，所有資料只存在你的瀏覽器（localStorage）。沒有後端、沒有帳號、沒有金流。歡迎拿來測，但別當真實理財工具用 :)

## 🌊 試用

直接打開部署版：**https://YOUR_USERNAME.github.io/tide/**

或下載 `index.html` 用瀏覽器開也行，不需要伺服器。

### 進階：跳過 onboarding 看主畫面

開 `locktest.html?lock=big` 可以直接看不同預算下的水球長相：

- `?lock=tiny2` — 預算 $1,128
- `?lock=tiny` — 預算 $1,500
- `?lock=mid` — 預算 $5,000
- `?lock=big` — 預算 50% 月費的情境
- `?lock=hi` — 預算 $3,789

## 📁 檔案

```
.
├── index.html          # 主檔，單一 HTML（CSS + JS + SVG 全在裡面）
├── locktest.html       # 開發測試版（含 seed 注入和 URL 參數）
├── docs/
│   └── handover.md     # 技術交接文檔，給接手開發者看
└── README.md
```

## 🐛 想回報問題嗎？

最有幫助的格式：

> **狀況**：我在做什麼  
> **預期**：以為會發生什麼  
> **實際**：實際發生什麼  
> **裝置**：iPhone 15 / Chrome on Mac / etc

開 [Issues](../../issues) 丟給我就好。

## 🔄 重設資料

想清掉測試資料重新體驗 onboarding：

- **Chrome/Edge**：F12 → Application → Local Storage → 刪 `tide_state_v15`
- **Safari**：開發者工具 → 儲存空間 → 本機儲存
- **手機**：開無痕視窗

## 🧰 開發

純前端、單檔、vanilla JS、零依賴。改完直接重新整理就看到。

技術細節（水位算法、月費視覺、Pro 商業模式演化過程）寫在 `docs/handover.md`。
