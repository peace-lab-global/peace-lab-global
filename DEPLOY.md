# GitHub Pages 部署指南

## 方式一：使用 GitHub Actions（推荐）

### 步骤 1: 配置 GitHub Pages 设置

1. 进入仓库的 **Settings** 页面
2. 左侧菜单选择 **Pages**
3. **Build and deployment** 部分：
   - Source 选择：**GitHub Actions**
   - 保存设置

### 步骤 2: 推送代码

```bash
git add .
git commit -m "添加 GitHub Actions 自动部署配置"
git push
```

### 步骤 3: 自动部署

- 每次推送到 `main` 分支会自动触发部署
- 访问 `https://allen-galler.github.io/peace-lab-global/` 查看结果

---

## 方式二：手动部署

### 步骤 1: 配置 GitHub Pages 设置

1. 进入仓库的 **Settings** 页面
2. 左侧菜单选择 **Pages**
3. **Build and deployment** 部分：
   - Source 选择：**Deploy from a branch**
   - Branch 选择：`gh-pages` 分支，文件夹：`/(root)`
   - 保存设置

### 步骤 2: 手动构建并部署

```bash
# 1. 安装依赖
npm install

# 2. 构建项目
npm run build

# 3. 部署到 gh-pages 分支
npx gh-pages -d dist

# 或者安装 gh-pages 后使用
npm install -D gh-pages
npx gh-pages -d dist
```

---

## 配置说明

### 修改部署路径

如果你的仓库名不是 `peace-lab-global`，需要修改 `vite.config.js`：

```javascript
export default defineConfig({
  base: '/your-repo-name/',  // 修改为你的实际仓库名
  build: {
    outDir: 'dist',
    assetsDir: 'assets'
  }
})
```

### 自定义域名（可选）

1. 在仓库根目录创建 `CNAME` 文件
2. 文件内容填写你的域名（如 `www.peacelab.com`）
3. 在域名提供商处配置 DNS 记录

---

## 常见问题

### Q: 部署后页面样式丢失？
A: 检查 `vite.config.js` 中的 `base` 路径是否正确，应该与仓库名一致。

### Q: GitHub Actions 失败？
A: 检查仓库设置中 Pages 的 Source 是否选择了 "GitHub Actions"。

### Q: 如何手动触发部署？
A: 进入 GitHub 仓库的 Actions 页面，选择 "Deploy to GitHub Pages"，点击 "Run workflow"。

---

## 访问地址

部署成功后，通过以下地址访问：

```
https://allen-galler.github.io/peace-lab-global/
```

*注意：将 `allen-galler` 替换为你的 GitHub 用户名，`peace-lab-global` 替换为仓库名*
