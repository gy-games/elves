# ELVES
*IT Automatic Develop Platform*

**注意**:  `master` 分支为团队开发分支，可能存在不稳定情况，请优先使用[[release]](https://github.com/gy-games/elves/releases "release")中的代码进行业务搭建。


# Community & ELVES-WIKI

https://gy-games.gitbooks.io/elves/

---

# 介绍

Elves为一套开源自动化运维开发平台\(IT Automatic Develop Platform\)，面向开发，注重以编程实现运维自动化，致力于为运维研发人员提供便捷的运维自动化业务编程实现环境， Elves自身不提供业务性功能，运维开发人员可根据自身的业务进行应用\(APP\)的开发来实现相应业务的自动化管理。

# 特性

灵活的业务\(App\)编程设计：Elves主要面向运维开发人员，以编程方式实现某业务的自动化操作，Elves与用户间交互以RESTful方式进行，与Apps间交互以进程调用方式进行，理论上支持所有的编程语言，目前Elves提供Python与C\#版开发SDK

任务模式：Elves提供及时任务\(同步\)，队列任务\(异步,支持依赖\)，计划任务\(异步\) 三种任务调度模式，且允许开发者直接将App-worker的执行结果直接反馈至App-processor，以构建C/S架构服务

高可用与高性能：在Elves的设计中各组件为可拔插形式，且极大程度的降低各组件间依赖关系，几乎所有组件均可以独立使用与集群部署

数据交互传输：Elves-Center间各组件的数据传输使用RABBITMQ以队列形式进行交互，Elves-Center与Elves-Agent间数据传输使用Thrift进行交互，开发人员操作Elves\(App\)使用RESTful方式交互

开发语言与结构：Elves自身以C/S架构设计，Elves-Center\(SERVER\)由JAVA实现，Elves-Agent\(CLIENT\)由Golang实现

# 定位

可能看完以上的介绍甚至看完\[[elves-wiki](https://gy-games.gitbooks.io/elves/content/intro.md)\]中的技术架构后以下的架构还会有些人有疑问，ELVES到底能做什么，它在运维自动化中扮演什么样的角色，这里来简单介绍一下，了解完后结合\[[ELVES实践案例](https://gy-games.gitbooks.io/elves/content/practice.md)\]能对ELVES有一个更清晰的认识。

**站在运维自动化系统实现角度**，运维自动化系统正走在向平台化，更优质的用户体验提升的道路上，往往此类产品均为WEB端或桌面的形式提供运维使用， 这类运维自动化系统若需要与业务操作系统OS或与操作系统上的服务进行交互的时候往往需要自己定义通讯以及调用的实现方式。通过ELVES后，此类运维自动化系统将可以全部面向统一的EVELS API接口，ELVES API的背后为运维所开发的各种业务的实现脚本。![](https://gy-games.gitbooks.io/elves/content/assets/system-implemention.png)

**站点运维团队与开发\(前端\)团队合作角度，**运维团队更懂系统，更懂业务并但产品感不强，前端等技能欠缺，开发\(前端\)团队产品感强，有较好的产品实现技能如前端JS,CCS等,但其不熟悉运维业务，更不了解具体业务实现。通过ELVES，开发\(前端\)团队将面向面向的ELVES API接口，运维团队将更加专注的面向脚本，面向具体功能的![](https://gy-games.gitbooks.io/elves/content/assets/op-with-dev.png)

---

# License
Licensed under the Apache License, Version 2.0

Copyright 2017-2018 Gy-Games, Inc.
