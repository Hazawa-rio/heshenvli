# 和善里 · 旅遊導覽網站

這是一個單頁 HTML 網站（首頁 + 兩則公告內頁 + 五個待補分頁骨架），使用純 HTML／CSS／JavaScript 製作，沒有任何建置流程，可直接部署到 GitHub Pages。

## 檔案結構

```
site/
├── index.html          網站主檔案（GitHub Pages 會自動以此為首頁）
├── .nojekyll            告訴 GitHub Pages 不要用 Jekyll 處理這個網站
└── assets/
    ├── logo.png          LOGO（跨頁不消失）
    ├── favicon.png        瀏覽器分頁小圖示
    ├── home-hero.jpg       首頁主圖
    ├── announcement-a.jpg  公告 A 圖片
    └── announcement-b.jpg  公告 B 圖片
```

## 部署到 GitHub Pages 的步驟

1. 在 GitHub 上新增一個 repository（例如 `heshan-li-guide`）。
2. 把這個 `site` 資料夾裡的**所有檔案（含 `.nojekyll`）**上傳到 repository 的根目錄（或 `main` 分支）。
   - 用網頁介面拖曳上傳，或用 `git add . && git commit -m "init" && git push` 皆可。
3. 到 repository 的 **Settings → Pages**。
4. Source 選擇 `Deploy from a branch`，Branch 選 `main`（或你上傳的分支）、資料夾選 `/ (root)`，儲存。
5. 等 1–2 分鐘，GitHub 會給你一個網址，格式通常是：
   `https://<你的帳號>.github.io/<repository名稱>/`
6. 之後只要修改 `index.html` 或 `assets/` 裡的檔案並重新 push，網站就會自動更新。

## 之後如何編輯內容

- **文字**：直接用文字編輯器打開 `index.html`，搜尋你要改的中文字修改即可。
- **圖片**：把新照片放進 `assets/` 資料夾，檔名跟原本的圖片一樣（例如新的公告圖片一樣命名為 `announcement-a.jpg`）直接覆蓋，就不用改 HTML 裡的路徑。若要用不同檔名，記得同步修改 `index.html` 裡對應的 `src="assets/...jpg"`。
