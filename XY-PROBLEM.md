---
title: The X-Y PROBLEM (XY-问题)
---
### The universal problem during life 这是我们生活中常遇到的问题


> You want to do X, and you think Y is the best way of doing so. Instead of asking about X, you ask about Y.

> — *from [Re: sequencial file naming](https://www.perlmonks.org/index.pl?node_id=87035) by [Abigail](https://www.perlmonks.org/index.pl?node_id=19977)*

* 你想去解决问题X, 但你觉得Y是最好的方式.没有去问别人X应该怎么做, 而是问了Y应该怎么做.
* 

> You're trying to do X, and you thought of solution Y. So you're asking about solution Y, without even mentioning X. The problem is, there might be a better solution, but we can't know that unless you describe what X is.

> — *from [Re: How do I keep the command line from eating the backslashes?](https://www.perlmonks.org/index.pl?node_id=430320) by [revdiablo](https://www.perlmonks.org/index.pl?node_id=163683)*

* 你想要去解决X, 但是你认为Y是最好的解决方案. 于是你提了很多解决Y的问题, 却丝毫没有提到X.于是问题就来了: ==除非你对X做了问题描述, 即使找到了在Y上更好的解决方案, 也可能对X丝毫没有帮助.(理解出现分歧)==
* 你试图做X，并想到了用Y方案。所以你去问别人Y，但根本不提X。于是，你可以会错过本来可能有更好更适合的方案，除非你告诉大家X是什么。




> To answer question Y, without understanding larger problem (the context) X, will most likely *not* help them entirely with X.

> — *from [](http://groups.google.com/groups?hl=en&selm=m18zt5muq9.fsf_-_@halfdome.holdit.com) by [merlyn](https://www.perlmonks.org/index.pl?node=merlyn) **Update:** Link seems to be dead. message can be found [here](http://diswww.mit.edu/bloom-picayune.mit.edu/perl/16823).*

* 有人在还没有真正理解更严重更重要的问题X时, 去问了问题Y, 这很大可能上对Ta在问题X上完全没有帮助.
* 

> A.k.a. "premature closure": the questioner wanted to solve some not very clearly stated X, they concluded that Y was a component of a solution, and now they're asking how to implement Y.

> — *from [](http://groups.google.com/groups?hl=en&selm=Pine.GHP.4.21.0009061210570.8800-100000@hpplus03.cern.ch) by Alan J. Flavell*

* “过早的关闭/(premature conclusion 国语里过早地下结论比较贴合)”: 提问的人希望解决一些没有十分明确程序目的的X, 他们得出结论:Y是解决问题的一部分, 紧接着他们现在开始提问如何去实现Y.
* X-Y Problem又叫“过早下结论”：提问者其实==并不非常清楚想要解决(更好)==的X问题，他猜测用Y可以搞定，于是他问大家如何实现Y。

> The XY problem is when you need to do X, and you think you can use Y to do X, so you ask about how to do Y, when what you really should do is state what your X problem is. There may be a Z solution that is even better than Y, but nobody can suggest it if X is never mentioned.

> — *from [](http://groups.google.com/groups?hl=en&selm=slrn89um8j.5g9.tadmc@magna.metronet.com) by Tad McClellan*

* XY问题是当你需要去完成X时, 你认为你可以用完成Y去实现完成X.所以当你应该去做属于问题X的部分的时候,你反而开始去提问如何去实现Y. 即使能找到更好的Z方法去解决Y的问题, 在不触及X问题的情况下 也没有人能去肯定Z可行.

### Example:
A. 
> Q) 我怎么用Shell取得一个字符串的后3位字符？
> A1) 如果这个字符的变量是$foo，你可以这样来 echo ${foo:-3}
> A2) 为什么你要取后3位？你想干什么？
> Q) 其实我就想取文件的扩展名
> A1) 我靠，原来你要干这事，那我的方法不对，文件的扩展名并不保证一定有3位啊。
> A1) 如果你的文件必然有扩展名的话，你可以这来样来：echo ${foo##*.}

B.
> Q）问一下大家，我如何得到一个文件的大小
> A1)  size = `ls -l $file  | awk ‘{print $5}’`
> Q) 哦，要是这个文件名是个目录呢？
> A2) 用du吧
> A3) 不好意思，你到底是要文件的大小还是目录的大小？你到底要干什么？
> Q)  我想把一个目录下的每个文件的每个块（第一个块有512个字节）拿出来做md5，并且计算他们的大小 ……
>A1) 哦，你可以使用dd吧。
>A2) dd不行吧。
>A3) 你用md5来计算这些块的目的是什么？你究竟想干什么啊？
>Q) 其实，我想写一个网盘，对于小文件就直接传输了，对于大文件我想分块做增量同步。
>A2) 用rsync啊，你妹！

### Conclusion:
> 我们不要以为X-Y Problem就像上面那样的简单，我们不会出现，其实我们生活的这个世界有有各种X-Y Problem的变种。下面我个人觉得非常像XY Problem的总是：
> 其一、大多数人有时候，非常容易把手段当目的，他们会用自己所喜欢的技术和方法来反推用户的需求，于是很有可能就会出现X-Y Problem – 也许解决用户需求最适合的技术方案是PC，但是我们要让他们用手机。
> 
> 其二、产品经理有时候并不清楚他想解决的用户需求是什么，于是他觉得可能开发Y的功能能够满足用户，于是他提出了Y的需求让技术人员去做，但那根本不是解决X问题的最佳方案。
> 
> 其三、因为公司或部门的一些战略安排，业务部门设计了相关的业务规划，然后这些业务规划更多的是公司想要的Y，而不是解决用户的X问题。
>
> 其四、对于个人的职业发展，X是成长为有更强的技能和能力，这个可以拥有比别人更强的竞争力，从而可以有更好的报酬，但确走向了Y：全身心地追逐KPI。
>
> 其五、本来我们想达成的X是做出更好和更有价值的产品，但最终走到了Y：通过各种手段提升安装量，点击量，在线量，用户量来衡量。
>
> 其六、很多团队Leader都喜欢制造信息不平等，并不告诉团队某个事情的来由，掩盖X，而直接把要做的Y告诉团队，导致团队并不真正地理解，而产生了很多时间和经历的浪费。


### Reference:
[1. Author-perlmonks‘blog](https://www.perlmonks.org/index.pl?node_id=542341)
[2. CoolShell 酷壳 X-Y PROBLEM](https://coolshell.cn/articles/10804.html)


