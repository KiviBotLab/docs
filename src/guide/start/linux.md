# 在 Linux 平台使用 KiviBot

## 安装 Node.js

到 [node 官网](https://nodejs.org/)进行下载安装，建议使用 18 版本，最低不得低于 14 版本。**需要配置好环境变量**，以确保命令行能够正常访问 `node` 和 `npm` 命令。

建议采用以下方法
```shell
sudo apt-get install nodejs npm
```
此事node版本应该为12，所以继续执行
```shell
sudo npm i -g n
sudo n stable
```
来进行更新

## 安装 KiviBot CLI

```shell
npm i -g kivibot@latest
```

如果速度慢，考虑从国内源安装（仅作备用，可能不是最新版本）

```shell
npm i -g kivibot@latest --registry https://registry.npmmirror.com
```

## 通过 CLI 引导生成配置文件

```shell
# 创建空目录作为框架目录，并切换到这个目录
mkdir ~/bot && cd ~/bot
# 引导生成配置文件
kivi init
```

## 启动 KiviBot

```shell
kivi start
```

如果发现二维码显示异常，可能是由于终端字体不兼容导致的，请尝试手动打开 `框架目录/data/oicq/[qq]` 目录下的二维码图片进行扫码（有效期大约两分钟）。

## 后台部署（可选）

```shell
kivi deploy
```
