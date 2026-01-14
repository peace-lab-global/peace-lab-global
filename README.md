# 平静实验室 Peace Lab

心理自助频道主页

## 快速开始

### 安装依赖
```bash
npm install
```

### 开发模式
```bash
npm run dev
```

### 构建生产版本
```bash
npm run build
```

### 预览构建结果
```bash
npm run preview
```

## 项目结构

```
peace-lab-global/
├── index.html          # 主页面
├── style.css           # 样式文件
├── vite.config.js      # Vite 配置
├── package.json        # 依赖配置
├── .gitignore         # Git 忽略文件
└── README.md          # 项目说明
```

## 部署

### GitHub Pages（推荐）

详细部署步骤请查看 [DEPLOY.md](./DEPLOY.md)

**快速部署：**

1. 在 GitHub 仓库设置中启用 GitHub Pages（Source 选择：GitHub Actions）
2. 推送代码，自动触发部署
3. 访问 `https://allen-galler.github.io/peace-lab-global/`

### 其他平台

构建后，将 `dist` 目录部署到 Netlify、Vercel、CloudBase 等平台。

## 配置说明

### 修改部署路径
编辑 `vite.config.js` 中的 `base` 配置：

```js
export default defineConfig({
  base: '/your-repo-name/',  // 修改为你的仓库名
  // ...
})
```

### 修改配色
编辑 `style.css` 中的 CSS 变量：

```css
:root {
  --primary-color: #6a89cc;      /* 主色 */
  --secondary-color: #4a69bd;    /* 辅助色 */
  --accent-color: #82ccdd;       /* 强调色 */
  /* ... */
}
```

### 修改内容
直接编辑 `index.html` 中的文本内容即可。

## 平台账号

各平台主账号同名：**平静实验室 PeaceLab**

- 图文：微信公众号、小红书、知乎、微博
- 视频：微信视频号、哔哩哔哩、抖音
- 博客：小宇宙、喜马拉雅、Apple Podcast
- 音乐：网易云音乐

## 联系方式

- 邮箱：allengaller@qq.com
- 微信：allengaller
