title:fiblog前言-玩博客的历程
date:21:57 2013/2/26
tag:web

####玩博客的历程

我看到舍友居然有一个非常美得博客，非常羡慕，了解了一下是wordpress，

上网一搜，新浪sae中就有wordpress，一键安装，非常方便。而且我还买了非常美得主题。写篇博客都开心的要命，但是后来云豆快不足了。

于是妄想自己搭建服务器，当时很傻的用nginx+php，安装了wordpress，并且用花生壳解析一个域名到网上，很显然，这是不行的，第二天网监管就打来电话。

后来我渐渐懂了些编程。并且得知nodejs这个东西，只要学了javascript，就可以通吃前后端。

我开始写自己的博客程序。其实我开始用php写着玩过，不过写到登陆和发博客就结束了。简直就像玩具。

用nodejs写的第一个博客当然也是玩具。当时依然被wordpress的思想禁锢着，感觉非得要有个数据库，以前我非常喜欢sqlite这个数据库，小巧好用。

于是选sqlite做了数据库，nodejs连着sqlite，把博客一条一条存进去，至今依然觉得很有趣。

可惜刚做完雏形，发现写博客非常麻烦，在网页上写博客简直就是愚蠢。但是直接用html写。又显得本末倒置。

直到有一天群里有人问，哪里写博客好？没人回应，只有一个说，farbox不错。无聊的我就上网搜了下。

我发现这简直太神奇了，在本地写markdown文法，同步到网盘（farbox默认金山快盘和dropbox），然后自己生成了博客网页。

幸好我当时了解了markdown，不然一定会错过这种博客思想。

github的readme.md就是markdown的意思。（有些童鞋貌似不知道.md的意思。）

markdown绝对是优秀的创新。他使人专注写作。

我现在就开着记事本在写博客。从不考虑排版。相比较word，有些人用word写作。要么把word当记事本用，写成一坨；要么就是一直在排版，居中，加粗，段落，玩的不亦乐乎。

用wordpress那里面那种编辑器也是不行的，首先你得开着网，这样才能保存草稿。但是开着网还能专心写作么？

而且在wordpress中加图片简直是痛苦，（反正在我放弃用wordpress的时候还没有拖拽的功能，我自己做了拖拽上传的功能。）

总而言之在网页上写博客也很愚蠢。markdown是专心写作的完美选择。

但这并不是说farbox就是完美的了，它有些缺点：

1. 它的模板引擎我看不懂。貌似是python的，我没环境。就算写模板也难以测试。
2. 更换模板体验很差。farbox自以为做了个很不错的模板克隆功能，谁知大家的模板都是自己的，克隆过来一下子变的乱七八糟。
3. 同步速度极慢。有一天需要给师兄看片技术文章，不得不把自己博客地址暴露，但是我曾经写过一篇屌丝文章，于是我慌忙删除了那篇博客，结果farbox一小时后才同步删除了这文章。

其中同步速度慢是最大的硬伤。farbox给出一个链接，可以激活同步，不过我感觉是不可用的。按个几分钟都没啥用。

后来看到在farbox和github page的介绍中提到jekyll，得知了这些生成博客的程序。

还有[octopress](http://octopress.org/) 自称`A blogging framework for hackers.`

已经略懂编程和网页的我觉得这实在没什么难（初生牛犊不怕虎。。）

于是我就决定自己做博客了。

