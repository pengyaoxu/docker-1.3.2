近期研究docker容器迁移方案，看到hustcat大神的实现，实在佩服，费了九牛二虎之力才把这个低版本的改良型docker编译成功，下面盗用作者的一些介绍：

概述
==================================

Ceph的RBD支持快照，我们可以通过RBD，让Docker的rootfs也跑在网络存储之上，从而实现OS、数据全部跑在网络上，从而打造无本地磁盘的容器服务。

逻辑示意图：

![struct](http://hustcat.github.io/assets/2015-07-24-docker-on-ceph.jpg)
