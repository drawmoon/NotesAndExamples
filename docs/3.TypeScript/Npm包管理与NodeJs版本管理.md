# Npm 包管理与 NodeJs 版本管理

- [通过二进制文件安装](#通过二进制文件安装)
- [查看全局安装依赖包](#查看全局安装依赖包)
- [安装 NodeJs 管理工具](#安装-nodejs-管理工具)
- [安装 Npm 依赖包升级工具](#安装-npm-依赖包升级工具)
- [升级 Npm](#升级-npm)
- [卸载 Npm](#卸载-npm)

## 通过二进制文件安装

下载[Linux 二进制文件](https://nodejs.org/en/download/)

```bash
VERSION=v14.16.1
DISTRO=linux-x64
sudo mkdir -p /usr/local/lib/nodejs
sudo tar -xJvf node-$VERSION-$DISTRO.tar.xz -C /usr/local/lib/nodejs
```

设置系统环境变量

```bash
sudo vim /etc/profile.d/node.sh
```

将以下内容添加至文件中

```sh
VERSION=v14.16.1
DISTRO=linux-x64
export PATH=/usr/local/lib/nodejs/node-$VERSION-$DISTRO/bin:$PATH
```

保存后执行`source /etc/profile`刷新系统环境变量

## 查看全局安装依赖包

```bash
npm list -g --depth 0
```

## 安装 NodeJs 管理工具

```bash
npm install -g n
```

## 安装 Npm 依赖包升级工具

> 提供命令行图形界面，可以手动选择需要升级的依赖包

```bash
npm install -g npm-check
```

升级项目中的依赖包

```bash
npm-check -u

# 命令行图形界面，上下键可以移动选择，空格选中或取消选中
? Choose which packages to update. (Press <space> to select)

 Minor Update New backwards-compatible features.
>( ) typescript devDep  4.0.6  ❯  4.2.3  https://www.typescriptlang.org/

 Space to select. Enter to start upgrading. Control-C to cancel.
```

## 升级 Npm

```bash
npm install -g npm

# Or
npm install -g npm@7.8.0
```

## 卸载 Npm

```bash
npm uninstall -g npm
```
