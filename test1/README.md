# 实验一：SQL语句的执行计划分析与优化指导



### 实验目的

分析SQL执行计划，执行SQL语句的优化指导。理解分析SQL语句的执行计划的重要作用。

### 实验内容

- 对Oracle12c中的HR人力资源管理系统中的表进行查询与分析。
- 首先运行和分析教材中的样例：本训练任务目的是查询两个部门('IT'和'Sales')的部门总人数和平均工资，以下两个查询的结果是一样的。但效率不相同。
- 设计自己的查询语句，并作相应的分析，查询语句不能太简单。

### 教材中的查询语句

#### 查询1：

执行结果：

![image-20210315214713853](C:\Users\25827\AppData\Roaming\Typora\typora-user-images\image-20210315214713853.png)



执行计划：

<img src="C:\Users\25827\AppData\Roaming\Typora\typora-user-images\image-20210315215345660.png" alt="image-20210315215345660" style="zoom: 67%;" />

语句分析：

该sql语句先查询出了name为it或者name为sales的记录，然后再判断id相同与否。



#### 查询2：

执行结果：

<img src="C:\Users\25827\AppData\Roaming\Typora\typora-user-images\image-20210315215554967.png" alt="image-20210315215554967" style="zoom:80%;" />

执行计划：

<img src="C:\Users\25827\AppData\Roaming\Typora\typora-user-images\image-20210315215735531.png" alt="image-20210315215735531" style="zoom: 50%;" />

语句分析：

该sql语句先判断id相同与否，再查询出了name为it或者name为sales的记录。

#### 自己的查询：

执行结果：

<img src="C:\Users\25827\AppData\Roaming\Typora\typora-user-images\image-20210315220704494.png" alt="image-20210315220704494" style="zoom: 80%;" />

执行计划：

<img src="C:\Users\25827\AppData\Roaming\Typora\typora-user-images\image-20210315220746297.png" alt="image-20210315220746297" style="zoom:67%;" />

优化：

因为和查询一的执行计划一样，没有什么优化思路，暂时也想不到更好的查询语句