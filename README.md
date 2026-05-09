# Mewna · GitHub Pages 設定

把這個資料夾的內容當成獨立 repo,推到 `gckenny/mewna`,啟用 GitHub Pages,網址就是 `https://gckenny.github.io/mewna/`。

## 步驟

```bash
# 1. 建立 repo(在 GitHub 上手動建,或用 gh)
gh repo create gckenny/mewna --public --description "Mewna · AI Sleep Companion · Privacy · Terms · Support"

# 2. 把這個 legal 資料夾當作 repo root push
cd ~/git/personal/AISleepMonitor/AppStoreSubmission/legal
git init
git add .
git commit -m "Mewna marketing + legal pages"
git branch -M main
git remote add origin git@github.com:gckenny/mewna.git
git push -u origin main

# 3. 啟用 GitHub Pages
gh repo edit gckenny/mewna --enable-pages
# 或用 web UI: Settings → Pages → Source: main / (root)
```

## 部署後 URL

- 首頁: https://gckenny.github.io/mewna/
- 隱私: https://gckenny.github.io/mewna/privacy.html
- 條款: https://gckenny.github.io/mewna/terms.html
- 支援: https://gckenny.github.io/mewna/support.html

App Store Connect 三個必填欄位填這些 URL 即可。

## 要修改

- 全部都是純 HTML + 內嵌 CSS,直接編輯 `.html` 檔
- 文字裡所有 `gckennyh@gmail.com` 是聯絡 email,可改
- `apple.com/app/mewna/id0000000000` 在 index.html 是 placeholder,App Store 上架後拿到 ID 再改
