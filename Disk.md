**磁盘分区、逻辑卷、扩容、配额**

**第一章：pv vg lv 概念**

pv、vg、lv概念：https://www.cnblogs.com/lijiaman/p/12885649.html

逻辑卷是使用逻辑卷组管理(Logic Volume Manager)创建出来的设备，如果要了解逻辑卷，那么首先需要了解逻辑卷管理中的一些概念。

- 物理卷（Physical Volume,PV）：也就是物理磁盘分区，如果想要使用LVM来管理这个分区，可以使用fdisk将其ID改为LVM可以识别的值，即8e。
- 卷组（Volume Group,VG）：PV的集合
- 逻辑卷（Logic Volume,LV）：VG中画出来的一块逻辑磁盘

了解概念之后，逻辑卷是如何产生的就很清晰了：物理磁盘或者磁盘分区转换为物理卷，一个或多个物理卷聚集形成一个或多个卷组，而逻辑卷就是从某个卷组里面抽象出来的一块磁盘空间。具体架构如下：

![image-20230712111742976](C:\Users\houlj\AppData\Roaming\Typora\typora-user-images\image-20230712111742976.png)

