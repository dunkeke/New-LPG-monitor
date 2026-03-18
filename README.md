# New-LPG-monitor

这是一个**纯静态 HTML 单页应用**（SPA 风格），无需 Node/npm、无需打包，直接双击 `index.html` 即可本地打开。

## 本地打开方式（HTML App）

### 方式 1：直接文件打开
1. 下载仓库后进入目录。
2. 直接双击 `index.html`。
3. 浏览器会以 `file://.../index.html` 形式打开页面。

### 方式 2：本地静态服务（推荐）
```bash
python -m http.server 8000
```
然后打开：`http://localhost:8000`

> 说明：页面不依赖后端 API，所有数据均在前端脚本中内置。

## GitHub Pages 部署方案

仓库已提供 `.github/workflows/deploy-pages.yml`：
- 在 `main` 分支有 push 时自动部署。
- 也可在 Actions 中手动触发 `workflow_dispatch`。

### 需要在仓库中确认的设置
1. 打开 GitHub 仓库 **Settings → Pages**。
2. Build and deployment 选择 **GitHub Actions**。
3. 确保默认分支为 `main`（或者按需把 workflow 触发分支改为你的主分支）。

部署完成后，访问：
`https://<你的GitHub用户名>.github.io/<仓库名>/`

## 目录结构

- `index.html`：完整前端页面（样式 + 交互 + 图表）
- `.github/workflows/deploy-pages.yml`：Pages 自动部署工作流

