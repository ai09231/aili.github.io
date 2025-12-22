# aili.github.io

本仓库用于托管一个纯静态的 Three.js 小演示页面：`dex.html`（3D 发动机/曲柄滑块机构原理演示）。

- 在线预览：`https://aili.github.io/dex.html`
- 主要交互：鼠标拖拽/滚轮（OrbitControls 视角控制）、右上角滑块调节转速

## 技术栈

- 纯静态页面：HTML + ES Modules
- Three.js：通过 `unpkg` CDN 引入（`three@0.160.0`）

## 本地运行

由于使用了 ES Modules（`type="module"` + `importmap`），建议通过本地静态服务器访问，避免直接用 `file://` 打开导致的模块加载问题。

在仓库根目录执行任意一种方式：

- Python 3：`python -m http.server 5173`
- Node（如已安装）：`npx serve .`
- VS Code：安装 Live Server 扩展后右键“Open with Live Server”

然后在浏览器打开：

- `http://localhost:5173/dex.html`

## 目录结构

- `dex.html`：Three.js 演示主页面
- `README.md`：项目说明

## 说明

- 页面依赖 CDN 资源，离线环境无法正常加载 Three.js
- 推荐使用现代浏览器（需支持 ES Modules + importmap）
