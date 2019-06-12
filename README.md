# xeline 计算端
[![Build Status](https://travis-ci.org/xel-software/xeline.svg?branch=master)](https://travis-ci.org/xel-software/xeline)

xeline主要功能是向xel计算网络提交任务的客户端

重要提示：这个不是XEL钱包, 因为不包含管理硬币一些关键功能，如果你需要管理你的硬币建议使用官方钱包（安装版钱包或网络钱包）

## 安装

### 二进制
最快的方法是使用官方二进制文件 : https://github.com/xel-software/xeline/releases

### from sources
- install nodeJS (https://nodejs.org)
- clone this repository
- run `npm install` to setup dependencies
- run `npm start` to launch the client

## build
- install yarn
- run `yarn && yarn package:mac` to build a macOS client (only from a macOS host)
- run `yarn && yarn package:linux` to build a linux client
- run `yarn && yarn package:win` to build a windows client (only from a windows host)

You can also build a release using docker :
```
docker run --rm -ti \
 --env-file <(env | grep -iE 'DEBUG|NODE_|ELECTRON_|YARN_|NPM_|CI|CIRCLE|TRAVIS_TAG|TRAVIS|TRAVIS_REPO_|TRAVIS_BUILD_|TRAVIS_BRANCH|TRAVIS_PULL_REQUEST_|APPVEYOR_|CSC_|GH_|GITHUB_|BT_|AWS_|STRIP|BUILD_') \
 --env ELECTRON_CACHE="/root/.cache/electron" \
 --env ELECTRON_BUILDER_CACHE="/root/.cache/electron-builder" \
 -v ${PWD}:/project \
 -v ${PWD##*/}-node-modules:/project/node_modules \
 -v ~/.cache/electron:/root/.cache/electron \
 -v ~/.cache/electron-builder:/root/.cache/electron-builder \
 electronuserland/builder:wine \
 /bin/bash -c "yarn && yarn package:windows"
 ```


----
## 帮助改进


  - 我们乐见你多提交请求
  - 我们喜欢问题（实际解决的问题）
  - 在任何事情上，请确保留下你的意见
  - 在问题跟踪上可以协助其他人
  - 审核现有代码和提交请求

----
## 故障排除

  - UI错误或追踪？
    - 汇报在GITHUB上

----
## 更多消息

  - on discord : https://link.xel.org/discord
