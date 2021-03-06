### 概念

* 裸机\(纯硬件\)
* 操作系统
  * 负责管理协调硬件、软件等计算机资源的工作
  * 为上层的应用程序用、户提供简单的易用的服务
  * 操作系统是系统软件，而不是硬件
  * 定义
    * 操作系统是指控制和管理整个计算机系统的硬件和软件资源，并合理地组织调度计算机的工作和资源的分配，以提供给用户和其他软件方便的接口和环境，是计算机系统中最基本的系统软件
* 应用程序\(软件\)
* 用户

### 推动操作系统发展的主要动力

* 不断提高计算机资源利用率
* 方便用户
* 器件的不断更新换代
* 计算机体系结构的不断发展
* 不断提出新的应用需求

### 未配置操作系统的计算机系统

* 人工操作方式
  * 人工操作方式严重降低了计算机资源的利用率
  * 解决:通过技术/缓存技术/脱机输入、输出技术
* 脱机输入/输出\(Off-Line I/O\)方式

  * 在脱离主机的情况下进行的，称为脱机输入/输出方式
  * 把主机的直接控制下进行输入/输出的方式称为联机输入/输出方式
  * 优点
    * 减少CPU的空闲时间
    * 提高了I/O速度

* 单道批处理系统是在解决人机矛盾和CPU、I/O设备速度不匹配矛盾的过程中形成的

  * 旨在提高系统资源的利用率和系统吞吐量
  * 缺点
    * 系统中的资源得不到充分利用

* 多道批处理系统

  * 特征:多道性、无序性、调度性
  * 目的:为了进一步提高资源利用率和系统吞吐量
  * 优缺点
    * 资源利用率高
    * 系统吞吐量大
    * 无交互能力
    * 平均周转时间长
  * 需要解决的问题:
    * 处理机争用问题
    * 内存分配和保护问题
    * I/O设备问题
    * 文件的组织和管理问题
    * 作业管理问题
    * 用户与系统的接口问题

* 分时系统

  * 主要动力:为了满足用户对人机交互的需求
  * 实现中的关键问题:如何使用户能与自己的作业进行交互
  * 特征
    * 多路性
    * 独立性
    * 及时性
    * 交互性

* 实时系统:指系统能及时响应外部事件的请求，在规定的时间内完成对该事件的处理，并控制所有实时任务协调一致地运行

  * 实时系统类型
    * 工业\(武器\)控制系统
    * 信息查询系统
    * 多媒体系统
    * 嵌入式系统
  * 实时任务类型
    * 周期性实时任务和非周期性实时任务
    * 硬实时任务和软实时任务
      * 硬实时任务:系统必须满足任务对截止时间的要求，否则可能出现难以预测的结果
      * 软实时任务:偶尔错过了任务的截止时间，对系统产生的影响也不会太大
  * 特征
    * 多路性
    * 独立性
    * 及时性:实时系统-毫秒级，分时系统-秒级
    * 交互性
    * 可靠性:实时系统要求系统高度可靠，分时系统要求系统可靠

### 操作系统的功能和目标

* 在计算机系统上配置操作系统，其主要目标是:方便性、有效性、可扩充性和开放性\(方便性和有效性是OS的最重要的目标\)

  * 方便性:使计算机系统使用起来更方便

  * 有效性:改善资源利用率，提高系统吞吐量

  * 可扩充性:能够不断适应发展的要求

  * 开放性:使来自不同厂家的计算机和设备能够有效地协同工作，实现应用的可移植性和互操作性

* `作为系统资源的管理者`

  * 提供的功能
    * 处理机管理
    * 存储器管理
    * 文件管理
    * 设备管理
  * 目标
    * 安全、高效

* `作为用户与计算机硬件之间的接口`，要为其上层的用户、应用程序提供简单易用的服务

  * 提供的功能
    * 命令接口:运行用户直接使用
      * 联机命令接口 = 交互式命令接口
        * 用户说一句，系统做一句
      * 脱机命令接口 = 批处理命令接口
        * 用户说一堆，系统做一堆
    * 程序接口\(系统调用\):运行用户通过程序间接使用
      * 由一组系统调用组成\(程序接口 = 系统调用\)
    * GUI\(图形用户界面\):现代操作系统中最流行的图形用户接口
  * 目标
    * 方便用户使用

* `作为最接近硬件的层次(实现了对计算机资源的抽象)`

  * 实现对硬件机器的拓展
    * 没有任何软件支持的计算机成为裸机。在裸机上安装的操作系统，可以提供资源管理功能和方便用户的服务功能，将裸机改造成功能更强、使用更方便的机器

```
进程是一个程序的执行过程。执行前需要将程序放到内存中，才能被cpu处理
# 书上讲解
进程是指在系统中能独立运行并作为资源分配的基本单位，是由一组机器指令、数据和堆栈等组成的
```

### 操作系统的特征

* 并发:指两个或多个时间在同一时间间隔内发生。这些事件宏观上是同时发生的，但微观上是交替发生的
  * 并行:指两个或多个事件在同一时刻同时发生
  * 操作系统的并发性指计算机系统中同时存在着多个运行着的程序
  * 目的:提供系统中的资源利用率，增加系统的吞吐量
* 共享:资源共享，是指系统中的资源可供内存中多个并发执行的进程共同使用
  * 互斥共享方式\(如对摄像头设备的共享使用\)
    * 系统中的某些资源，虽然可以提供给多个进程使用，但`一个时间段内只允许一个进程访问该资源`
  * 同时共享方式\(如对硬盘资源的共享使用\)
    * 系统中的某些资源，运行一个时间段内由多个进程"同时"对它们进行访问
    * 宏观上是同时的，微观上是分时共享
* 虚拟:指把一个物理上的实体变为若干个逻辑上的对应物\(物理实体是实际存在的，逻辑上对应物是用户感受到的\)
  * 空分复用技术\(如虚拟存储器技术\)
    * 利用存储器的空闲空间区域存放和运行其他的程序，以此提高内存的利用率
  * 时分复用技术\(如虚拟处理器\)
    * 利用某设备为一用户服务的空闲时间，又转去为其他用户服务，使得设备得到最充分的利用
* 异步:在多道程序环境下，允许多个程序并发执行，但由于资源有限，进程的执行不是一贯到底，而不是走走停停的，以不可预知的速度向前推进，这就是进程的异步性
  * 只有系统拥有并发性，才有可能导致异步性

```
两个最基本的特征:并发和共享，二者互为存在条件
```



