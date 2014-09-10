Document
========
欢迎参加比赛。附件有培训资料(我们会8月中旬组织一次在线培训)。题目任选如下其
一。根据自己时间与精力，选择移植题目1或2程序中的一个模块或整个程序，当然移植
模块越多越好。


RDMA大学生编程挑战赛题目公布：

同学们可以在如下两个题目中任选一个，最终只需提交你选定的一个。比赛中间可以自
己决定是否更换题目。评委只按最终程序更改情况/性能提高报告来评测（英文）
两个比赛程序均是开源代码程序。

题目1：http://tachyon-project.org/

Tachyon is a memory-centric distributed file system enabling reliable file
sharing at memory-speed across cluster frameworks, such as Spark and
MapReduce. It achieves high performance by leveraging lineage information
and using memory aggressively. Tachyon caches working set files in memory,
thereby avoiding going to disk to load datasets that are frequently read.
This enables different jobs/queries and frameworks to access cached files at
memory speed.
Tachyon is Hadoop compatible. Existing Spark and MapReduce programs can run
on top of it without any code change. The project is open source (Apache
License 2.0 <https://github.com/amplab/tachyon/blob/master/LICENSE> ) and is
deployed at multiple companies.

请下载最新版本Tachyon 0.5.0 RC，
https://github.com/amplab/tachyon/releases/download/v0.5.0/tachyon-0.5.0-bin
.tar.gz


题目2：https://spark.apache.org/

Apache Spark(tm) is a fast and general engine for large-scale data
processing.
下载最新版本：
http://d3kbcqa49mib13.cloudfront.net/spark-1.0.1.tgz


两个应用程序是基于Java编写。在向RDMA迁移时，可使用RDMA编程中间件：
http://www.accelio.org/
Accelio is a high-performance asynchronous reliable messaging and RPC
library optimized for hardware acceleration. RDMA as well as other transport
implementations, such as TCP/IP, shared-memory, and others can take
advantage of efficient and convenient API.
Accelio is designed to maximize message and CPU parallelism, while
minimizing CPU contention and locking and enabling zero data copy
communication procedures. The result is an unparalleled performance gains as
measured by transactions per second, latency (Ping-Pong and under load),
bandwidth, and CPU overhead.

RDMA 基础培训资料看附件。


由于两个应用程序均具有相当难度，在团队选择题目时请酌情考虑。同时如果团队任务
整个应用的通信环节向RDMA迁移难度太大，可选择你选中的程序中某些对通信要求高的
模块进行移植（开发插件），或对比较简单模块移植，而不是整个程序的移植。总之选
择自己能够完成的进行。不过一定要做出清楚说明为什么移植该功能模块。最终成功运
行程序，评委需要看到程序在RDMA环境下 与 TCP/IP的性能对比结果。

相信比赛会给团队带来意巨大的收获。祝比赛顺利。

各参赛队，大家好：

 

为了让参赛队伍能够顺利完成比赛，特此就比赛细则做进一步说明, 由于竞赛时间紧难度大，并非一定要完成移植与编译才能得分：

 

1.       竞赛评分将分为以下几部分

Ø  选定模块

在参赛题目中选定要做RDMA移植的通信功能模块 （可以一个或多个），在提交的最终报告中做出分析说明问什么移植该模块。原则上在整个应用运行时间中占比最高的通信模块移植意义更大。

Ø  模块移植

因题目是Java程序，而RDMA编程接口verbs底层是C程序，所以移植RDMA需要编写符合JNI接口标准的类库（C 与 JAVA之间转换）。大家可以采用Accelio http://www.accelio.org/。然而如果觉得Accelio中的JXIO使用困难，可自行编写简单的类似于JXIO的类库（只用编写必须的函数，JXIO中可能有很多函数是你用不到的）。其中verbs程序部分可参考很多程序实例：

www.rdmamojo.com；网盘地址：www.115.com 用户名/密码：lichq3553@gmail.com/000000

 

 

Ø  程序性能提升

提交报告时请注明移植具体通信函数，同时运行程序得出最终结果对比（TCP 对比 RDMA）。请不要更改源程序中与通信无关的算法来提高程序速度。

 

程序移植最佳者除获得本次比赛奖励外将自动参与HPC Advisory Council在全球范围内的年度大学奖评选。

 

注：报告请用英文书写

 

组委将于9月23日上午10:00-12:00进行在线培训并回答大家的问题。培训PPT看附件，大家可提前学习。

培训在线会议Webex地址：


-------------------------------------------------------
To join the online meeting (Now from mobile devices!)
-------------------------------------------------------
1. Go to https://mellanox.webex.com/mellanox/j.php?MTID=m7db4447dc3a13d79167ba0c3df6fe270
2. If requested, enter your name and email address.
3. If a password is required, enter the meeting password: 123456
4. Click "Join".
5. Follow the instructions that appear on your screen.

To view in other time zones or languages, please click the link:
https://mellanox.webex.com/mellanox/j.php?MTID=m75ea2e62ff43f06ac1c7d4389c96d63a

-------------------------------------------------------
To join the audio conference only
-------------------------------------------------------
Call-in toll number (US/Canada): 1-408-792-6300

Access code:571 070 940

同时请大家提供所有参赛队员的个人高清图片。我们会制定竞赛短片以及所有队员的参赛纪念品。希望大家尽量派代表参加11月5日在HPC Advisory Council China Workshop 2014的颁奖典礼。

预祝程序移植顺利。


Best Regards

RDMA Competition Committee

