# 2nd java集合框架
2.1引言
===
数据结构是以某种形式将数据组织在一起的集合。数据结构不仅存储数据，还支持
那些访问和处理数据的操作。

java集合框架支持两种类型的容器
- 一种是为了存储一个元素集合，简称为集合(collection)
- 存储键值对，称为图(map)

2.2集合
===
- 规则集(Set)
- 线性表(List)
- 队列(Queue)

这些集合的通用特性被定义在接口中，而它的实现在具体类中提供

java集合框架中的所有具体类都实现了java.lang.Cloneable和java.io.Serializable接口，
它们的实例都是可复制且可序列化的。

2.3 Collection接口和AbstractCollection类
===
Collection接口中的有些方法是不能在具体的子类中实现的，这是可以让这些方法抛出异常
java.lang.UnsuportedOperationException.它是RuntimeException异常类的一个子类


2.4规则集
===
Set接口扩展了Collection接口。他没有引入新的方法或常量，只是规定了Set实例不包含
重复的元素。

Set接口的三个具体实现类是：散列类HashSet、链式散列集LinkedHashSet、树形集TreeSet。

###2.4.1 散列集HashSet
散列集中的元素没有特定的顺序，如果强加顺序，要使用LinkedHashSet。

for-each循环可用在数组上，也可以用在任何Collection的实例上

###2.4.2链式散列集LinkedHashSet
用链表来扩展HashSet类

###2.4.3树形集TreeSet
比较TreeSet中的对象可以使用Comparable接口，或者指定一个比较器

2.5比较器接口Comparator
===
一个实现了java.util.Comparator接口的类。Comparator有两个方法compare和equals。

2.6线性表
===
为了在集合中存储重复的元素，需要用到线性表，同时线性表允许用户指定存储的位置，用户可以
通过下标来访访问元素。List扩展了Collection接口，定义了允许重复元素的有序集合，List接口
增加了面向位置的操作，并且增加了能够双向遍历线性表的迭代器。

**数组线性表ArrayList和链表类LinkedList**

线性表的大小时可以动态改变，但是数组的大小是固定的。如果应用程序不需要在线性表中插入和删除
元素，那么数组是效率最高的数据结构。

ArrayList不能自动减小

LinkedList有两个构造方法。

2.7线性表和集合的静态方法
===

2.8规则集和线性表的性能
===
规则集比线性表更加高效

2.9向量类Vector和栈类Stack
===
除了包含用于访问和修改向量的同步方法外，Vector类和ArrayList是一样的。同步方法用于
防止两个或多个线程同时访问某个向量时引起数据损坏。

在Java集合框架中，栈类Stack是作为Vector类的扩展来实现的

2.10队列和优先队列
===
队列是一种先进先出的数据结构，元素被追加到队列的末尾，然后从队列头删除。在优先队列中，
元素被赋予优先级，删除元素时，拥有最高优先级的元素最先被删除。

2.11图
===
假设程序存储了一百万个学生，而且经常用使用社保号来搜索某个学生。针对这个任务的有效的
数据结构就是图(map).图是一种按照键值存储元素的容器。

图有三种类型：
1. 散列图
2. 链式散列图LinkedHashSet
3. 树形图TreeSet
