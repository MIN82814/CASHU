# 🪙 CASHU 記帳 App

[![Frontend](https://img.shields.io/badge/Role-Front--End%20Developer-blue)](https://github.com/MIN82814/CASHU)
[![Build Tool](https://img.shields.io/badge/Build%20Tool-Vite-646CFF?logo=vite)](https://github.com/MIN82814/CASHU)
[![Style](https://img.shields.io/badge/Style-SCSS%20%7C%20Bootstrap%205-7952B3?logo=bootstrap)](https://github.com/MIN82814/CASHU)
[![Template](https://img.shields.io/badge/Template-EJS-A45A4B)](https://github.com/MIN82814/CASHU)

> **與 AAPD UI 設計團隊跨領域深度合作的現代化行動端網頁應用。**
> 本專案架構基於 **Vite** 構建，整合 **EJS 模板引擎**、**Bootstrap 5** 與 **SCSS 模塊化管理**。專案核心聚焦於極致的行動端畫素級（Pixel-Perfect）精密還原、高度解耦的樣式架構，以及高度自動化的前端開發與部署工作流。

---

## 🌟 核心功能

### 前台

| 功能 | 說明 |
| :--- | :--- |
| **動態收支記帳** | 提供直覺的計算機記帳面板，支援動態選擇資金來源帳戶與消費種類分類。 |
| **遊戲化儲蓄** | 透過「存錢計畫」與儲蓄任務挑戰，搭配每日打卡激發用戶持續記帳的動力。 |
| **數據儀表板** | 將複雜財務數據轉化為圖表，簡化行動端用戶的收支瀏覽體驗。 |
| **行動端極致優化** | 採用全向量化資產與客製化手勢導覽列，確保手持裝置的流暢度。 |

---

## 🙌 團隊分工

| 成員 | 共用 / 架構 | 🪙 記帳業務主線 | 🎯 存錢計畫主線 |
| :--- | :--- | :--- | :--- |
| **Min** | 搭建全站 SCSS 模塊化架構、封裝 `EJS` 共用模板、建置 `_navbar-bottom` 與 `_mobile-frame` 等全站核心視覺組件 | **獨立負責完整互動與頁面切換：**<br>· `log-add.html` (日誌新增)<br>· `select_account.html` (帳戶選擇)<br>· `category-page.html` (消費分類)<br>· `add-result.html` (新增結果) | **獨立負責完整互動與頁面切換：**<br>· `plan-save.html` (計畫主頁)<br>· `plan-save-detail.html` (詳情追蹤)<br>· `plan-save-success.html` (成功回饋) |
| **Kate** | 負責處理全站 `LOADING` 狀態之 GIF 動態載入與流暢視覺顯現切換 | · `index.html` (預設首頁入口與核心動態引導) | **獨立負責遊戲化任務與成就模組：**<br>· `Homepage_misson.html` (主頁儲蓄任務)<br>· `complete.html` (任務完成狀態)<br>· `mission-complete.html` (挑戰達成)<br>· `personal-accomplishment.html` (個人成就頁) |
| **Sherry** | 負責全站圖書/核心帳簿與報表相關的數據視覺樣式實作 | · `book.html` (歷史帳簿與圖書數據核心頁面) | - |
| **AAPD 設計團隊** | 負責全站行動端產品定位、Persona 洞察、全站高保真 UI 設計稿（Figma） | 記帳流與計算機介面 UX 流程規劃、視覺規範定義 | 遊戲化儲蓄任務、打卡挑戰與成就勳章視覺設計 |

---

## 🛠️ 前端技術棧 (Tech Stack)

| 技術 / 工具 | 說明 |
| :--- | :--- |
| **Vite** | 現代化前端構建工具與高效能開發伺服器（HMR） |
| **EJS** | 網頁模板引擎，用於 HTML 頁面的組件化與組裝管理 |
| **Bootstrap 5** | 響應式（Responsive Design）CSS 框架 |
| **Sass / SCSS** | CSS 預處理器，負責高可維護性的模塊化樣式管理 |
| **Lucide** | 高性能向量圖示庫（Icon Library） |
| **gh-pages** | GitHub Pages 一鍵自動化部署工具 |

---

## 前端技術實作亮點

### 1. 核心業務模組開發：精密佈局與 SVG 效能優化
- **功能實作**：負責「記帳」與「存錢計畫」兩大核心商務邏輯鏈的完整前端開發。
- **畫素級還原 (Pixel-Perfect)**：為確保在行動端各式解析度螢幕（含 Retina 視網膜螢幕）上的極致清晰度，深入運用 **SVG 向量圖形** 與 **Icon Font (Lucide)** 進行優化。大幅減少了頁面的 HTTP 請求次數（Request Counts）與資源包體積（Bundle Size），顯著提升首頁及功能頁的 DOM 渲染效能。

### 2. SCSS 模塊化架構設計與高度複用性元件
- **共用樣式解耦**：採用 `7-1 Pattern` 概念對 SCSS 進行架構分層（包含 base, layout, components, pages, utils），確保樣式碼的極高可讀性與擴充性。
- **獨立元件開發**：獨立開發全站核心視覺元件與其相對應的樣式模組（`_navbar-bottom.scss` 行動端底部導覽列、`_mobile-frame.scss` 全站通用手機外框、`_calculator.scss` 記帳計算機面板），成功統一全站行動端視覺，並讓團隊並行開發效率提升數倍。

### 3. 跨領域協商（技術守門人）
- 針對 UI 設計團隊提出的前衛互動稿進行前端可行性與效能評估。
- 在「設計師追求的複雜視覺」與「前端瀏覽器渲染效能、時程限制」之間取得最佳平衡點。透過主動提出替代技術方案（例如：運用 CSS/SCSS 變數與過渡動畫替代沉重的 JS 動畫庫），在不犧牲使用者體驗的前提下順流推進專案精密封版。

---

## 📁 資料夾結構

```text
CASHU/
├── main.js
├── package.json
├── vite.config.js
├── README.md
│
├── assets/
│   ├── images/
│   └── scss/
│       ├── all.scss
│       ├── base/
│       ├── components/
│       ├── layout/
│       ├── pages/
│       └── utils/
│
├── layout/
│   ├── header.ejs
│   └── footer.ejs
│
└── pages/
    ├── index.html
    ├── add-result.html
    ├── book.html
    ├── category-page.html
    ├── complete.html
    ├── Homepage_misson.html
    ├── log-add.html
    ├── mission-complete.html
    ├── personal-accomplishment.html
    ├── plan-save-detail.html
    ├── plan-save-success.html
    ├── plan-save.html
    └── select_account.html

---

## 快速開始 (Getting Started)

### 環境要求
- **Node.js**: v18.0.0 或更高版本

### 安裝與本地開發
1. **複製與安裝**

```bash
   git clone [https://github.com/MIN82814/CASHU.git](https://github.com/MIN82814/CASHU.git)
   cd CASHU
   npm install
````

2. **啟動即時熱更新開發伺服器**

```bash
   npm run dev
```

伺服器啟動後將自動開啟：`http://localhost:5173/CASHU/pages/index.html`

3. **生產環境構建與預覽**

```bash
   npm run build     # 編譯優化版本至 dist/ 資料夾
   npm run preview   # 本地預覽生產環境編譯結果
```

---

## 🚀 部署自動化 (CI/CD Workflow)

專案已配置基於 `gh-pages` 的自動化部署流水線，大幅簡化發布流程。

當代碼修改完成並推送到 GitHub 遠端倉庫後，僅需在終端機執行一行指令：

```bash
npm run deploy
```

**自動化構建行為**：
Vite 會自動啟動生產環境編譯，優化所有打包資產、編譯 SCSS 並處理 EJS 模板整合，隨後自動將 `dist/` 靜態檔案推送至遠端 `gh-pages` 分支。

---

## 📄 授權

此專案為跨領域團隊協作與學習用途作品。

```

```
