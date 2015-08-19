# 深入理解 Android 卷I

全书一共 10 章，其中一些重要章节中还设置了“拓展思考”部分。这十章的主要内容是：   

- 第 1 章介绍了阅读本书所需要做的一些准备工作，包括对 Android 整个系统架构的认识，以及 Android 开发环境和源码阅读环境的搭建等。   
- 第 2 章通过 Android 源码中的一处实例深入地介绍了 JNI 技术。
- 第 3 章围绕 init 进程，介绍了如何解析 init.rc 以启动 Zygote 以及属性服务（property service）工作的原理。
- 第 4 章剖析了 Zygote 以及 system_server 进程的工作原理。本章的拓展思考部分，讨论了Andorid启动速度、虚拟机 heapsize 大小调整问题以及“看门狗”的工作原理。
- 第 5 章讲解了 Android 源码中常用的类，如sp、wp、RefBase、Thread 类、同步类、Java 中的 Handler 类以及 Looper 类。这些类是 Android 中常用和基本的类，只有掌握这些类的知识，后续的代码分析才可能做到游刃有余。
- 第 6 章以 MediaServer 为切入点，对 Binder 进行了较为全面的分析。本章拓展思考部分，讨论了和 Binder 有关的三个问题，它们分别是 Binder 和线程的关系、死亡通知以及匿名 Service。笔者希望，读者通过本章学习，能更深入认识 Binder 的本质。
- 第 7 章阐述了 Audio 系统中三位重要成员AudioTrack、AudioFlinger 和 AudioPolicyService 的工作原理。本章拓展思考部分，分析了 AudioFlinger 中DuplicatingThread 的工作原理，并且和读者一道探讨了单元测试、ALSA、Desktop check 等问题。通过对本章的学习，相信读者会对 Audio 系统有更深的理解。
- 第 8 章以 Surface 系统为主，分析了 Activity 和 Surface 的关系、Surface 和SurfaceFlinger 的关系以及 SurfaceFlinger 的工作原理。本章的拓展思考部分，分析了 Surface 系统中数据传输控制对象的工作原理、有关 ViewRoot 的一些疑问，最后介绍了 LayerBuffer 的工作流程。这是全书中难度较大的一章，读者反复阅读和思考，或许能进一步深入理解 Surface 系统。
- 第 9 章分析了 Vold 和 Rild、其中 Vold 负责 Android 平台中外部存储设备的管理，而 Rild 负责与射频通信有关的工作。本章的拓展思考部分，介绍了与嵌入式系统中存储有关的知识，还探讨了 Rild 以及 Phone 设计优化方面的问题。
- 第 10 章分析了多媒体系统中 MediaScanner 的工作原理。在本章的拓展思考部分中，笔者提出了几个问题，旨在激发读者对 Android 深入思考和学习的欲望。

## 本书面向的读者   

- Android 应用开发工程师:刚接触 Android 系统的读者朋友，本书中关于 Binder，sp 和 wp、Handler 及 Looper 等常用类的分析，或许能帮助你迅速适应 Android 平台上的开发工作。
- Android 系统开发工程师:系统开发工程师常常需要深入理解系统的运转过程，而本书所涉及到的内容，可能正是他们在工作和学习中最想了解的。那些对具体模块（如 Audio 系统、Surface 系统）感兴趣的读者，也可以单刀直入，阅读相关章节的内容。
这里有必要提醒，要阅读此书，应具有与 C++ 相关的基本知识，因为本书的大部分内容都集中在了 Native层。

## 版权声明

本系列书籍或文章的作者是邓凡平。内容托管在极客学院 Wiki 平台上发布。 

本文为作者原创文章，未经作者允许不得转载。   

## 联系方法   

- 邮箱:fanping.deng@gmail.com
- CSDN 博客：[http://blog.csdn.net/innost](http://blog.csdn.net/innost)
- 新浪微博：阿拉神农
 
 

