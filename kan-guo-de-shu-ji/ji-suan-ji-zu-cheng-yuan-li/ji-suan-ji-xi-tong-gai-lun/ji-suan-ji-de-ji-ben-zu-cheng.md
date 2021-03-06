* MAR:存储器地址寄存器,反映存储单元的个数
* MDR:存储器数据寄存器,反映存储字长

### 冯诺依曼计算机的特点

* 计算机由五大部件组成
  * 运算器
  * 存储器
  * 控制器
  * 输入设备
  * 输出设备
* 指令和数据以同等地位存于存储器，可按地址寻访
* 指令和数据用二进制表示
* 指令由操作码和地址码组成
* 存储程序
* 以运算器为中心
* 基本特点:
  * 按地址访问并顺序执行指令

### 冯诺依曼计算机硬件框图

![](/assets/js-14.2.1.2-1.png)

* 输入设备:将信息转换成机器能识别的形式
* 输出设备:将结果转换成人们熟悉的形式
* 存储器:存放数据和程序
* 运算器:完成算数运算和逻辑运算
* 控制器:控制、指挥程序和数据的输入、运行以及处理运算结果

### 现代计算机硬件框图

![](/assets/js-14.2.1.2-2.png)

![](/assets/js-14.2.1.2-3.png)

### 系统复杂性管理的方法

* 层次化:将被设计的系统划分为多个模块或子模块
* 模块化:有明确定义的功能和接口
* 规则性:模块更容易被重用

### 计算机的工作步骤

* 上机前的准备
  * 建立数学模型
  * 确定计算方法
  * 编制解题程序
    * 程序
      * 运算的全部步骤
    * 指令
      * 每一个步骤

```
计算ax^2+bx+c             =          (ax+b)x+c

取x 至运算器中                        乘 x 至运算器中
乘以 x在运算器中                      乘以a在运算器中
乘以 a在运算器中                      加b在运算器中
存ax^2 在存储器中                     乘以x在运算器中
取b 至运算器中                        加c在运算器中
乘以x在运算器中
加ax^2 在运算器中
加c 在运算器中


右边的指令比左边的指令少
```

* 存放在寄存器ACC中的操作数有

  * 被加数及和
  * 被除数及余数

* 指令格式

  * 操作码和地址码

* 指令和数据都是保存在存储器中的

### 存储器的基本组成

* 存储体-存储单元-存储元件\(0/1\)
* 存储体:由多个存储单元组成
* 存储单元:存放一串二进制代码\|存放一个存储字的所有存储元集合
* 存储字:存储单元中的二进制代码组合
* 存储字长:存储单元中二进制代码的位数，每个存储单元赋予一个地址
* 存储单元按地址寻访

#### 主存储器

* MAR:存储器地址寄存器,反映存储单元的个数
  * 存放欲访问的存储单元地址
* MDR:存储器数据寄存器,反映存储字长
  * 缓存\(进去/出去的\)数据
* 存储体M

```
设MAR=4位，MDR=8位
存储单元个数为16=2^4
存储字长为8
```

```
运算器的结构是什么?
运算器的功能是什么？如何工作的？
加法
乘法
```

### 运算器

* ACC:累加器
* MQ:乘商寄存器
* ALU:算述逻辑单元
  * 不能存储运算结果
  * 不只是做加法运算
* X:数据寄存器

![](/assets/js-14.2.1.2-6.png)

```
加法操作
[M] -> X
[ACC] + [X] -> ACC

减法操作
[M] -> X
[ACC] - [X] -> ACC

乘法操作
[M] -> X
[ACC] -> X
0 -> ACC
[X]X[MQ] -> ACC//MQ ==> //: 表示两个寄存器串接


除法操作
[M] -> X
[ACC] / [X] -> MQ
余数保存在ACC中
```

### 控制器

#### 功能

* &gt;解释指令
* &gt;保证指令的按序执行

完成一条指令的步骤:

* 取指令-PC

* 分析指令

* 执行指令

#### PC程序计数器

* 存放当前欲执行指令的地址
* 具有计数功能\(PC\)+1-&gt;PC

#### IR指令寄存器

* 存放当前欲执行的指令

#### CU控制单元

---

### 主机完成一条指令的过程

#### 以取数指令为例

![](/assets/js-14.2.1.2-7.png)

#### 以存数指令为例

![](/assets/js-14.2.1.2-8.png)

### ax^2+bx+c程序的运行过程

* 将程序通过输入设备送至计算机
* 程序首地址 -&gt; PC
* 启动程序运行
* 取指令 PC -&gt; MAR -&gt; M -&gt; MDR -&gt; IR,\(PC -&gt; PC+1\)
* 分析指令 OP\(IR\)-&gt;CU
* 执行指令 Ad\(IR\) -&gt; MAR -&gt; M -&gt; MDR -&gt; ACC

* ...

* 打印结果

* 停机



