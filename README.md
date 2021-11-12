# 电源-【不死鸟】

## **写在前面：**

本怪之前参加了很多的小车比赛，是个十足的小车爱好者。🤷‍♀️

在做小车的过程中，主控制器基本上千篇一律，功能也是一样。

但是翻过最多车的就是供电。

对于竞赛小车而言，**18650是首先排除的**（它能提供的电流实在是太小了）。最好用的方案就是使用**航模电池**（2S,3S,4S）

**但是航模电池也不是完美的**，它的放电倍率太大，10A以上是常态，过放问题也很头疼。

我们的电源使用起来是需要对此进行合理管理和降压的。

你比如模块、舵机使用的5V，MCU之类使用的3.3V（LM2596已经不适用我的项目了）。

还有电源波动导致模块工作异常问题等等。

于是我把他们都集合了起来，组成了不死鸟。😬

![ad](https://images.gitee.com/uploads/images/2021/1102/133434_9a49f554_7821111.png "ad.png")



## **主要功能：**

1. 自锁电路（你可以很长时间不拔电池）
2. 电压检测/电池识别
3. 快冲输出（USB3.0）USB口可以给手机快充,也可以外挂一个需要USB 5V供电设备（树莓派）
4. 降压输出（4.8--7V可调输出）、（3.3VMCU供电电压不可输出）
5. 过放保护（例如3S电池在11.1V时，停止放电）
6. 过流保护（软件自己设置）
7. 过温保护（软件自己设置）
8. 通讯设置（软件自己设置），可以和主控通信，告诉它还剩多少电，按照现在电流还能工作多久...

## 尺寸：DC-DC Power 8~25V        64*34mm

![渲染正面](https://images.gitee.com/uploads/images/2021/1102/133500_4afa0141_7821111.jpeg "Bird.f.jpg")

![背面](https://images.gitee.com/uploads/images/2021/1102/133533_9e4ae17f_7821111.jpeg "Bird.b.jpg")


![实拍](https://images.gitee.com/uploads/images/2021/1102/133556_6fea1c5c_7821111.jpeg "e5b5243195053be5e1663db0ae2cc25.jpg")

![实拍](https://images.gitee.com/uploads/images/2021/1102/133618_e396a0ef_7821111.jpeg "398e327fef771e3dd3794119da8df5d.jpg")

## **食用方法：**

MDK按需修改（大多数人没必要改）

![MDK](https://images.gitee.com/uploads/images/2021/1102/133638_1b93aeaa_7821111.png "dd11496a19d1379e027cacc54b1cb2a.png")

下载设置

![STC-ISP](https://images.gitee.com/uploads/images/2021/1102/133657_ad311975_7821111.png "821f025d0598807623070460e4ea139.png")

## **写在最后：**

本次设计直接用STC15W408AS，10位ADC，UART，SPI都有，关键是我之前大二的项目，现在更新移植一下即可。有想法的小伙伴可以用STM8/32。

我叫卡文迪许怪，咸鱼一条，如果你有好的Idea可以告诉我哦！

预计在11月后开源（我得先测试好并且莽玩代码）10月份发是体验版。（手把手原理教程发B站）

[B站传送门](https://space.bilibili.com/102898291?spm_id_from=333.1007.0.0)

[github](https://github.com/SwiperWiity)

[下载链接](https://gitee.com/Swiper_witty/bird)
