# Sam Gu 个人求职网站（Static Portfolio Site）

本项目是面向课程作业与长期维护使用的 GitHub Pages 兼容静态个人网站，内容基于 `sam_gu_codex_project_brief.md` 的要求构建。

## 目录结构

- `index.html`：首页
- `about/index.html`：关于页面
- `skills/index.html`：技能页
- `projects/index.html`：项目总览
- `projects/*/index.html`：六个项目详情页
- `resume/index.html`：简历页
- `contact/index.html`：联系方式
- `blog/index.html`：博客列表页
- `blog/*/index.html`：四篇博客占位详情页
- `styles/main.css`：统一样式
- `.nojekyll`：GitHub Pages 兼容文件
- `assets/resume/sam-gu-resume.html`：简历下载占位文件（本地版本）
- `docs/`：Obsidian 过程文档（中文）

## 本地预览

在项目目录下直接双击 `index.html` 打开，或用任意静态服务器查看：

```bash
python3 -m http.server 8080
```

访问 <http://localhost:8080>。

## 部署到 GitHub Pages

1. 提交全部文件到仓库。
2. 仓库设置 -> Pages。
3. 选择分支和根目录（或 Docs 目录，如按需调整）。
4. 确认 `.nojekyll` 存在。
5. 检查相对路径是否正确。

## 相对链接策略

网站内全部使用相对链接，支持在 GitHub Pages 静态站点路径下直接访问。
