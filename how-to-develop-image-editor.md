# 如何开发一款图片编辑器（基于html5）

> 最近开发了一个图片编辑器，类似于photoshop的网页版，源码参考自GitHub上，顺便也总结下使用html+js开发一个编辑器需要用到哪些知识点。

- 预览地址： [https://ps.gitapp.cn](https://ps.gitapp.cn)
- github地址：[https://github.com/photopea/photopea](https://github.com/photopea/photopea)

![首页效果](https://upload-images.jianshu.io/upload_images/3360192-d7f01e92e29b3a29.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/800)

## 架构设计


**选型**： jquery.js 和 blueimp-canvas.js都是强大的页面库，功能上类似，jquery.js比较新中文文档也多一些。Exif.js提供了 JavaScript读取图像的原始数据的功能扩展，例如：拍照方向、相机设备型号、拍摄时间、ISO感光度、GPS 地理位置等数据。
**要点**： 本项目使用的是分功能模块开发的方式，将菜单、左区域、语言、配置，都放在了不同的文件中，比如菜单是config-menu.js，语言是languages文件夹，类库是libs文件夹，各种模块放到modules文件夹，核心库放到了core里面，各种小工具放到了tools里面。如果同学们想深入了解各区域代码，可以定位到相应的文件夹下面查看。

## 代码结构

整个项目的代码分为三个部分，分别是css、js、html。入口文件是js文件夹中的main.js，入口页面文件是index.html。如图所示：

![src-pic.jpg](https://upload-images.jianshu.io/upload_images/3360192-1a4cbe3427f8f767.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


## 首页介绍

首页将各种css、js文件引入，其中bundle.js是主渲染文件（使用npm打包命令打包后会生成bundle.js文件）。

```
	<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
	<meta http-equiv="x-ua-compatible" content="IE=edge" />
	<title>在线PS</title>
	<meta name="description" content="." />
	<meta name="keywords"
		content="" />
	<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1.0, user-scalable=0" />
	<link rel="icon" sizes="192x192" href="images/favicon.png">

	<!-- Google -->
	<meta itemprop="name" content="在线PS网页版" />
	<meta itemprop="description" content="在线PS网页版是使用HTML5的免费在线图片编辑器..." />
	<!-- Twitter -->
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content="在线PS网页版" />
	<meta name="twitter:description" content="在线PS网页版是使用HTML5的免费在线图片编辑器..." />
	<!-- Facebook, Pinterest -->
	<meta property="og:title" content="在线PS网页版" />
	<meta property="og:type" content="article" />
	<meta property="og:url" content="https://ps.gitapp.cn" />
	<meta property="og:description" content="在线PS网页版是使用HTML5的免费在线图片编辑器..." />
	<meta property="og:site_name" content="在线PS网页版" />

	<script src="dist/bundle.js"></script>
```




## 参考知识

- [如何调整图片大小](https://ps.gitapp.cn/blog/ps/how-to-resize-image-photoshop.html)
- [开源常见issues问题](https://github.com/photopea/photopea/issues)
- [如何学习photoshop](https://juejin.cn/post/7288128426836574208)
- [用 Photoshop 做的 15 件创意事](https://blog.csdn.net/net19880504/article/details/133749756)
- [ps官网学习简介](https://helpx.adobe.com/cn/support/photoshop-china.html)

