---
layout: post
title: Obj-C 桥接 Swift
date: 2018-01-09 11:00:00
tags: iOS 开发
---
### 测试环境

```
Xcode版本：Version 9.2 (9C40b)

不管是新建Swift文件还是导入其他Swift文件，都要走一遍
```
**直接进入干货教程**
#### 打开准备混编的项目，然后创建Swift文件:

![1](/assets/2018-01-10/1.jpg)

**然后就会看到两个文件（代码是我添加的）：**
![2](/assets/2018-01-10/2.jpg)


```
如果Swift类想要被OC发现，必须继承自NSObject，具体信息可以去看Swift的访问控制
```

**在需要使用Swift文件的地方导入:**

`#import "Build-Swift.h"` 

一般来说是不会提示的，我这里就没有任何提示，你可以这样：

```
//  先import:
#import "Build-Bridging-Header.h"   //桥接头文件
//  然后改成:
#import "Build-Swift.h"
```
![3](/assets/2018-01-10/3.jpg)
### 混编成功！



