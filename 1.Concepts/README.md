# 一. 基本概念
## Entry
指定 webpack 从哪个模块开始构建内部依赖关系图
默认为 `./src/index.js` ，可以通过配置entry属性自定义入口文件或定义多个入口文件

## Output
指定在何处创建包以及如何命名这些文件。
文件默认打包在 `./dist` 目录下，主文件默认为 `./dist/main.js`
output.filename 设置打包文件的名称
output.path 设置打包路径 

## Loaders
webpack 仅能处理 javascript 和 JSON 文件。Loader 可以让 webpack 处理其它类型的文件。
loaders 在 webpack 配置中有两个属性
`test` 标识需要被转换的文件
`use` 表明使用哪个 Loader 进行转换

## Plugins
Loader 用来转换某些类型的模块，Plugin 用于执行更广泛的任务。例如打包优化，资源管理以及环境变量注入。
要使用plugin，要用 `require()` 引入它并将它加入 plugins 数组中
可以将一个插件引入多次以用于不同的目的，所以需要使用 new 来实例化插件

## Mode
mode 可以设置为 `development`、`production`、`none`, 默认为`production`
通过设置不同的mode可以启用每个环境对应的webpack内置优化

## Browser Compatibility
webpack 支持所有符合 ES5 的浏览器（不支持IE8及其以下版本），webpack 的 `import()` 和 `require.ensure()` 需要 Promise 的支持。
如果要支持旧版浏览器，在使用这些表达式之前需要加载 polyfill


## Environment
Node.js 8.x及以上版本

