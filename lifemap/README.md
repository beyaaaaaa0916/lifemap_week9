# LifeMap｜人生探索地圖

LifeMap 是一個把人生願望整理成探索地圖的繁體中文單頁網站。它從既有的 LifeMap 作業延伸，將原有互動整理成可持續新增願望分類、示範內容與功能的專案，並以 `AGENTS.md` 明確記錄 AI 接手開發時要遵循的規則。

## 網站功能

- 新增、編輯願望，記錄分類、描述、動機、目標日期與完成心得。
- 以地圖地標及卡片呈現願望，快速查看每段旅程。
- 更新「尚未開始／進行中／已完成」狀態，並顯示整體完成率。
- 依關鍵字、分類與狀態搜尋篩選。
- 將願望清單匯出為 JSON 備份。
- 首次造訪會載入可編輯、可刪除的示範願望。

## 專案規則

修改前請先閱讀 [`AGENTS.md`](AGENTS.md)。新增內容時應遵守其中的資料格式、分類同步、版面風格與隱私規則。這使 AI 能按照同一套方式延伸功能，而不必每次重新猜測網站結構。

## 本機瀏覽

下載或複製專案後，直接以瀏覽器開啟 `index.html` 即可使用；不需要安裝套件或執行伺服器。每個瀏覽器各自保存自己的資料，清除瀏覽器資料可能會移除願望，請使用「匯出清單」備份。

## 部署到 GitHub Pages

1. 將整個專案資料夾推送到 GitHub Repository。
2. 在 Repository 的 **Settings → Pages → Build and deployment**，將 **Source** 設成 **GitHub Actions**。
3. 推送到 `main` 分支後，`.github/workflows/pages.yml` 會發布網站。
4. 在 Actions 頁面確認 `Deploy LifeMap to GitHub Pages` 成功，再由 Pages 設定頁開啟網站網址。

網站是靜態前端，不會接收或同步使用者資料。瀏覽器本機儲存和匯出 JSON 的設計也適用於 GitHub Pages。

## 專案結構

```text
LifeMap/
├── index.html                 # 單頁網站、樣式與互動
├── AGENTS.md                  # AI 延續開發規則
├── README.md                  # 專案介紹與使用／部署方式
└── .github/workflows/
    └── pages.yml              # GitHub Pages 自動部署
```

## 授權與素材

本專案以原有 LifeMap 作業為基礎延伸。地圖插畫使用頁面內建 SVG，無外部圖片或字型依賴。
