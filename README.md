# PhiCommunityAPP

# 这里是哪里

这里是[PhiCommunity](https://github.com/Yuameshi/PhiCommunity)的客户端仓库，目前只有Android客户端，使用Cordova开发。

# 构建指南

## 1.克隆PhiCommunity仓库

执行以下命令，克隆并构建PhiCommunity可浏览网页：

```sh
git clone https://github.com/Yuameshi/PhiCommunity
cd ./PhiCommunity/
sudo npm install webpack webpack-cli -g
npm install
npm run build
mv ./dist/ ../www/
cd ..
rm -rf ./PhiCommunity/*
```
或者直接克隆`gh-pages`分支
```sh
git clone -b gh-pages https://github.com/Yuameshi/PhiCommunity www
rm -rf www/.git/*
```

## 2.开始构建
>注意：在构建前请确保您的系统已经安装了`gradle`，`Android SDK 32`，`JDK 8`。
```sh
# 安装构建工具
npm install -g cordova
npm install
#配置平台
npm run add-platform:android
#确保依赖都搞定
npm run check
#构建Debug版本
npm run build:debug
#输出目录在./platforms/android/app/build/outputs/apk/目录下
#npm run build:release
#如需构建release版本请先配置build.json（build.sample.json为模板）
```