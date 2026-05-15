# 部署到 GitHub Pages

## 第一次部署

### 1. 建 repo 並推上去

```bash
cd tide-repo            # 解壓後的資料夾名
git init
git add .
git commit -m "Initial commit: Tide v16"
git branch -M main

# 在 github.com 新建一個空 repo（建議名稱：tide），然後：
git remote add origin https://github.com/YOUR_USERNAME/tide.git
git push -u origin main
```

### 2. 在 GitHub 啟用 Pages

到 repo 頁面 → **Settings** → 左側 **Pages** → **Source** 選 **GitHub Actions**。

存檔後等 1–2 分鐘，回 repo 首頁右側會出現綠色 ✅ 的 deployment 訊息，網址在 `https://YOUR_USERNAME.github.io/tide/`。

### 3. 改 README 的網址

把 `README.md` 第一段那個 `YOUR_USERNAME` 換成你的 GitHub 帳號。

```bash
git add README.md
git commit -m "Update deploy URL"
git push
```

## 之後更新

只要 push 到 `main`，`.github/workflows/deploy.yml` 會自動重新部署。

```bash
git add .
git commit -m "Fix XXX"
git push
```

## 想自訂網址 / 私人測試

- **自訂網址**：Settings → Pages → Custom domain
- **私人測試**：免費的 GitHub Pages 不能設密碼，如果要對少數人保密，建議考慮：
  - 把 repo 設 Private，網址改用 [Cloudflare Pages](https://pages.cloudflare.com/) 或 [Netlify](https://netlify.com)（都有密碼保護）
  - 或乾脆把 `index.html` 用 LINE / Telegram 直接傳給朋友，他們存到手機桌面也能直接開
