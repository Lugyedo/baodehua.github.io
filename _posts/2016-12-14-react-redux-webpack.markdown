---
layout: post
title:  "使用 webpack + react + redux + es6 组件化前端项目"
date:   2016-12-14 10:37:15
categories: React
---
## React-工程化

### 要完成的功能
- 编译 jsx、es6、scss 等资源
- 自动引入静态资源到相应 html 页面
- 实时编译和刷新浏览器
- 按指定模块化规范自动包装模块
- 自动给 css 添加浏览器内核前缀
- 按需打包合并 js、css
- 压缩 js、css、html
- 图片路径处理、压缩、CssSprite
- 对文件使用 hash 命名，做强缓存
- 语法检查
- 全局替换指定字符串
- 本地接口模拟服务
- 发布到远端机

### 脚本构建工具配置
1. 生成package.json
`npm init`
2. 安装React和ReactDom模块
`npm i react react-dom redux --save`
3. 安装webpack
`npm install webpack --save-dev`
4. webpack配置
每个项目下都必须配置有一个 webpack.config.js
5. 安装jsx-loader
`npm install jsx-loader --save-dev`
6. 安装babel
`npm install babel`
7. 打包项目
`webpack --display-error-details`