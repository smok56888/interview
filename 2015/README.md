
# 20150717快的
> 大数据变现部门
+ 快排
+ redis怎么实现大数据量hash的速度
+ 两堆大量整数求差集



# 20150707上午 宜信
> 社会气太重，简历都没准备，没有前台。 
- 面试没问什么太有含量的东西，上来就要求加班9106，薪水给的不多。
- 放弃。

# 20150706下午  美团
- 类加载机制，双亲委托模型
- mysql里update会加几个锁，myisam的共享锁S、排它锁X
- redis支持的数据类型，深入了解过么
- hashset扩容问题-同hashMap
- concurrentHashMap求size怎么实现：尝试两次不加锁的累加segment，如果中间没变化ok，中间有变化在加锁处理
- mq如果消费者挂了，消息会怎么样
- 并发集合：http://blog.sina.com.cn/s/blog_616e189f0100rw7x.html
- 一面过，二面挂。面试官不友善。


# 20150702上下午面试微点|口袋购物
> 位于酒仙桥东做621公交过去，但是堵车晚到了20分钟。 
- 面试基础比较多。
- 消息队列怎么处理丢包的问题。
- concurrentHashMap怎么保证线程安全。get不阻塞，迭代是迭代器创建时候的快照，只能同时被一个线程使用。更新操作的并发基本可以配置。
- 算法：走台阶，一次可以走一步或者两部，问n阶有几种走法。f(n)=f(n-1)+f(n-2)；可以用递归或者循环做。分析时间和空间复杂度。

# 20150701下午面试搜狗营销事业部
> 一面 
- httpclient的超时机制
- 表的主键用数字和字符串哪个效率高，
- 存储引擎的区别，
- myisam的适用范围
- shell命令，awk命令。
- outofmemmery相关的产生原因。
- 线程的sleep和wait的区别，
- executorservice的submit和execute区别，
- mysql事务的隔离级别，

> 二面 
- 二面问的差不多，问的东西比较虚，要深度但是没有表现出来，目测要挂。

# 20150701下午阿里云3面
- 从自我介绍讲，讲项目，工作内容，然后常规的基础问题，
- 抽象类和接口的区别,是否可以实例化、可以有自己的方法
- 线程池。
- 感觉后续有戏 -- 并没有

# 20150701上午面试优酷
> 笔试题 
- 提到了重入锁，乐观锁悲观锁的概念
- 还有进程交替打印，字符串递归逆转的编程题。

> 面试官问题 
- 针对jvm调优，问题追踪，
- memcache和redis展开，只聊了皮毛，没深入，写的笔试题也没有提到。
- 岗位职责是优酷维护用户的吐槽吧产品，前期百万级用户，小组5个人左右，感觉也没什么意思。

> hr面 
- hr面热心冷不太喜欢，上来让自我介绍，介绍完了项目经历还问，感觉都没听进去。
- 最后给的offer是15base我写的期望是22-25。hr一直以16到20个月来诱惑，可惜爷是见过世面的~约定下周一给回复。

# 2015年6月14日 21:26:59 准备阿里云电话面
- nio和io
- jvm内存模型和调优
- 常用rpc框架
- 并发编程、设计模式
- 如何设计hashmap的key对象的hashcode
- 泛型通配符，什么情况下用
- 场景式的问题:秒杀,能列出常见的排队、验证码、库存扣减方式对系统高并发的影响
    http://blog.sina.com.cn/s/blog_63d8dad801019wrh.html
    http://www.zhihu.com/question/20496392
- ehcache
- tcp/ip；http
    http://kb.cnblogs.com/page/209100/
- 熟悉主流分布式文件系统FastDFS等。
- 熟悉JMS，可熟练使用ActiveMQ。
- 长连接 短连接
- Java 虚拟机有什么优化？
- 系统可靠性和可用性如何理解~
- 事务实现的底层机制


# 2015年6月12日 14:28:54  阿里云电话面
- spring aop的设计模式
> 代理模式
- mysql的存储引擎，及区别
> mysql所有b+tree http://blog.jobbole.com/24006/
- arrayList linkedList的区别
- redis删除后会从内存删掉么？什么时机删掉
-- 删除的时候不删除，再次查询到的时候才去删除
- java 泛型，和其它语言泛型的区别，Integer包装类在泛型中应用
- 5个线程，1一个一组另4个一组，实现组间串行，组内并行
-- CountDownLatch
- Memcache内部是怎么实现原子操作的
- Integer、int的区别
> Integer a\b = 100 c\d = 200判断相等关系。
- java反射机制

# 6月11日  滴滴    当代城市家园9月份去上地软件园
- mysql的引擎类型，区别
- mysql的索引类型，实现机制
- java的引用类型，方法内new个新的对象会怎样
- java方法中参数传递的都是值，不过基本类型传递的是值本身，引用类型传递的是引用对象的地址；到达方法之后会在栈中开辟一个新的地址存放传进来的值或者引用的地址。
--    针对基本类型，在方法内修改入参，改变的只是方法栈中的值，不会影响调用方法前变量的值，因为是存放在栈的不同位置。
--    针对引用类型，在方法内修改入参的属性，改变的是该引用对象在堆内地址的值，而方法内核方法外的引用指向的都是同一个地址，所以对属性的更改会表现在方法外。而如果是在方法内new一个新对象，则方法内引用的就是堆内一个新地址的对象，与方法外的引用对象不是同一个。
--    针对shtring，虽然string是一个引用类型，可是表现却和基本类型一致。
- 算法，聚合的实现
- memcache存储的结构
-- http://blog.csdn.net/wusuopuBUPT/article/details/18238003
- spring的特点，aop及其设计模式
- sql in的例子



# 2015年6月8日 19:13:39  百度商业平台研发部
先是介绍项目，接着算法题，然后开放性的问擅长java哪些工具（集合类、concurrent包之类的），然后又是算法题。
- 求n个数中最小的k个http://blog.csdn.net/fisher_jiang/article/details/2473698
(```)
    a\内存中记录k个数，O（kn）
    b\构造k节点的大顶堆，遍历n，与顶点比较并维护堆，O（klogn）
    c\败者树
(```)
- 10个运动员，裁判发令，等运动员结束或者超时后汇报结果
- 集合类型
-- http://www.cnblogs.com/xwdreamer/archive/2012/05/30/2526822.html
-- http://www.importnew.com/16138.html
- java关键字 volatile
(```)
http://blog.chinaunix.net/uid-26806098-id-3182336.html
http://www.cnblogs.com/wenjiang/p/3276433.html
http://blog.csdn.net/fanaticism1/article/details/9966163
volatile和static的区别http://blog.sina.com.cn/s/blog_4e1e357d0101i486.html
velotile和线程http://www.cnblogs.com/wenjiang/p/3276433.html
volatile告诉编译器它修饰的变量是易变的，对其的访问不做优化 -- 主寄存器和线程寄存器，线程看到的是其寄存器的副本，如果线程共享变量就看不到其他线程对变量的修改；volatile使得线程对变量的读取修改都通过主内存实时进行，这样线程间可以看到其他进程的修改。---volatile提供了对变量一致性的保证，也即可见性；volatile仅能作用在变量上，且只有自身值的修改与自身之前的值无关时才有效。
synchronized是修饰方法或者代码块，保证同时只有一个线程执行该段代码。当一个线程访问synchronized代码块时，其他线程对代码块的访问将会造成等待阻塞；synchronzied不仅保证了对变量的可见性，也保证了互斥性，比volatile同步粒度更大，但带来的消耗也更大
static声明变量的唯一性
(```)
- java内存结构
(```)
http://www.cnblogs.com/gw811/archive/2012/10/18/2730117.html
http://www.cnblogs.com/dingyingsi/p/3760447.html
(```)

# 2015年3月26日 10:11:45  网易乐得
公司印象：安静、台式机、加班给钱、打卡&弹性上下班，一周加班2-3天到9点、团队不大，处于五道口
- servlet是单例还是多例的 -- servlet详细
(```)
Servlet容器默认是采用单实例多线程的方式处理多个请求的：
1.      当web服务器启动的时候（或客户端发送请求到服务器时），Servlet就被加载并实例化（只存在一个Servlet实例）；

2.      容器初始化Servlet。主要就是读取配置文件（例如tomcat，可以通过servlet.xml的<Connector>设置线程池中线程数目，初始化线程池；通过web.xml，初始化每个参数值等等）；

3.      当请求到达时，Servlet容器通过调度线程（Dispatchaer Thread）调度它管理下的线程池中等待执行的线程（Worker Thread）给请求者；

4.      线程执行Servlet的service方法；

5.      请求结束，放回线程池，等到被调用；
(```)
- jvm调优http://unixboy.iteye.com/blog/174173
- 重写equals方法的原则
(```)
一。 在重写equals方法时，要注意满足离散数学上的特性
1   自反性：对任意引用值X，x.equals(x)的返回值一定为true.
2   对称性：对于任何引用值x,y,当且仅当y.equals(x)返回值为true时，x.equals(y)的返回值一定为true;
3   传递性：如果x.equals(y)=true, y.equals(z)=true,则x.equals(z)=true
4   一致性：如果参与比较的对象没任何改变，则对象比较的结果也不应该有任何改变
5   非空性：任何非空的引用值X，x.equals(null)的返回值一定为false 
二。 在重写equals方法时，还要顺手把 hashCode方法一起重写了。
     这一点主要是考虑和集合类协同工作的需要。一般集合为加快存取速度，通常使用类hashtable的方式存取对象， hashCode() && equals() 则是判断待查找元素与集合中某个元素相等的依据。 而java中默认的hashCode是由对象的内存地址生成的, 如果重写了equals 而 不重写 hashCode， 则会造成“A和B相等，A加入集合后，用B查询集合却查不到”的悖论。 
当然了，以上只是约束条件，关键还是要符合自己设计的初衷，把最起码的相等判别逻辑给无视了。 
三。重写equals方法的一般步骤：
1. 使用==操作符检查“实参是否为指向对象的一个引用”。 
2. 使用instanceof操作符检查“实参是否为正确的类型”。 
3. 把实参转换到正确的类型。 
4. 对于该类中每一个“关键”域，检查实参中的域与当前对象中对应的域值是否匹 配。
          a。对于既不是float也不是double类型的基本类型的域，可以使用==操作符进行比较（why？）；
          b。对于对象引用类型的域，可以递归地调用所引用的对象的equals方法； 
　　    c。对于float类型的域，先使用Float.floatToIntBits转换成int类型的值， 然后使用==操作符比较int类型的值；
          d。对于double类型的域，先使用Double.doubleToLongBits转换成long类型的值，然后使用==操作符比较long类型的值。
5. 当你编写完成了equals方法之后，应该问自己三个问题：它是否是对称的、传 
　　递的、一致的？(其他两个特性通常会自行满足)如果答案是否定的，那么请找到 
　　这些特性未能满足的原因，再修改equals方法的代码。
(```)
- java类中的设计模式http://www.uml.org.cn/j2ee/201010214.asp

    单例模式 --- java.lang.Math
    装饰模式---java中的IO流的类层次 InputStream OutputStream
    

- HashMap、HashTable、CurrentHashMap的区别

    CorrentHashMap和hashTable的区别http://blog.csdn.net/kobejayandy/article/details/16834311
    
    hashmap和hashtable的区别http://www.importnew.com/7010.html

    hashMap的工作原理http://www.importnew.com/7099.html

    ConcurrentHashMap和Hashtable的区别：Hashtable和ConcurrentHashMap有什么分别呢？它们都可以用于多线程的环境，但是当Hashtable的大小增加到一定的时候，性能会急剧下降，因为迭代时需要被锁定很长的时间。因为ConcurrentHashMap引入了分割(segmentation)，不论它变得多么大，仅仅需要锁定map的某个部分，而其它的线程不需要等到迭代完成才能访问map。简而言之，在迭代的过程中，ConcurrentHashMap仅仅锁定map的某个部分，而Hashtable则会锁定整个map。
    
    HashMap的工作原理：HashMap基于hashing原理，我们通过put()和get()方法储存和获取对象。当我们将键值对传递给put()方法时，它调用键对象的hashCode()方法来计算hashcode，让后找到bucket位置来储存值对象。当获取对象时，通过键对象的equals()方法找到正确的键值对，然后返回值对象。HashMap使用链表来解决碰撞问题，当发生碰撞了，对象将会储存在链表的下一个节点中。 HashMap在每个链表节点中储存键值对对象。当两个不同的键对象的hashcode相同时会发生什么？ 它们会储存在同一个bucket位置的链表中。键对象的equals()方法用来找到键值对。
    
    “你知道HashMap的工作原理吗？” “你知道HashMap的get()方法的工作原理吗？”：HashMap是基于hashing的原理，我们使用put(key, value)存储对象到HashMap中，使用get(key)从HashMap中获取对象。当我们给put()方法传递键和值时，我们先对键调用hashCode()方法，返回的hashCode用于找到bucket位置来储存Entry对象。
    
    “当两个对象的hashcode相同会发生什么？”：因为hashcode相同，所以它们的bucket位置相同，‘碰撞’会发生。因为HashMap使用链表存储对象，这个Entry(包含有键值对的Map.Entry对象)会存储在链表中。
“如果两个键的hashcode相同，你如何获取值对象？”：找到bucket位置之后，会调用keys.equals()方法去找到链表中正确的节点，最终找到要找的值对象

    如果HashMap的大小超过了负载因子(load factor)定义的容量，怎么办？：默认的负载因子大小为0.75，也就是说，当一个map填满了75%的bucket时候，和其它集合类(如ArrayList等)一样，将会创建原来HashMap大小的两倍的bucket数组，来重新调整map的大小，并将原来的对象放入新的bucket数组中。这个过程叫作rehashing，因为它调用hash方法找到新的bucket位置。
    
    你了解重新调整HashMap大小存在什么问题吗？：当重新调整HashMap大小的时候，确实存在条件竞争，因为如果两个线程都发现HashMap需要重新调整大小了，它们会同时试着调整大小。在调整大小的过程中，存储在链表中的元素的次序会反过来，因为移动到新的bucket位置的时候，HashMap并不会将元素放在链表的尾部，而是放在头部，这是为了避免尾部遍历(tail traversing)。如果条件竞争发生了，那么就死循环了
    
    为什么String, Interger这样的wrapper类适合作为键？ ：String, Interger这样的wrapper类作为HashMap的键是再适合不过了，而且String最为常用。因为String是不可变的，也是final的，而且已经重写了equals()和hashCode()方法了。其他的wrapper类也有这个特点。不可变性是必要的，因为为了要计算hashCode()，就要防止键值改变，如果键值在放入时和获取时返回不同的hashcode的话，那么就不能从HashMap中找到你想要的对象。不可变性还有其他的优点如线程安全。如果你可以仅仅通过将某个field声明成final就能保证hashCode是不变的，那么请这么做吧。因为获取对象的时候要用到equals()和hashCode()方法，那么键对象正确的重写这两个方法是非常重要的。如果两个不相等的对象返回不同的hashcode的话，那么碰撞的几率就会小些，这样就能提高HashMap的性能。
    
    我们可以使用自定义的对象作为键吗？：可以，只要遵守equals()和hashCode()方法的定义规则
    
    我们可以使用CocurrentHashMap来代替Hashtable吗？：。我们知道Hashtable是synchronized的，但是ConcurrentHashMap同步性能更好，因为它仅仅根据同步级别对map的一部分进行上锁。ConcurrentHashMap当然可以代替HashTable，但是HashTable提供更强的线程安全性。

- linux常用命令

1. cat
2. tac
3. head
4. tail
5. cat /proc/cpuinfo  ： 查看cpu的信息


- java中的内存泄漏  

    http://www.cnblogs.com/qq78292959/archive/2011/07/25/2116123.html
    java中的gc通过引用来判断内存是否使用，如果不再使用的对象依然有引用，就会造成内存泄漏，或者叫对象游离
    
(```)
    Vector v=new Vector(10);
    for (int i=1;i<100; i++){
    Object o=new Object();
    v.add(o);
    o=null;
    }
(```)

- 运行时异常和非运行时异常

    Java提供了两类主要的异常:runtime exception和checked exception。checked异常也就是我们经常遇到的IO异常，以及SQL异常都是这种异常。对于这种异常，JAVA编译器强制要求我们必需对出现的这些异常进行catch。所以，面对这种异常不管我们是否愿意，只能自己去写一大堆catch块去处理可能的异常。      
但是另外一种异常：runtime exception，也称运行时异常，我们可以不处理。当出现这样的异常时，总是由虚拟机接管。比如：我们从来没有人去处理过NullPointerException异常，它就是运行时异常，并且这种异常还是最常见的异常之一。      

    出现运行时异常后，系统会把异常一直往上层抛，一直遇到处理代码。如果没有处理块，到最上层，如果是多线程就由Thread.run()抛出，如果是单线程就被main()抛出。抛出之后，如果是线程，这个线程也就退出了。如果是主程序抛出的异常，那么这整个程序也就退出了。运行时异常是Exception的子类，也有一般异常的特点，是可以被Catch块处理的。只不过往往我们不对他处理罢了。也就是说，你如果不对运行时异常进行处理，那么出现运行时异常之后，要么是线程中止，要么是主程序终止。      

    如果不想终止，则必须扑捉所有的运行时异常，决不让这个处理线程退出。队列里面出现异常数据了，正常的处理应该是把异常数据舍弃，然后记录日志。不应该由于异常数据而影响下面对正常数据的处理。在这个场景这样处理可能是一个比较好的应用，但并不代表在所有的场景你都应该如此。如果在其它场景，遇到了一些错误，如果退出程序比较好，这时你就可以不太理会运行时异常，或者是通过对异常的处理显式的控制程序退出。
异常处理的目标之一就是为了把程序从异常中恢复出来。

