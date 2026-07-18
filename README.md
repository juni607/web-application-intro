# 從網頁到 Web Application (Web Fundamentals Presentation)

這是一個專為網頁開發初學者設計的**互動式簡報網頁（教學投影片）**。透過簡潔美觀的視覺設計與實用的互動元件，引導學習者理解網頁的基本結構，以及現代 Web Application（前端、後端、資料庫）在幕後協同運作的原理。

---

## 🚀 如何運行與預覽

由於此項目為純靜態網頁（Static Website），您可以透過以下幾種方式輕鬆運行：

1. **直接開啟**：
   在瀏覽器中直接打開 `index.html` 即可運作所有功能。
2. **使用本地伺服器（推薦）**：
   如果您想在更接近真實生產環境的條件下測試，或避免瀏覽器因安全性限制影響某些 API，可以在專案根目錄下運行本地 HTTP 伺服器：
   *   **Python**:
       ```bash
       python -m http.server 8000
       ```
       然後在瀏覽器打開 `http://localhost:8000`
   *   **Node.js (npx)**:
       ```bash
       npx serve ./
       ```
       然後在瀏覽器打開 `http://localhost:3000`（或終端機輸出的對應埠口）

---

## 📁 檔案結構說明

```text
web-application-introduction/
├── README.md                     # 本專案說明文件（供人類與 AI 閱讀）
├── VIBE_LOG.md                   # Vibe Coding 進度追蹤與 AI 協作手冊（AI 核心讀檔）
├── index.html                    # 網站核心檔案（包含 HTML、CSS 樣式與 JS 互動邏輯）
└── assets/                       # 靜態資源目錄
    └── web-application-anatomy.png # 封面所使用的 Web 系統架構插圖
```

---

## 🤖 專屬 AI Vibe Coding 指引

本專案採用 **Vibe Coding** 開發模式。為了維持程式碼的乾淨、美學品質與邏輯一致性，當有 AI 助手介入開發時，請務必遵循以下規範：

1. **優先閱讀 `VIBE_LOG.md`**：了解當前最新的開發需求、進度、技術規範與歷史變更。
2. **遵守現有的 UI/UX 美學規範**：本專案採用精心設計的 Vanilla CSS（內建 CSS 變數），進行任何樣式修改時，請優先使用 `:root` 中定義的變數（如 `--ink`, `--muted`, `--fe` 等），以確保設計風格的一致性。
3. **保持程式碼簡潔**：除非有明確要求，否則應避免引入龐大的第三方 JavaScript/CSS 庫，以維持單一檔案載入的流暢度。
4. **即時更新進度**：每次完成新功能開發或 bug 修復後，請務必更新 `VIBE_LOG.md` 中的**進度狀態**與**變更日誌**。

更詳細的開發規格與當前任務清單，請參見：👉 **[VIBE_LOG.md](file:///Users/zhengbohong/Documents/codex%20vibe%20coding/web%20application%20introduction/VIBE_LOG.md)**
