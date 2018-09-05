设计模式之代理模式

设计模式 代理模式

---

## 结构型模式
类的适配器模式-**对象的适配器模式**-接口的适配器模式

## 几种代理模式
· 远程代理：JAVA的RMI（Remote Method Invocation）技术。
https://blog.csdn.net/DreamLi1314/article/details/79123024
https://blog.csdn.net/mingtianhaiyouwo/article/details/50513577

· 虚拟代理：每个代理对象只有id和名字用来显示，需要显示具体信息的时候再取详细信息

· 安全代理：保护代理，控制权限

· 智能指引： 执行一些附加操作，例如计数

· cooy-on-write: 算是虚拟代理的一个分支

## 代理模式的应用场景：
如果已有的方法在使用的时候需要对原有的方法进行改进，此时有两种办法：
1、修改原有的方法来适应。这样违反了“对扩展开放，对修改关闭”的原则。
2、就是采用一个代理类调用原有的方法，且对产生的结果进行控制。这种方法就是代理模式。???修改之后，调用方使用代理类来调用方法？

## 相关模式
· 代理模式和适配器模式
都为另一个对象提供间接性的访问，而且都是从自身以外的一个接口向这个对象转发请求
从功能上来讲是不一样的，适配器主要用来解决接口之间不匹配的问题，通常是为所适配的对象提供一个不同的接口；而代理模式会实现和目标对象相同的接口

· 代理模式和装饰模式：
装饰模式的实现和保护代理的实现上类似，都是在转调其他对象的前后执行一定的功能；
但是他们的目的和功能是不同的。
装饰模式的目的是为了让你不生成子类就可以给对象添加职责，也就是为了动态增加功能；而代理模式的主要目的是控制对对象的访问。
装饰器模式主要用来替代继承，为的是给一个现有的类增加新的功能，客户端关心的是装饰后的类所具有的功能；而代理模式为的是对被代理对象提供访问控制，客户端关心的实际上还是被代理对象所具有的功能。

## 优点
协调调用者和被调用者，降低了系统的耦合度
代理对象作为客户端和目标对象之间的中介，起到了保护目标对象的作用

## 缺点
由于在客户端和真实主题之间增加了代理对象，因此会造成请求的处理速度变慢；
实现代理模式需要额外的工作（有些代理模式的实现非常复杂），从而增加了系统实现的复杂度。


