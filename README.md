# dim
可以让弹窗背景变为高斯模糊(毛玻璃效果)  或者调用本工具类返回一个被模糊的bitmap,内含截取activity快照方法

[TOC]

可以让弹窗背景变为高斯模糊(毛玻璃效果)  或者调用本工具类返回一个被模糊的bitmap,内含截取activity快照方法


###  1. 弹出一个 弹窗背景为底层界面的高斯模糊##
![效果图](http://img.blog.csdn.net/20161211130813773?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvcWZhbm1pbmd5aXE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

	使用: 
	 1. 下载源码关联依赖
	 2. 调用工具类FMYImgUtil.getDialog即可
	如下

```java
 View inflate =getLayoutInflater().inflate(R.layout.activity_second, null);
 //第一个参数上下文 
 //第二个参数 填充view 
 //第三个参数 模糊力度1-25 (超出标准自动为25 低于标准自动为1)
 Dialog dialog = FMYImgUtil.getDialog(this, inflate, 25);
 dialog.show();
```

###  2. 返回一个高斯模糊图片##

```java
//第一个参数你想高斯模糊的图片 
//第二个参数 上下文
//第三个参数 模糊力度1-25
//返回一个被高斯模糊的图片
 Bitmap fmyimg = FMYImgUtil.getFMYIMG(bitmap, activity, randle);
```

###  3. 返回activity的快照##
说白了就是截屏

```java
//第一个参数上下文
//返回此activity快照图
    Bitmap bitmap = FMYImgUtil.takeScreenShot(activity);
```
