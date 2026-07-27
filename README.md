# Ivy 的学习花园

一个使用 Hexo 和 Fluid 主题构建的学习笔记与技术博客，发布地址为 <https://ivylinice.github.io/myblog/>。

## 本地开发

需要 Node.js 22（可使用 `nvm use` 读取 `.nvmrc`）。

```bash
npm install
npm run server
```

浏览器访问终端显示的本地地址预览网站。

## 写一篇新文章

```bash
npx hexo new "文章标题"
```

文章会创建在 `source/_posts/`。在文件顶部填写 `categories`、`tags` 和 `description`，然后使用 Markdown 写正文。文章封面等资源可放入同名文章资源目录中。

## 常用命令

```bash
npm run clean    # 清除生成文件
npm run build    # 生成静态网站到 public/
npm run server   # 本地预览并监听修改
```

## 发布到 GitHub Pages

1. 确认仓库默认分支是 `main`，并推送本项目文件。
2. 在 GitHub 仓库的 **Settings → Pages** 中，把部署源设置为 **GitHub Actions**。
3. 推送到 `main` 后，`.github/workflows/deploy.yml` 会自动构建并发布网站。

站点配置中的 `url` 和 `root` 已为项目站点 `ivylinice.github.io/myblog` 设置；如果更改仓库名或绑定自定义域名，请同步更新 `_config.yml`。
