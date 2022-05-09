# hexo-theme-apollo

a fork version of https://github.com/pinggod/hexo-theme-apollo

## 安装

``` bash
hexo init Blog
cd Blog
npm install
npm install --save hexo-renderer-pug hexo-generator-feed
git clone --depth 1 https://github.com/p7e4/hexo-theme-apollo.git themes/apollo
```

## 启用

修改 `_config.yml` 的 `theme` 配置项为 `apollo`:

```yaml
theme: apollo

# 生成订阅源
feed:
  enable: true
  type: atom
  path: atom.xml
  limit: 20
  hub:
  content:
  content_limit: 140
  content_limit_delim: ' '
  order_by: -date
  icon: favicon.png
  autodiscovery: true
  template:
```

## 更新

``` bash
cd themes/apollo
git pull
```

## Meta Description

如果你想设置页面的 meta description 信息，请在每篇 markdown 文件的头部添加 `desc` 字段信息——更实用的方式是在 scaffolds 文件夹中，将 `desc` 配置到常用模板中去，示例如下：

```md
title: Lorem ipsum dolor
date: 2015-12-31 14:49:13
desc: Lorem ipsum dolor sit amet, consectetur.
---

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Totam, non numquam saepe ex ut. Deleniti culpa inventore consectetur nam saepe!
```

生成结果:

```html
<meta name="description" content="Lorem ipsum dolor sit amet, consectetur.">
```

如果没有配置该信息，Hexo-theme-apollo 会使用 `page.title` 和 `page.author` 来配置该标签。

## 文章摘要

如果你想创建文章摘要用于向读者展示文章的核心内容，那么需要在文章摘要之后其他内容之前添加 HTML 注释标签 `<!--more-->`，使用方法如下图所示：

![https://cloud.githubusercontent.com/assets/9530963/14064341/0fa3c754-f432-11e5-8ad7-5d063d4a0886.png](https://cloud.githubusercontent.com/assets/9530963/14064341/0fa3c754-f432-11e5-8ad7-5d063d4a0886.png)

## 警告块

使用警告块需要 `div` 标签和 `tip` 类名：

```html
<div class="tip">
    预处理器很强大，但它只是编写 CSS 的辅助工具。出于对扩展和维护等方面的考虑，在大型项目中有必要使用预处理器构建 CSS；但是对于小型项目，原生的 CSS 可能是一种更好的选择。不要肆意使用预处理器！
</div>
```

## License

MIT
