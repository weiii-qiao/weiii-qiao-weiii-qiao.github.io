# 个人主页 - Hugo Researcher

这是一个基于Hugo Researcher主题的个人主页项目，适配GitHub Pages自动部署。

## 📋 项目结构

```
.
├── archetypes/          # Hugo文章模板
├── assets/              # SCSS样式资源
├── content/             # 网站内容
│   ├── _index.md       # 首页/关于页面
│   └── contact.md      # 联系页面
├── layouts/             # 网站布局模板
├── static/              # 静态文件（favicon、avatar等）
├── .github/
│   └── workflows/
│       └── hugo.yml    # GitHub Actions自动部署配置
├── config.toml          # 网站配置文件
└── .gitignore           # Git忽略文件

```

## 🚀 快速开始

### 前置要求
- Hugo（extended版本）0.74.3+
- Git

### 本地开发

1. **克隆或下载项目**
   ```bash
   git clone <your-repo-url>
   cd hugo-researcher-master
   ```

2. **初始化主题子模块**
   ```bash
   git submodule init
   git submodule update
   ```
   
   或者在克隆时直接初始化：
   ```bash
   git clone --recurse-submodules <your-repo-url>
   ```

3. **本地预览**
   ```bash
   hugo server -D
   ```
   
   访问 http://localhost:1313 查看网站

4. **构建静态文件**
   ```bash
   hugo
   ```
   
   生成的网站文件在 `public/` 目录中

## ⚙️ 配置说明

### 修改config.toml

编辑项目根目录的 `config.toml` 文件来自定义网站：

```toml
# 替换为你的GitHub Pages地址
baseURL = "https://username.github.io/"

# 网站标题
title = "Your Name"

# 个人信息
[params]
  author = "Your Name"
  description = "Your personal description"
  
  # 社交媒体链接
  [[params.socialIcons]]
    icon = "fab fa-github"
    title = "GitHub"
    url = "https://github.com/your-username"
```

### 修改内容

- **首页/关于页面**: 编辑 `content/_index.md`
- **联系页面**: 编辑 `content/contact.md`

### 添加头像

将你的头像图片放在 `static/` 文件夹中，命名为 `avatar.jpg` 或 `avatar.png`

## 📤 部署到GitHub Pages

### 步骤1：创建GitHub仓库

1. 创建新仓库，名称为 `username.github.io`（其中username是你的GitHub用户名）
2. 克隆该仓库到本地

### 步骤2：上传项目文件

```bash
# 将项目文件复制到仓库中
cp -r hugo-researcher-master/* username.github.io/

cd username.github.io

# 初始化git并推送
git add .
git commit -m "Initial commit"
git push -u origin main
```

### 步骤3：配置GitHub Actions

项目已包含 `.github/workflows/hugo.yml` 工作流文件，GitHub会自动：

1. 检测主分支上的推送
2. 使用Hugo构建网站
3. 将静态文件部署到GitHub Pages

### 步骤4：启用GitHub Pages

在GitHub仓库设置中：

1. 进入 Settings > Pages
2. Source 选择 "Deploy from a branch"
3. Branch 选择 "gh-pages" 和 "/ (root)"
4. 保存

几分钟后，你的网站将在 `https://username.github.io` 上线！

## 🎨 自定义样式

编辑 `config.toml` 中的样式部分：

```toml
[params.style]
  fontFamily = "Inconsolata"      # 字体族
  fontSize = "14pt"               # 字体大小
  pageWidth = "750px"             # 页面宽度
  colorBlack = "#222222"          # 主色调
  colorRed = "#dc3545"            # 强调色
```

## 📝 使用KaTeX数学公式

在内容中启用数学公式：

```markdown
+++
title = "页面标题"
math = true  # 启用KaTeX
+++

$$
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix}
$$
```

## 🔗 主题来源

- **原主题**: [ankitsultana/researcher](https://github.com/ankitsultana/researcher)
- **Hugo版本**: [ojroques/hugo-researcher](https://github.com/ojroques/hugo-researcher)

## 📄 许可证

本项目采用 GPL-3.0 许可证。详见 [LICENSE](LICENSE) 文件。

## 💡 常见问题

### Q: 如何添加新页面？
A: 在 `content/` 目录中创建新的 `.md` 文件，然后在 `config.toml` 的菜单中添加链接。

### Q: 网站没有自动部署？
A: 检查 `.github/workflows/hugo.yml` 是否存在，并确保仓库的Actions选项卡中没有失败的运行记录。

### Q: 如何修改菜单？
A: 编辑 `config.toml` 中的 `[menu.main]` 部分。

### Q: 本地预览和部署效果不一致？
A: 确保 `config.toml` 中的 `baseURL` 正确设置，本地可使用 `hugo server` 预览，不受baseURL影响。

## 📞 支持

如有问题，请查看：
- [Hugo文档](https://gohugo.io/documentation/)
- [主题GitHub仓库的Issues](https://github.com/ojroques/hugo-researcher/issues)

---

**祝你的个人主页运营顺利！** 🎉

