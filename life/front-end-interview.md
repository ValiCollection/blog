title:面试
date:2013/5/8

看到寒冬winter大大的公开面试题，觉得很有意思，又看了下面的一些回复，觉得我可以答的更好些。。

所以忍不住凑个热闹

1. 你对前端职业发展有何看法
---------
前端职业充满了未知和激情。

前端更容易写出一个完整而且有趣的作品

比起做内核的程序员，我们也许更加愉快，不必去考虑进程通信，信号，阻塞这些繁杂的问题。使用脚本又大大节约本该关注内存的时间。

但是前端也面临这风险。如果在一个不关注前端的公司（他们认为前端就是做网页，做效果），前端很难有发展，也很难得到较高的地位

2. 前端和后端程序员应该如何合作？
------------
我个人觉得前端完全包括了后端。

比如表单数据验证，同一个数据格式的验证必须前后端都做，如果两个人分别做的话就会浪费一倍的时间。

ajax接口：ajax接口一般很难一下子就做的最好，经常面临一些改动，比如数据格式之类的，这样的改动直接影响到前端的调用。因此前端的程序员应该直接参与后台数据结构的设计。

前端还必须完全熟悉http协议，什么时候重定向，哪个url会设置cookie。css，img文件的缓存控制。这些都和http息息相关。不管怎样，我认为前端必须完全有后端的能力。

讲几个你在项目中解决的让你印象最深的问题（难、匪夷所思、解决方案有趣都可以）--------
有一种这样的需求。提供一个路径字符串数组，构造成一个hash。

在JavaScript面向对象方面，你有什么体会和实践？
-------------
在这方面我深有体会。

js在处理多态，封装上都毫无压力。甚至是纯天然的。但在继承上却有些难懂

所以说js的oo，我还是说js的继承吧

我很早就知道js是原型继承，但我当初并没有专门去了解原型链

后来在做一个小小的canvas引擎的时候，竟然发现

。。。

new 并没有新建内存数据，也就是说修改子实例a上的proto上的属性，也会修改子实例b上的proto上的属性，以后再new也是这样了。

也就是说这个new完全是挂在了prototype树上。（我个人喜欢称原型为树而不是链。。）

这个绝对是一个大坑，最后的解决就是用call来复制属性，用new proto来借用函数。

对于数据对象是先JSON.stringify把引用数据转为原数据复制。

总之我认为的js的继承就是属性值复制，函数借用。

谈谈javaScript中的闭包，以及你的实践。（todo）
----------------
对于闭包我实践的很少，唯一用到的就是在编码规范上的。

在写自己的模块时完全不能使用全局变量，所有函数用匿名立即执行函数套住。

在写主要的js中，也要尽量使用闭包，把全局变量降为1个，最好也是0个。

（ajax异步调用？）

说说 http://m.taobao.com 前端做的最烂的地方，以及你的改进。
---------
我只是上过这个网站而且也没有资格说这个前端最烂的地方，但却是有几个疑惑的地方。

1. 网页宽度直接为何直接定死了？手机本来就可是空间不大（被状态栏和浏览器占了不少），而移动淘宝却连宽度都没有占满。

2. radius和shadow都是耗费渲染性能的。手机端不该用。

3. 点击搜索框的事件有点匪夷所思，给不怎么懂技术的人的感觉就是：

 >啊，怎么搜索还跳转页面啊，下面还没有刷出来。我刷新一下（后退一下）

 他的问题就在于我明明只想输入几个字，他却来个页面大变化。让人以为换了个页面，然后就会导致使用后退刷新等错误操作想回到原页面。

 谈几个有趣的html标签，以及它们的语义。
 -------------
 我一开始觉得html标签并不有趣或者特别，因为标签都一样，只不过有user agent stylesheet加了默认样式

 后来想想还是有有趣的标签的，比如pre。pre就是保持格式。一般配合code来显示源代码。同时我更多的用在调试上，比如view改变model，我就把model显示在pre中

  >JSON.stringify(model, null, '\t');

 非常方便。

 再一个有趣的标签那必须说canvas了，我特别喜欢拿canvas做一些小游戏，比如连连看，塔防，小人对打。canvas完全把人带入另一个世界。webGL的介入使得canvas不再是纯canvas演示，而且可以展示更加华丽的效果同时分担css渲染线程的压力

 讲一讲CSS的position/float/display都有哪些取值，它们相互叠加时的行为都是什么？
 -----------




