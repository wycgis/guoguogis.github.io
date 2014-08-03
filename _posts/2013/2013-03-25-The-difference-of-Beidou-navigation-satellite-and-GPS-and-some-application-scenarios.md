---
layout: post
title: 北斗导航卫星与GPS的区别及一些适用场景
date: 2013-03-25 11:42
author: guoguogis
comments: true
categories: [thinking]
tags: [GPS]
---
这一两年，北斗导航卫星的建立算是国家安全战略中发展最快的一个领域了。除了军事用途之外，北斗导航也在逐步尝试民用和商业化。

前段时间在网上挂了简历找工作，有幸得到好几个做北斗导航的GIS公司约我去面试。我对北斗导航系统的认识还停留在2009-2010年前后的水平，当时在学习《GPS原理》时学习到了这一块，由于各种原因对这块的知识一直没来得及更新。今天抽空在网上找了一些资料，并和同学们（大学GIS专业）在QQ群里讨论了一下北斗导航卫星的一些适用场景。总结如下，由于本人水平有限，本文所述内容如有不正确或者误导大家之处，欢迎指正！若能为那些对该领域感兴趣并需要入门的童鞋提供一些帮助，本人将倍感荣幸。

闲话少叙，先上网上的一些资料：

1、覆盖范围：北斗导航系统是覆盖中国本土的区域导航系统。覆盖范围东经约70°一140°，北纬5°一55°。GPS是覆盖全球的全天候导航系统。能够确保地球上任何地点、任何时间能同时观测到6-9颗卫星(实际上最多能观测到11颗)。

2、卫星数量和轨道特性：北斗导航系统是在地球赤道平面上设置2颗地球同步卫星颗卫星的赤道角距约60°。GPS是在6个轨道平面上设置24颗卫星，轨道赤道倾角55°，轨道面赤道角距60°。航卫星为准同步轨道，绕地球一周11小时58分。

3、定位原理：北斗导航系统是主动式双向测距二维导航。地面中心控制系统解算，供用户三维定位数据。GPS是被动式伪码单向测距三维导航。由用户设备独立解算自己三维定位数据。“北斗一号”的这种工作原理带来两个方面的问题，一是用户定位的同时失去了无线电隐蔽性，这在军事上相当不利，另一方面由于设备必须包含发射机，因此在体积、重量上、价格和功耗方面处于不利的地位。

4、定位精度：北斗导航系统三维定位精度约几十米，授时精度约100ns。GPS三维定位精度P码目前己由16m提高到6m，C/A码目前己由25-100m提高到12m，授时精度日前约20ns。

5、用户容量：北斗导航系统由于是主动双向测距的询问--应答系统，用户设备与地球同步卫星之间不仅要接收地面中心控制系统的询问信号，还要求用户设备向同步卫星发射应答信号，这样，系统的用户容量取决于用户允许的信道阻塞率、询问信号速率和用户的响应频率。因此，北斗导航系统的用户设备容量是有限的。GPS 是单向测距系统，用户设备只要接收导航卫星发出的导航电文即可进行测距定位，因此GPS的用户设备容量是无限的。

6、生存能力：和所有导航定位卫星系统一样，“北斗一号”基于中心控制系统和卫星的工作，但是“北斗一号”对中心控制系统的依赖性明显要大很多，因为定位解算在那里而不是由用户设备完成的。为了弥补这种系统易损性，GPS正在发展星际横向数据链技术，使万一主控站被毁后GPS卫星可以独立运行。而“北斗一号” 系统从原理上排除了这种可能性，一旦中心控制系统受损，系统就不能继续工作了。

7、实时性：“北斗一号”用户的定位申请要送回中心控制系统，中心控制系统解算出用户的三维位置数据之后再发回用户，其间要经过地球静止卫星走一个来回，再加上卫星转发，中心控制系统的处理，时间延迟就更长了，因此对于高速运动体，就加大了定位的误差。此外，“北斗一号”卫星导航系统也有一些自身的特点：

“北斗”具有定位和通信双重作用,具备的短信通讯功能就是GPS所不具备的。
“北斗”定位精度一点二米。
“北斗”终端价格两万元左右。
采用接收终端不需铺设地面基站。
灾难中心的船只一秒钟就可以发出信息。

虽然GPS已广泛应用，但也绝非完美无缺。

其规模太大、造价太高，其他国家很难效仿，俄罗斯和欧洲的空间局就是典型的例子。
GPS只能用作导航却无法实现通信功能，因而不能满足日益增长的用户需求。如果仅依赖GPS，则容易受别人的控制。

“北斗一号”和GPS的区别主要在于两个方面：

一方面是技术体制的区别，GPS是一个接收型的定位系统，只转播信号，用户接收就可以做定位了，不受容量的限制。“北斗一号”是双向的，既有定位又有通信的系统，但是有容量的限制，GPS是美国军方控制的军民共用的系统，对世界开放。我们中国人所说的使用的GPS是可以免费接收它的信号，但美国人并不承诺保证你的使用，他目前不收费，但没有承诺永远不收费。美国的GPS在当年刚刚被使用时要比“北斗一号”贵得多，早期在上世纪80年代末90年代初人们在用GPS系统时最便宜的GPS接收机就要几万美元，贵的要几十万美元，一套两个。北斗现在的用户终端的价格是比GPS低端的价格要贵，现在GPS价格一般导航系统在几千元人民币，高精度GPS几万到十几万元人民币不等。北斗的用户终端目前在两万元左右。

另一个问题就是它的用途和特点是不一样的，GPS解决了一个我在哪里的定位问题，比如在沙漠里，在海洋上。而北斗不仅仅解决了我在哪里，它还解决你在这里他在哪里的问题，北斗的用户终端实际是具有收发功能，而GPS只具有接收功能，它通过接收才知道位置，而北斗是具有收发功能，它的定位需要发射然后再得到位置，同时它的位置可能传给你也可以传给关心你的人，实际上北斗是具有一个定位和通信双重功能的设备，在用户群上是不一样的，接收的场合是不一样的。


北斗卫星的一些适用场景：

(1)若是军用的话，作战小组成员间可以共享位置信息，当收到攻击时其他成员能够迅速赶到现场进行救援。

(2)当在野外时，可以通过共享位置信息得到营救人员的帮助。

(3)进行测绘时，可以边测绘边上传数据。

虽然如此，但是由于需要终端主动发射信号，这就造成了信号容易被捕获，暴露目标等现象。上面这句纯属蝈蝈YY，具体细节尚不清楚。作为混迹GIS，地图，导航界的我来说，对GPS导航有一点认识，加之北斗的容量有限而我国却拥有14亿人口，所以本人觉得北斗导航卫星实现民用，商业化还需要至少5年时间。北斗卫星的军事意义才是最主要的。