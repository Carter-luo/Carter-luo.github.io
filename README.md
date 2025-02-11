1. 创建新文章
在你的Hexo博客项目目录中，运行以下命令创建新文章：
bash复制
hexo new "文章标题"
例如，如果你想创建一篇名为“我的第一篇文章”的文章，可以运行：
bash复制
hexo new "我的第一篇文章"
这将在source/_posts目录下生成一个Markdown文件，文件名类似于我的第一篇文章.md。
2. 编辑文章
打开source/_posts目录，找到你刚刚创建的Markdown文件。使用文本编辑器（如VS Code）打开并编辑它。以下是一个简单的文章模板：
markdown复制
---
title: 我的第一篇文章
date: 2025-02-11 20:00:00
tags:
  - 示例
  - 教程
---

这里是文章的内容。你可以使用Markdown语法来格式化文本。

## 标题1

这是一个段落，包含一些文本内容。

### 标题2

这是另一个段落。
3. 生成静态文件
编辑完成后，运行以下命令生成静态文件：
bash复制
hexo generate
4. 本地预览
运行以下命令启动本地服务器，预览你的文章：
bash复制
hexo server
访问http://localhost:4000，你应该能看到你的文章。
5. 部署到GitHub Pages
确认文章内容无误后，运行以下命令将文章推送到GitHub Pages：
bash复制
hexo deploy
6. 检查GitHub仓库
登录到你的GitHub账户，进入Carter-luo.github.io仓库，检查文件是否已经上传成功。访问https://Carter-luo.github.io，你应该能看到你的文章。
7. 删除文章
如果你想删除文章，直接删除source/_posts目录下的Markdown文件即可。例如：
bash复制
rm source/_posts/我的第一篇文章.md
总结
通过上述步骤，你可以创建、编辑、预览和发布文章。以下是完整的命令流程：
创建新文章：
bash复制
hexo new "文章标题"
编辑文章：
打开source/_posts目录下的Markdown文件。
生成静态文件：
bash复制
hexo generate
本地预览：
bash复制
hexo server
部署到GitHub Pages：
bash复制
hexo deploy
如果你在过程中遇到任何问题，可以参考Hexo的官方文档或在评论区提问。祝你写作愉快！
