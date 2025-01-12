nvmw-fix [![npm](https://img.shields.io/npm/v/nvmw-fix.svg?style=plastic)](https://npmjs.org/package/nvmw-fix) [![npm](https://img.shields.io/npm/dm/nvmw-fix.svg?style=plastic)](https://npmjs.org/package/nvmw-fix)
====

- [简体中文](README_zh.md) &#8195;&#8195; [English](README_en.md)


这是一个简单的切换全局Node.js的工具，无需配置环境变量，无需管理员权限，只需要安装npm包，使用cmd命令即可。

使用场景：公司内无法自由安装软件，但是可以安装npm包

## 安装

```shell
npm i -g nvmw-fix
```

## 使用

```shell

// 打开命令行终端

// 查看当前使用的Node.js版本
node -v 

// 查看此电脑所有Node.js版本
nvmw ls

// 安装指定版本的Node.js
nvmw install  v22.13.0

// 永久切换到指定版本的Node.js，全局生效
nvmw switch  v22.13.0

// 关闭此命令行终端，打开新的命令行终端，查看当前使用的Node.js版本
node -v

// 输出 v22.13.0，生效
```

所有命令列表如下：

```shell

nvmw install  <version>  // 安装指定版本的Node.js
nvmw uninstall  <version>  // 卸载指定版本的Node.js
nvmw use  <version>  // 暂时切换到指定版本的Node.js，仅当前命令行终端生效
nvmw deactivate  // 撤销当前命令行终端中 nvmw 的效果
nvmw switch  <version>  // 永久切换到指定版本的Node.js，全局生效，需要打开一个新的命令行
nvmw ls // 查看所有Node.js版本
nvmw ls-remote // 查看所有远程Node.js版本
nvmw cleanup // 清除过时的本地缓存

nvmw -h, --help    // 输出帮助信息
nvmw -V, --version  // 输出当前nvmw版本信息
```

## 注意事项

* 仅支持在Windows CMD中运行
* 此工具无法安装版本低于v4.5.0的Node
* 您必须先使用安装一个系统版本的[Node](https://nodejs.cn/download/)
* 从[nvmw](https://github.com/nanjingboy/nvmw)拉取分支修改bug而来，如果您之前使用过nvmw，使用前请先全局卸载nvmw

```shell
npm uninstall -g nvmw
```

## License
[MIT](http://www.opensource.org/licenses/MIT)
