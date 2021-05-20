---
title: java多态polymorphic多态的理解一
categories: [development]
comments: true
---


polymorphic 多种形态的意思

A :多态概述
	事物存在多种形态（比如有一只狗在吃馒头，你可以说狗在吃馒头也可以说动物在吃饭）

B：多态前提
	a要有继承关系
	b要有方法重写
	c要有父类引用指向子类对象
    
C：案例演示

demo

```java
class Demo_polymorphic{
	public static void main(String args[]){
		Dog a = new Dog();
		a.eat();
		
		Animal b = new Dog();//父类引用指向子类对象
 
		b.eat();//想想这两个会打印出什么
}
```


Animal  and  Dog

```java
//声明动物类，并且动物都有一个吃饭的方法行为
class Animal{
	pubilc void eat(){
		System.out.println("动物吃饭")
	}
}

//狗属于动物为继承关系，它重写了吃饭行为改为吃馒头
class Dog extends Animal{//继承关系
	public void eat(){//方法重写
		System.out.println("狗吃馍")
	}
}
```