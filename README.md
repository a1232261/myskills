# 許奕偉 — 作品集網站

自建 ComfyUI 生成管線、自訓 SDXL LoRA、開源影片模型本地部署，
以及三個可直接在瀏覽器執行的互動原型。

## 部署到 GitHub Pages

1. 在 GitHub 建一個新的 **public** repo，例如 `portfolio`。
2. 把這個資料夾裡的**所有內容**（含 `.nojekyll`）放進 repo 根目錄，commit 後 push。
3. repo → **Settings → Pages** → Source 選 **Deploy from a branch**，
   Branch 選 `main`、資料夾選 `/ (root)` → Save。
4. 約 1 分鐘後網址會是 `https://<你的帳號>.github.io/portfolio/`。

## 結構

```
index.html                 單頁作品集（所有 CSS/JS 內嵌）
favicon.svg
.nojekyll                  讓 GitHub Pages 原樣輸出檔案
assets/img/*.webp          圖片（已縮圖、已清除 EXIF/生成參數中繼資料）
assets/video/*.mp4 + .jpg  影片與封面
apps/fps/                  3-1 FPS 戰術訓練場
apps/werewolf/             3-2 狼人殺 AI 對決版
apps/robotdog/             4-1 機器狗藍牙遙控器
files/*.json               可下載的 ComfyUI 工作流與訓練參數
```

## 已知事項

- `index.html` 目前掛著 `<meta name="robots" content="noindex,nofollow">`，
  **搜尋引擎不會收錄**。想讓它被 Google 搜到，把第 5 行那一行刪掉即可。
- 三個原型都依賴 CDN（cdnjs / jsdelivr / unpkg / Google Fonts），需連網。
- `apps/werewolf` 需要使用者自行填入 Google AI Studio API Key，
  金鑰只存在使用者自己的瀏覽器 localStorage，**沒有任何金鑰寫死在程式碼裡**。
- `apps/robotdog` 需要 Chrome/Edge 的 Web Bluetooth 與對應硬體才能實際連線。
- 頁面上沒有放電話號碼，只留 email。要加的話改 `index.html` 的 `.meta` 與 footer。

## 尚未收錄（素材備妥後再加）

- 桌面精靈（Live2D 模型已收錄於第 7 節，桌寵程式尚未完成）
- 2c 教學／宣傳影片四支（檔案較大，建議走 YouTube 未列出再嵌入）
- 角色設計企劃「植姬時光」（是否公開待定）
