# Chris Chen 的部落格

網站：https://cczy9498.github.io/

使用 Hugo 0.167.0 與 [Stack v4.0.3](https://github.com/CaiJimmy/hugo-theme-stack)。主題以 Git submodule 固定版本，保留原作者授權與頁尾署名。

## 本機預覽（PowerShell）

```powershell
cd D:\CodingProject\cczy9498.github.io
.\.tools\hugo\hugo.exe server -D
```

開啟 http://localhost:1313/。按 Ctrl+C 停止。

## 新增文章

```powershell
.\.tools\hugo\hugo.exe new content post/my-new-post/index.md
```

編輯文章，將 `draft: true` 改為 `draft: false` 即可發佈。圖片可放在同一個文章資料夾。

## 發佈

將變更提交並推送至 `main`，GitHub Actions 會自動建置及部署 GitHub Pages。推送時請使用個人帳號 **cczy9498**，勿使用工作帳號。

```powershell
git add .
git commit -m "Add a new post"
git push origin main
```

## 換電腦

```powershell
git clone --recurse-submodules https://github.com/cczy9498/cczy9498.github.io.git
```

另行安裝 Hugo extended 0.167.0。本機的 `.tools` 不會上傳。

網站名稱、簡介與選單在 `hugo.toml`；關於頁在 `content/page/about/index.md`。

## 驗證建置

```powershell
.\.tools\hugo\hugo.exe --gc --minify
```
