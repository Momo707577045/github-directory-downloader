## [工具在线地址](http://blog.luckly-mjw.cn/tool-show/github-directory-downloader/index.html)，推荐使用 chrome 浏览器。

## 使用方式

* 打开想要下载的 github 文件夹，如 facebook 的 react-dom 文件夹，则打开该页面。
![](http://upyun.luckly-mjw.cn/Assets/github-directory-downloader/001.jpeg)
* 复制页面链接，粘贴到本工具输入框。
![](http://upyun.luckly-mjw.cn/Assets/github-directory-downloader/002.jpeg)
* 点击下载。
![](http://upyun.luckly-mjw.cn/Assets/github-directory-downloader/003.jpeg)

## 背景

* github 不支持部分文件下载，只能下载整个项目。
* github 国内网速较慢，只能下载整个项目需要等待很长时间。譬如 facebook 的 react 项目，有时候我们只想下载 [react-dom](https://github.com/facebook/react/tree/master/packages/react-dom) 来学习。但却要下载包含 react-js 等 35 各其他功能的整个项目。导致无谓的时间浪费。
* 网络上有相关解决方案，譬如修改 svn，修改 git 路径等，但均有一定使用成本和软件依赖。本项目意在将使用成本降到最低。
![](http://upyun.luckly-mjw.cn/Assets/github-directory-downloader/005.jpg)

## 特点

* 无依赖，无需安装软件，不需要依赖 svn，甚至连 git 都不需要。有浏览器即可使用。
* 操作简单，复制 github 页面链接，点击下载即可。
* 支持特定分支和特定 tag 的文件下载，精确到单文件下载。
![](http://upyun.luckly-mjw.cn/Assets/github-directory-downloader/006.jpg)

### 功能说明

![](http://upyun.luckly-mjw.cn/Assets/github-directory-downloader/004.jpeg)

* 【解析下载】输入 github 链接，点击下载文件。
* 【重新下载错误文件】当部分文件下载失败时，点击该按钮，重新下载错误文件。
* 【强制下载现有文件】将已经下载好的文件强制整合下载。可以提前观看已经下载的文件。该操作不影响当前下载进程。
* 【文件条】对应每一个文件的下载情况。「灰色」：待下载，「绿色」：下载成功，「红色」：下载失败。点击红色文件栏可重新下载对应错误文件。

## 特别说明

* 项目使用到 github 提供的开放性 API，故仅支持 github 文件下载。不支持 gitlab，gitee 等平台。
* 目标仓库需为公开仓库，否则无权限下载。
![](http://upyun.luckly-mjw.cn/Assets/github-directory-downloader/006.jpeg)

## 原理

* 文件下载使用的是 [github 开放 API](https://docs.github.com/cn/rest/reference/repos)，如「罗列所有分支」「罗列所有tag」「下载文件」等
* 文件压缩，使用的是 [jszip 库](https://github.com/Stuk/jszip#readme)

## [项目源码](https://github.com/Momo707577045/github-directory-downloader)

* 项目只是简单的功能组合，都比较简单。
* 代码没有做优化，理解思路，看看就好。
![](http://upyun.luckly-mjw.cn/Assets/github-directory-downloader/007.jpeg)
