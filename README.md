# BigWaterMelon HTML5 部署说明

这是一个由 Godot 导出的 HTML5 游戏静态包，可部署到 **GitHub Pages** 或 **Vercel**。

## 文件结构要求

请确保以下文件保持在同一目录（仓库根目录）：

- `MakingBigWatermelon.html`
- `MakingBigWatermelon.js`
- `MakingBigWatermelon.wasm`
- `MakingBigWatermelon.pck`
- 图标与启动图等资源文件（`.png`）

仓库已包含 `index.html`，会自动跳转到 `MakingBigWatermelon.html`，便于直接通过站点根路径访问游戏。

## 方式一：GitHub Pages

1. 打开仓库页面：`Settings` → `Pages`
2. 在 `Build and deployment` 中选择：
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/ (root)`
3. 保存后等待部署完成
4. 访问地址：
   - `https://<你的用户名>.github.io/BigWaterMelon_html/`

> 若你直接访问 `https://<你的用户名>.github.io/BigWaterMelon_html/MakingBigWatermelon.html` 也可以运行。

## 方式二：Vercel（推荐）

1. 登录 Vercel 并导入该 GitHub 仓库
2. Framework Preset 选择 `Other`（或保持静态站点默认）
3. 保持无构建步骤：
   - Build Command: 留空
   - Output Directory: `.`
4. 点击 Deploy

仓库中的 `vercel.json` 已配置关键响应头：

- `Cross-Origin-Embedder-Policy: require-corp`
- `Cross-Origin-Opener-Policy: same-origin`

这对 Godot Web 运行环境更友好。
