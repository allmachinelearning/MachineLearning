## 机器学习的一些资料
### 1. 机器学习与概率、统计学
#### 1.1 公开课
1. [斯坦福机器学习入门课程](https://www.coursera.org/learn/machine-learning)，讲师为Andrew Ng，适合数学基础一般的人，适合入门，但是学完会发现只是懂个大概，也就相当于什么都不懂。
2. Coursera上国立台湾大学[林轩田](https://www.coursera.org/instructor/htlin)开的两门课：[机器学习基石](https://www.coursera.org/course/ntumlone)（适合入门），[机器学习技法](https://www.coursera.org/course/ntumltwo)（适合提高）。

#### 1.2 推荐书目
统计和概率是机器学习的基础，所以统计和概率一定要学好。

1. **推荐必读**   
  - 统计学和机器学习结合的入门书：[统计学习方法](http://ddl.escience.cn/f/Iwn0)，作者[李航](http://blog.sina.com.cn/u/2060750830)。这本书介绍了10个机器学习领域的代表性算法，讲的非常好，书本身也就200多页，很适合入门，强烈推荐。
  - 机器学习入门书：周志华老师的西瓜书[机器学习](https://github.com/allmachinelearning/MachineLearning/blob/master/books/Machine%20Learning/%E6%9C%BA%E5%99%A8%E5%AD%A6%E4%B9%A0(%E5%91%A8%E5%BF%97%E5%8D%8E.pdf),语言简单易懂，一度登录亚马逊，京东计算机类畅销书榜首，很适合入门阅读，相比于李航老师的书，这本书更片算法和应用 （李航老师的书更篇数学），先读李航老师的书，再读这本，效果更佳。

2. 机器学习理论方面：
	- **推荐** 著名教材《Pattern Recognition》中文版为[《模式分类》第二版](http://ddl.escience.cn/f/IwnM)，从数学的角度讲了机器学习的方方面面，非常不错。这本书好的地方是，书中所有的算法都有数学推导，讲的也很全面，作者的眼光很独到，习题和上机题也非常有挑战性；不好的地方就是，对现在流行的比如boosting和SVM等，书只是略讲了一下，可能需要额外再补充知识。不过即便如此，当我最近一个月看到这书时立刻就感叹为什么我当初上课的时候没有赶上这本书！

	- 权威学者[Kevin P. Murphy](http://www.cs.ubc.ca/~murphyk/)的著作[Machine Learning:A Probabilistic Perspective(MLAPP)](http://ddl.escience.cn/f/Iwob) ，非常厚，偏重数学理论，难度高，是学习机器学习理论的教材，我们上课用书。

3. 用python进行数据处理的书：[利用python进行数据分析](http://dlwt.csdn.net/fd.php?i=651281517754404&s=45e7feb35741a9192c2049454658704e)，适合浏览，偏重工程实践，介绍常用的python处理数据的方法和函数等，可以看看。
4. [机器学习实战](http://ddl.escience.cn/f/IwnL)，这个和第3点说的这个书配合看，效果不错，这个书很有针对性，每个算法有一个实际问题，有源程序让你去写，不错。
5. 学习统计不能不说的经典的[《统计学习基础》](http://ddl.escience.cn/f/Iwog)，我暂时还没看过。
6. 以及业界久负盛名的PRML（模式识别与机器学习），我这里[中文英文版](http://ddl.escience.cn/f/Iwoo)都有。

#### 1.3. 工具
* 第三方库
	机器学习有很多开源库可以直接拿来用，github是个不错的获取代码的网站，比较著名的有：
    * [libsvm](https://github.com/cjlin1/libsvm)，作者是林智仁，是svm的标准库。
    * [scikit-learn](http://scikit-learn.org)，scikit包是python中著名的处理数据的包，其中内置了几乎所有流行的机器学习算法，配合python简洁的语法操作，使用起来很方便。
    * [pandas](http://www.cnblogs.com/chaosimple/p/4153083.html)，python的一个包，其中对表的处理比较出色，我只是试用过。
    * [pylearn2](https://github.com/lisa-lab/pylearn2),这个我没有接触过，不过在github上排名很靠前，应该不错。
    * [smile](https://github.com/haifengl/smile)，彪悍的机器学习库，用java开发，有自然语言处理方面的库。
    * [oryx](https://github.com/cloudera/oryx)，处理大规模数据很彪悍。
    * [mlpack](https://github.com/mlpack/mlpack),老牌可靠c++编写的机器学习库。

* 工具
python、java以及matlab三种语言是目前比较流行的机器学习方面的语言。
    * python：强在各种包，几乎无所不能，其科学计算部分（scikit）和matlab不相上下。用Flask当作web框架，几乎可以直接部署成web项目，非常方便，强烈推荐。
    * java：强在其企业级应用能力和稳定性。
    * matlab：强在其科学计算部分上。matlab我用的不多，因为目前来看，它和python的科学计算差不多。

* 网上的教程
这是在一个妹子的微信朋友圈看到的[文章](http://mp.weixin.qq.com/s?__biz=MjM5MjAxMDM4MA==&mid=205009516&idx=1&sn=c5b157ad3fac5c5551a210b0d7df82e6&scene=1&key=dffc561732c22651bb1642a345869d95ab71b4da7c9d7e4cbaf2b67a7b354b4fc8d6a6105171f7a8d0afde389529bb7f&ascene=1&uin=NjMzMjQzMTYw&devicetype=Windows+10&version=61020020&pass_ticket=ygVY8iy3pSYNZ2Rwe2FnXSQ5lRAKLeMmssjmRIlD4QYgBeYoE1OPVBL%2BfpjaKY0i)，很不错。

### 2. 数据挖掘
* 快速入门：看我去年考试写的总结[数据挖掘复习整理](http://ddl.escience.cn/f/IwnW)，可快速了解数据挖掘的相关概念。这个总结去年在雁栖湖传的很火，还有妹子给我发短信感谢。。。
* 数据挖掘领域的经典著作：[数据挖掘：概念与技术](http://ddl.escience.cn/f/IwoF)，作者是[韩家炜](http://baike.baidu.com/link?url=UsI-yAamHGGNoe22xOWX7XjU-8eILnF4oQTP-2dysekLxDk6FleEefGc013or725zvos5Mach2j6cWEKcv2DF_)，是标准的上课教材，上一部分我的总结中对应的页码就是这个书里的。

### 3. 人工智能
* 教材：著名的教材[人工智能：一种现代方法](http://ddl.escience.cn/f/IwnK)，很厚，可以翻看。
