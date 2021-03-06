---
title: SharePoint2007安装图文详解二：安装AD（活动目录）及DNS
date: 2011-01-10
categories: [MOSS]
tags: [AD, SharePoint]
---

在上一篇[SharePoint2007安装图文详解一](http://blog.fwhyy.com/2011/01/iis-install/)：安装IIS及相关组件中已经介绍了IIS及相关组件的安装，本篇将详细介绍AD（活动目录）的安装。

打开“管理您的服务器”，点击“添加或删除角色”

![2011-01-09_114808](http://fwhyy.com/img/post/2011-01-09_114808.gif)

点击“添加或删除角色”后弹出“配置你的服务器向导”对话框

![2011-01-09_214602](http://fwhyy.com/img/post/2011-01-09_214602.gif)

点击下一步进入如下对话框

![2011-01-09_215159](http://fwhyy.com/img/post/2011-01-09_215159.gif)

数秒后，进入到下面视图

![2011-01-09_220636](http://fwhyy.com/img/post/2011-01-09_220636.gif)

选择“域控制器”后点击“下一步”

![2011-01-09_221344](http://fwhyy.com/img/post/2011-01-09_221344.gif)

点击“下一步”

![2011-01-09_222512](http://fwhyy.com/img/post/2011-01-09_222512.gif)

随之便出现下面的对话框

![2011-01-09_222554](http://fwhyy.com/img/post/2011-01-09_222554.gif)

点击“下一步”

![201101110942371851](http://fwhyy.com/img/post/201101110942371851.gif)

继续“下一步”

![2011-01-09_222702](http://fwhyy.com/img/post/2011-01-09_222702.gif)

选择“新域的域控制器”，点击“下一步”

![2011-01-09_222835](http://fwhyy.com/img/post/2011-01-09_222835.gif)

选择“在新林中的域”，点击下一步

![2011-01-09_222921](http://fwhyy.com/img/post/2011-01-09_222921.gif)

输入“新域的DNS全名”，如上图中我输入的fwhyy.com ， 点击下一步

![2011-01-09_223113](http://fwhyy.com/img/post/2011-01-09_223113.gif)

上图中的“域NetBIOS名”默认就好，一般不做修改，点击下一步

![2011-01-09_223228](http://fwhyy.com/img/post/2011-01-09_223228.gif)

AD数据库的保存路径保持默认就好，如果需要您可以修改为你想要存放的路径，然后点击“下一步”

![2011-01-09_223350](http://fwhyy.com/img/post/2011-01-09_223350.gif)

SYSVOL文件夹的位置也不做修改，点击“下一步”

![2011-01-09_223509](http://fwhyy.com/img/post/2011-01-09_223509.gif)

出现上图的窗口说明在安装AD前没有安装DNS，当然我们可以在之前先装好DNS再安装AD，此次安装中我选择的是选择上图对话框中的第二项，在安装AD的同时安装DNS。选择第二项后，点击“下一步”

![2011-01-09_223815](http://fwhyy.com/img/post/2011-01-09_223815.gif)

选择“只与Windows 2000 或 Windows Server 2003 操作系统兼容的权限”，点击“下一步”

![2011-01-09_225001](http://fwhyy.com/img/post/2011-01-09_225001.gif)

输入密码，点击“下一步”

![2011-01-09_225034](http://fwhyy.com/img/post/2011-01-09_225034.gif)

继续“下一步”，就会开始安装了

![2011-01-09_225123](http://fwhyy.com/img/post/2011-01-09_225123.gif)

稍等几分钟，就会出现安装成功的窗口，如下图

![2011-01-09_225700](http://fwhyy.com/img/post/2011-01-09_225700.gif)

点击完成会弹出重启电脑的确认框

![2011-01-09_225755](http://fwhyy.com/img/post/2011-01-09_225755.gif)

重启动脑后会弹出下面对话框，提示此服务器已是域控制器

![2011-01-09_230726](http://fwhyy.com/img/post/2011-01-09_230726.gif)

点击“完成”就完成了AD和DNS的安装。

## 相关文章

[SharePoint2007安装图文详解一：安装IIS及相关组件](http://blog.fwhyy.com/2011/01/iis-install/)
SharePoint2007安装图文详解二：安装AD（活动目录）及DNS
[SharePoint2007安装图文详解三：安装SqlServer2005](http://blog.fwhyy.com/2011/01/install-sqlserver2005/)
[SharePoint2007安装图文详解四：安装.NET Framework 3.0和SharePoint 2007](http://blog.fwhyy.com/2011/01/installation-of-the-net-framework-3-0-and-sharepoint-2007/)


