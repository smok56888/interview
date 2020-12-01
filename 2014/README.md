
# 2014-10-22 21:20:59   大街网
1. 集合类型树  http://skyuck.iteye.com/blog/526358

 答案：  collections

    map  set  list
    
hashmap sortedmap treemap     ||  hashset linkedhashset  sortedset  treeset   ||　　LinkedList  ArrayList  Vector

2. 设计模式有哪些？单例模式的实现？分布式实现方式？

http://blog.csdn.net/shiyanming1223/article/details/6933420

答案：将造成同步问题的创建抽成单独的Synchronized同步方法 -->这样只会在开始后的时候执行一次或多次，不影响性能

3. IOC

http://www.cnblogs.com/qqlin/archive/2012/10/09/2707075.html

4. javabean管理方式

5. 前后端的框架

6. Spring\Structs\Hibenate


# 2014-10-21 21:35:09    美团
1. StringBuilder与StringBuffer的区别

    答案：http://www.cnblogs.com/Fskjb/archive/2010/04/19/1715176.html
    
    一个是线程安全，一个是非线程安全；StringBuffer线程安全，单线程性能低于StringBuilder；    
    
2. 将一个字符串根据规则倒转

    ‘abc te 123.edf 123.12312 aa.’ ==> '21321 aa.fde 321. cba et 321.'
    
3. LRUcache的实现数据结构 

    答案：http://gogole.iteye.com/blog/692103
    
    http://blog.csdn.net/beiyeqingteng/article/details/7010411

    用双向链表实现
        
4. mysql给url建索引？ 数据库引擎

     url会使索引变大，一个方案是增加一列（hash）做索引，需要多维护一列，mysql5.0的触发器实现
     
5. 寻找整形数组乘机最大的子串
