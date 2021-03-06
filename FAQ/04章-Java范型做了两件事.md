Java 的范型就做了两件事情

1）根据各种语法元素，让编译器知道一个 Object 引用允许指向什么类型的对象。什么上界下界，协变逆变，都是细节。最终的目的就是判断，一个范型的引用是不是可以指向某个具体类型的对象，或者一个范型的参数，是否可以接受某个具体的类型的引用作为实参。

2）检查完之后，就是强制类型转换。 Java 编译器会在生成的字节码里，帮我们加上强制类型转换的语句，省去我们自己写强制类型转换了。而且通过1）的检查，也“尽力”避免了出现ClassCastException的可能。

汇成一句话就是：
“编译期类型检查，运行时类型擦除”

你如果去看 Java 编译出来的带范型的类文件的字节码，会发现编译器添加的强制类型转换相关的操作

P.S. ：Java 的范型是后面加上去的，有些设可能是处于妥协。但是在我看来，也是够用了。

***

这篇文章来自极客时间推出的[《零基础学Java》](https://time.geekbang.org/course/intro/181)中的FAQ。除了在每节视频课下方回答大家的问题之外，针对大家提出的优质问题或者普遍问题，如果需要更大篇幅的文章解答，则会在FAQ中以文章的方式给出回答。带你零基础入门，夯实Java，课程地址：https://time.geekbang.org/course/intro/181


