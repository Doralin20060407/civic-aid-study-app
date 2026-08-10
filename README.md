# CIVIC × AID — Humanitarian Aid × Civil Society Study App

這是一個可直接部署到 **GitHub Pages** 的靜態 Web App / PWA。

## 功能

- 八篇連貫閱讀路線
- 八篇資料庫與深度統整
- 全文搜尋
- 跨篇主題比較
- 詞彙表
- 測驗
- 深色模式
- 閱讀進度
- 每篇私人筆記（存在瀏覽器 `localStorage`）
- PWA：可加入手機主畫面
- 基本離線快取

## 最快部署方式：GitHub Pages

1. 在 GitHub 建立一個新的 repository，例如：
   `civic-aid-study-app`

2. 把這個資料夾內的所有檔案上傳到 repository **根目錄**：
   - `index.html`
   - `manifest.webmanifest`
   - `sw.js`
   - `icons/`

3. 進入 repository 的：
   **Settings → Pages**

4. 在 **Build and deployment**：
   - Source：`Deploy from a branch`
   - Branch：`main`
   - Folder：`/ (root)`
   - 按 **Save**

5. 等待 GitHub 部署完成。網址通常會是：

   `https://你的GitHub帳號.github.io/civic-aid-study-app/`

## 手機變成 App

網站部署完成後：

### iPhone / iPad
Safari 開啟網站 → 分享 → **加入主畫面**

### Android
Chrome 開啟網站 → 選單 → **Add to Home screen / Install app**

## 更新內容

修改 `index.html` 後 push 到 GitHub 即會自動重新部署。

如果更新後 PWA 仍顯示舊版，可修改 `sw.js` 第一行，例如：

`const CACHE = 'civic-aid-study-v2';`

讓瀏覽器建立新的 cache。

## 注意

閱讀進度與筆記存在每一台裝置自己的瀏覽器 localStorage。
因此：
- 不需要登入
- 不會上傳到 GitHub
- 換瀏覽器／清除網站資料後不會自動同步

如果日後要跨裝置同步，需要再接資料庫或登入系統（例如 Supabase / Firebase）。
