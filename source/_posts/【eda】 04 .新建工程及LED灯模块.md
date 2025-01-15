---
title: 立创eda-04 原理图的绘制
date: 2025-01-09
tags: 
    - eda
categories:
    - 软件
mathjax: false
---

## 立创eda-04 原理图的绘制

#### 0 新建工程

文件--新建---工程

**图纸基本信息更改**

![更改图纸默认信息](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109102631514.png)

**更改图纸大小**

![改图纸大小](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109102744499.png)

#### 1. 绘制LED部分

**原理图**

![LED灯原理图](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109102928198.png)

**新建元件**

​	在新建元件之前要先新建元件库

**可以把网格单位调至最小*-**

![网格单位](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109104031718.png)

![新建电阻器件](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109105114685.png)

- 一个矩形，两个引脚
- 引脚那个圆圈是电气连接部分，与外部相连

![可以用名称表示值](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109111131639.png)

**网络端口**

![网络端口放置](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109111419545.png)

#### 2. 3.3V稳压输出

**原理图**

![3.3V稳压输出](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109132051635.png)

**圆圈**

这里的圆圈代表是方向，大小可以从属性里面修改更为方便

![圆圈](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109135154698.png)

#### 3. micro输入口

**原理图**

![原理图](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109140059230.png)

**用了个差分信号**

![差分信号](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109140402510.png)

- 目的
  - 抗干扰，如果有2,3，两条线的话，在某一时刻产生了脉冲，本来应该3.3V的，变了，但是两条线差分，在这一时刻都变，差值不变
- ![](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109140602020.png)
  - 压差大的时候视为1；压差小的时候视为0

#### 4. MCU最小系统

**原理图**

![原理图](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109144752246.png)

#### 5.晶振电路

**原理图**

![外部晶振](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109162715347.png)

- R3主要是用来消除谐波和干扰的
- 一般晶振这里的电容都是20pF

#### 6. 按键部分

##### 复位按键

**原理图**

![复位按键原理图](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109164228324.png)

- 刚上电的时候，电容充电，nrst电位上升，电容起到缓冲作用
- 开关闭合，nrst为0.复位

##### 唤醒按键

![唤醒按键原理图](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250109164548756.png)

#### 7. 两个排针

![原理图1](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250114140557881.png)

![J3原理图](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250114142425018.png)

**选择参考点**

 设置---通用

![](D:\My blog\source\_posts\【eda】 04 .新建工程及LED灯模块\image-20250114145020863.png)

这样就能一路复制下来了

-----

#### 8. 原理图整理

- 横着先划线，分大区域，再竖着分
- 注意是折线而不是导线
- 点线的属性，改成虚线
- 添加文字介绍

#### 9. DRC检测

**DRC检测即规则检查**

设计---检查DRC