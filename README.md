# hexo-theme-apollo

a fork version of https://github.com/pinggod/hexo-theme-apollo

## 文档

- [中文文档](https://github.com/p7e4/hexo-theme-apollo/blob/master/doc%2Fdoc-zh.md)
- [Document](https://github.com/p7e4/hexo-theme-apollo/blob/master/doc%2Fdoc-en.md)

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

## License

MIT
