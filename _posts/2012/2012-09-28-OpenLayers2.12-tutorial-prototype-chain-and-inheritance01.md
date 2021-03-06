---
layout: post
title: OpenLayers2.12学习教程之原型链和继承(1)
date: 2012-09-28 22:54
author: root
comments: true
categories: [HTML5]
tags: [原型链，继承]
---
前面学习了命名空间。今天将结合OpenLayers继续学习JS的相关知识：JS的原型链和继承。

面向对象的语言中（如java和c++），对象是类实例化的结果。而在javascript中没有类的概念，对象由对象实例化。打个比方说，基于类的语言中类就像一个模具，对象由这些模具浇注产生，而基于原型的语言中，原型就好像是一件艺术品的原件，我们通过一台100%精确的机器把这个原件复制复制出很多份。

<strong>一、构造方法定义属性和原型构造属性的区别</strong>

在javascript中构造类（即对象）并定义类的属性有两种方式，一种是通过构造函数内部构造，另外一种是通过原型构造。

由上面的输出结果可以看出，对于通过构造函数定义的属性和方法，不同对象复制了一份该属性和方法，即同一个构造函数产生的两个对象不共享实例，而对于通过原型构造的方法，不同对象所对应的该方法指向了同一个函数指针；

既然这两种方式都能构造类的属性和方法，那么我们该如何取舍呢？

除非必须用构造函数闭包，否则尽量用原型定义成员函数，因为这样可以减小闭包的开销；

尽量在构造函数内定义一般成员，尤其是对象或数组，因为用原型定义的成员是多个实例共享的。

二、原型链

Javasript中有两个特殊的对象：Object和Function，他们都是构造函数，用于生成对象。Object.prototype是所有对象的祖先，Function.protorype是所有函数的原型，包括构造函数。

我们把JavaScript中的对象分为三类：

一类是用户创建的对象，用户创建的对象即用户使用new语句创建的对象。

一类是构造函数对象，指普通的构造函数，即通过new调用生成该函数可以生成用户自定义的对象的对象，就是前面所说的模具对象；

一类是原型对象，指构造函数prototype属性指向的对象。

这三类对象中每一类都有一个_proto_属性，它指向该对象的原型，从任何对象沿着它开始遍历都可以追溯到Object.prototype。构造函数对象有prototype属性，只想一个原型对象，通过该构造函数创建对象时，被创建的对象的_proto_属性只想构造函数的prototype属性。

![png01](http://www.gisthink.com/blog/guoguogis/wp-content/uploads/2012/09/11-300x119.png)


如上图所示，person2对象是Person对象通过new构造的用户自定义对象，所以person2中的_proto_指向了Person对象的prototype属性，并且constuctor指向了该构造对象的构造函数，如这里的Person()。

原型链的实例代码为：
