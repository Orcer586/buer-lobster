# GitHub Pages 配置指南

## 本地仓库状态

仓库位置：`/root/.openclaw/workspace/buer-lobster`

已提交：
- ✅ index.html (首页)
- ✅ articles.html (文章列表)
- ✅ about.html (关于页面)
- ✅ articles/hello-world.html (第一篇文章)

## 配置 GitHub Pages

### 方法1：自动推送（需要 GitHub Token）

1. 在 GitHub 生成 Personal Access Token：
   - 访问 https://github.com/settings/tokens
   - 点击 "Generate new token (classic)"
   - 勾选 `repo` 权限（完整仓库访问）
   - 生成并复制 Token

2. 提供 Token 给我，我会自动配置推送

### 方法2：手动配置

在你的本地环境执行：

```bash
# 克隆仓库
git clone https://github.com/Orcer586/buer-lobster.git
cd buer-lobster

# 复制以下文件到仓库目录
# - index.html
# - articles.html
# - about.html
# - articles/hello-world.html

# 提交并推送
git add -A
git commit -m "🦞 初始化网站"
git push origin master
```

### 启用 GitHub Pages

1. 访问 https://github.com/Orcer586/buer-lobster/settings/pages
2. Source 选择 "Deploy from a branch"
3. Branch 选择 "master" / "/ (root)"
4. 点击 Save

等待几分钟后，网站将在 https://orcer586.github.io/buer-lobster 上线

## 每日文章自动发布

已配置定时任务：每天上午 8:00 自动生成文章

### 配置自动推送

提供 GitHub Token 后，我会更新脚本实现全自动发布：
- 生成文章
- Git 提交
- 推送到 GitHub
- GitHub Pages 自动部署

## 网站文件结构

```
buer-lobster/
├── index.html          # 首页
├── articles.html       # 文章列表
├── about.html          # 关于页面
└── articles/
    └── hello-world.html # 第一篇文章
```

所有样式已内联，无需额外 CSS 文件。
