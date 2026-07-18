# 🤖 Vibe Coding 進度追蹤與 AI 協作手冊 (VIBE_LOG.md)

本文件是專門為 **AI 協作者** 設計的「記憶庫」與「進度追蹤表」。
每當新的 AI 助手接手本專案，或準備進行 Vibe Coding 時，請**優先讀取本檔案**以快速同步需求、進度與技術規約。

---

## 🎯 當前專案目標 (Project Goal)
本專案為一個 **Web 開發基礎互動式簡報**，旨在透過直觀的 UI 互動與視覺化圖表，引導學習者跨越從靜態網頁（HTML/CSS/JS）到動態 Web Application（前端、後端、資料庫）的心智模型。

*   **當前階段任務**：完成初始版本的架構搭建，並建立好 AI 協作的文檔基礎。

---

## 🛠 系統技術規格與設計系統 (Tech Stack & Design System)

為確保 Vibe Coding 過程中不會破壞現有的 UI 質感與體驗，修改程式碼時請遵守以下規範：

### 1. 設計變數 (Design Tokens)
所有顏色與背景均透過 `index.html` 中的 CSS 變數定義，修改樣式時請優先套用：
*   **主色調 (Main)**:
    *   文字主色碼 (`--ink`): `#193459` (深邃藍)
    *   次要文字 (`--muted`): `#657b98` (灰藍)
    *   底色/背景 (`--bg`): `#f6f9fd` (極淺藍灰)
    *   線條/邊框 (`--line`): `#dce7f4`
*   **技術代表色 (Tech Accents)**:
    *   HTML (`--html`): `#ef7643` (暖橘)
    *   CSS (`--css`): `#4288e9` (亮藍)
    *   JavaScript (`--js`): `#dfad08` (金黃)
    *   前端 (`--fe`): `#14aa97` (薄荷綠)
    *   後端 (`--be`): `#8168dc` (紫色)
    *   資料庫 (`--db`): `#3d76c9` (寶藍)

### 2. 字型系統 (Typography)
*   **標準字型**：`ui-sans-serif, -apple-system, BlinkMacSystemFont, "Noto Sans TC", "PingFang TC", sans-serif`
*   **等寬字型（程式碼區）**：`ui-monospace, SFMono-Regular, Menlo, monospace`

### 3. RWD 響應式斷點 (Responsive Breakpoints)
*   `max-width: 1100px`：調整卡片間距、架構圖大小、泳道圖高度，適配平板。
*   `max-width: 800px`：**行動裝置模式**。簡報由 `position: fixed` 全螢幕切換轉為 `overflow: auto` 的垂直流動排版（使用 `display: none` / `display: grid` 來顯示當前 active 的 slide）。
*   `max-width: 480px`：極小螢幕（手機）的內距與字型大小縮減。
*   `hover:none`：**觸控最佳化**。在觸控設備上取消 hover 縮放與陰影特效，避免黏滯感。

---

## 📝 任務清單與開發狀態 (Task Board)

* 標記說明：`[ ]` 未開始 / `[/]` 進行中 / `[x]` 已完成

### 第一階段：基本架構與內容設計 (已完成)
- [x] 設計 HTML 與 CSS 基礎框架（包含 RWD、磨砂玻璃質感、全螢幕簡報切換）
- [x] 編寫教學簡報 15 頁內容（HTML 角色、前後端分工、三層架構、系統運作等）
- [x] 實作 DOM 懸停高亮互動 Widget
- [x] 實作前端三劍客分工互動 Widget
- [x] 實作登入流程模擬互動 Widget（成功與失敗情境）
- [x] 加入鍵盤方向鍵、空白鍵切換 Slide 的輔助控制功能
- [x] 設計精美的網頁封面圖（`web-application-anatomy.png`）

### 第二階段：AI 協作環境建置 (已完成)
- [x] 建立 `README.md`，說明專案啟動方式與檔案結構
- [x] 建立 `VIBE_LOG.md`，記錄 AI Vibe Coding 技術規約與進度追蹤

### 第三階段：選單與導覽優化 (已完成)
- [x] 實作漢堡選單 (Hamburger Menu) 導覽側邊欄，支援快速跳轉章節與投影片

### 第四階段：未來預計擴充功能 (Backlog)
- [ ] **夜間模式 (Dark Mode)**：提供深色主題，減少暗處閱讀疲勞。
- [ ] **動畫轉場優化**：為 Slide 切換增加更平滑的滑入、淡出動畫（如 CSS Page Transitions API 或自訂類別）。
- [ ] **進度進階儲存**：使用 `localStorage` 紀錄使用者上一次讀到的頁數，重整網頁時自動恢復。
- [ ] **測驗小遊戲 Widget**：在簡報最後加入一個簡單的選擇題或連連看，複習「前端/後端/資料庫」的分工。

---

## 📅 歷史變更日誌 (Change Log)

### 2026-07-18
*   **新增項目**：
    *   新增 `README.md`：提供專案啟動、檔案結構與 AI 指引的說明。
    *   新增 `VIBE_LOG.md`：建立專門用於 vibe coding 進度與 AI 記憶同步的追蹤手冊。
    *   **漢堡選單功能實作**：
        *   在 `index.html` 中新增圓形毛玻璃 `.menu-toggle` 按鈕，點擊時具備變形成「X」的平滑動畫。
        *   實作側邊抽屜式選單 `.menu-drawer` 與背景遮罩 `.menu-overlay`，支援毛玻璃模糊效果與滑出動畫。
        *   透過 JavaScript 動態讀取投影片的 `data-chapter` 與 `.title` 標題，自動生成結構化的章節導覽列表，並具備點擊快速跳轉與目前所在頁面高亮（`.active`）功能。
        *   調整鍵盤監聽，加入 `Escape` 鍵關閉選單，以及在選單開啟時停用空白鍵翻頁功能以利捲動。
*   **現狀確認**：確認靜態網頁（`index.html`）功能正常，包含 DOM 懸停高亮、三劍客分工、登入流程、漢堡選單等互動 Widget 皆可正常操作。

