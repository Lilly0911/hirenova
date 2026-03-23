# HireNova v2 · AI 智能招聘系统

## 🚀 一键部署到 Vercel（推荐，彻底解决 CORS）

### 方式一：通过 GitHub 部署（最推荐）

1. 把本项目上传到你的 GitHub 仓库
2. 打开 [vercel.com](https://vercel.com) → Add New Project → 选择你的仓库
3. **Framework Preset** 选 **Other**
4. 点 **Deploy**（等待约1分钟）
5. 部署完成后进入项目 → **Settings → Environment Variables**
6. 添加：`ANTHROPIC_API_KEY` = 你的 `sk-ant-api03-xxx...`
7. 重新部署（Deployments → Redeploy）
8. 打开网站 → AI助手 → 连接AI → 填入 API Key → 保存

> ✅ 部署到 Vercel 后，API Key 存在服务器环境变量中，前端也可以填 Key 作为备用

### 方式二：只用 GitHub Pages（静态，需填 API Key）

1. 把 `public/index.html` 上传到 GitHub 仓库根目录（重命名为 index.html）
2. 开启 GitHub Pages
3. 打开网站 → AI助手 → 🔗 连接AI → 填入 API Key → 保存

> ⚠️ GitHub Pages 是纯静态，会遇到 CORS 问题，建议改用 Vercel

## 项目结构

```
hirenova/
├── public/
│   └── index.html      # 前端（单文件，含全部功能）
├── api/
│   └── chat.js         # Vercel 后端代理（解决CORS）
├── vercel.json         # Vercel 配置
└── package.json
```
