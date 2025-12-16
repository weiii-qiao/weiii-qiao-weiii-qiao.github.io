# 个人主页 - Hugo Researcher主题

一个为GitHub Pages优化的个人履历和主页模板，基于[Hugo Researcher](https://github.com/ojroques/hugo-researcher)主题。

## 📸 特点

- ✨ 简洁优雅的单栏设计
- 🚀 GitHub Pages自动部署
- 📱 响应式设计
- 🎨 可自定义的样式
- 📐 支持KaTeX数学公式
- 🏃 快速构建和加载

## 🚀 快速开始

### 基本要求
- Hugo（extended版本）0.74.3+
- Git

### 本地开发

```bash
# 1. 克隆项目（包括主题子模块）
git clone --recurse-submodules <your-repo-url>
cd hugo-researcher-master

# 2. 本地预览
hugo server -D

# 访问 http://localhost:1313
```

### 部署到GitHub Pages

1. 创建仓库 `username.github.io`
2. 将项目文件推送到 `main` 分支
3. GitHub Actions会自动构建和部署
4. 访问 `https://username.github.io` 查看你的网站

详细部署说明请查看 [DEPLOYMENT.md](DEPLOYMENT.md)

## 📋 快速配置

### 编辑网站信息 (config.toml)

```toml
baseURL = "https://username.github.io/"
title = "Your Name"

[params]
  author = "Your Name"
  description = "Your personal description"
  
  [[params.socialIcons]]
    icon = "fab fa-github"
    url = "https://github.com/username"
```

### 编辑内容

- **首页**: `content/_index.md`
- **联系页**: `content/contact.md`

### 添加头像

将头像放在 `static/` 文件夹中，命名为 `avatar.jpg`

## 🎨 自定义

### 修改样式

编辑 `config.toml` 中的样式配置：

```toml
[params.style]
  fontFamily = "Inconsolata"
  fontSize = "14pt"
  pageWidth = "750px"
  colorBlack = "#222222"
  colorRed = "#dc3545"
```

### 启用数学公式

在markdown文件中添加 `math = true`：

```markdown
+++
title = "Page"
math = true
+++

$$E = mc^2$$
```

## 📁 项目结构

```
.
├── content/              # 网站内容
├── static/               # 静态文件（头像、favicon等）
├── layouts/              # 页面布局
├── assets/               # 样式资源
├── .github/workflows/    # GitHub Actions自动部署
└── config.toml           # 网站配置
```

## 📚 文档

- 详细部署指南: [DEPLOYMENT.md](DEPLOYMENT.md)
- 原始主题文档: [Hugo Researcher](https://github.com/ojroques/hugo-researcher)
- Hugo官方文档: [gohugo.io](https://gohugo.io/documentation/)

## 📄 许可证

[GPL-3.0 License](LICENSE)

## 🔗 相关资源

- 原始Jekyll主题: [ankitsultana/researcher](https://github.com/ankitsultana/researcher)
- Hugo版本主题: [ojroques/hugo-researcher](https://github.com/ojroques/hugo-researcher)
