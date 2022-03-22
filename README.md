## Hello world!
+ 安装npm
+ 设定淘宝源
```shell
npm config set registry http://registry.npm.taobao.org/
```
+ 安装express web frame
```shell
npm i express --save
```
+ 编写代码
在根目录``server.js``中编写如下代码
```js
const express = require('express');
const app = express();

app.get('/', (req, res) => {
    res.send('Hello World!');
});

app.listen(3000, () => {
    console.log('Express web app on localhost:3000');
});
```
+ 运行代码
```shell
npm start
```
+ 在浏览器中访问``localhost:3000``

## 将node脚本像命令行工具一样运行
+ 编写脚本
```js
#! /usr/bin/env node
const [nodePath, scriptPath, name] = process.argv;
console.log('Hello', name);
```
+ 赋予权限
```shell
chmod 777 cli.js
```
+ 运行脚本
```shell
./cli.js HE
```