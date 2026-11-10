# Phychi 的博客

这是一个使用 Hugo 和 PaperMod 构建的静态博客，通过 GitHub Pages 免费发布。

计划发布的地址：<https://phychi.github.io/>

## 本地预览

```powershell
& "D:\CodexTools\hugo-0.169.0\hugo.exe" server -D
```

浏览器访问 `http://localhost:1313/`。

## 新建文章

在博客根目录打开 PowerShell，运行：

```powershell
& "D:\CodexTools\hugo-0.169.0\hugo.exe" new content --kind posts "posts/文章名称/index.md"
```

编辑生成的 `index.md`，完成后将 `draft` 改为 `false`。

文章图片放在 `index.md` 同一目录，然后通过相对路径引用：

```markdown
![图片说明](图片.webp)
```

## 发布

```powershell
git add .
git commit -m "更新博客"
git push
```

推送到 GitHub 的 `main` 分支后，GitHub Actions 会自动构建并发布网站。
