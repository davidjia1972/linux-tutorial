### 一、什么是 Linux？
**Linux** 是一个类 Unix 操作系统，核心部分是 Linux Kernel（内核）。内核本身只负责最底层的任务，如进程调度、内存管理、硬件驱动等。而我们平时使用的 “Linux 系统” 实际是：

+ **Linux 内核（Kernel）**
+ **一组 GNU 工具和软件包管理系统**
+ **各种桌面环境、服务程序与用户工具**

这些被集成打包后，形成了各种不同的 **Linux 发行版（Distribution）**，简称 **发行包（distro）**。

### 二、常见的 Linux 发行版及其特点
| 发行版 | 上游关系 | 包管理器 | 特点说明 |
| --- | --- | --- | --- |
| **Ubuntu** | Debian | `apt` | 最流行的桌面/服务器发行版之一，文档丰富，入门友好 |
| **Debian** | 无（上游） | `apt` | 稳定、保守，社区驱动，常被用作其他发行版的基础 |
| **CentOS** | RHEL（已停更） | `yum`/`dnf` | 企业环境常用（目前建议改用 Rocky / AlmaLinux） |
| **Rocky Linux** | RHEL | `dnf` | CentOS 替代者，100% 兼容 RHEL |
| **AlmaLinux** | RHEL | `dnf` | 企业级兼容，社区支持良好 |
| **Fedora** | RHEL 上游 | `dnf` | 新技术实验地，更新快，Red Hat 赞助 |
| **Arch Linux** | 无（独立） | `pacman` | 极简、滚动更新、完全自主搭建，适合进阶用户 |
| **openSUSE** | SUSE | `zypper` | 提供图形工具 Yast 管理系统，适合企业与开发者 |
| **Kali Linux** | Debian | `apt` | 专为渗透测试与安全研究打造 |
| **Linux Mint** | Ubuntu | `apt` | 更符合 Windows 使用习惯，适合桌面用户 |
| **Raspberry Pi OS** | Debian | `apt` | 为树莓派优化的小型系统 |


> 注：Ubuntu 是培训和教学中最常见的选择，尤其在服务器场景下的 Ubuntu Server。本教程也是针对Ubuntu编写的。
>

### 三、不同 Linux 发行版之间的区别
#### 3.1 技术基础不同
+ 有些发行版是“源头发行版”（如 Debian、Arch、Gentoo）；
+ 有些发行版是“下游再发行版”，从上游继承并加入定制（如 Ubuntu 基于 Debian）；

#### 3.2 包管理系统不同
| 包管理器 | 典型发行版 |
| --- | --- |
| `apt` | Debian、Ubuntu |
| `dnf`/`yum` | CentOS、Fedora |
| `pacman` | Arch Linux |
| `zypper` | openSUSE |


#### 3.3 发布策略不同
| 发布策略 | 说明 |
| --- | --- |
| 定期发布 | 如 Ubuntu 每 6 个月更新一次 |
| 滚动更新 | 如 Arch Linux，软件持续更新无“版本号” |
| LTS 版本 | Ubuntu 的长期支持版，5 年支持周期 |
| 企业版 | RHEL、Rocky、AlmaLinux，稳定、安全、支持周期长 |


### 四、Linux 内核（Kernel）与发行版的关系
#### 4.1 什么是内核？
+ Linux Kernel 是整个操作系统的**心脏**，负责与硬件交互；
+ 所有 Linux 发行版都需要使用 Kernel，但可能使用不同的版本和配置。

#### 4.2 同一个 Kernel，不同的发行包
举个例子：

+ Ubuntu 和 Debian 都使用 Linux 内核，但 Ubuntu 默认内核更新更快；
+ Arch Linux 用户往往使用最新内核，而 Debian 更偏向稳定旧版。

#### 4.3 用户能否自己升级内核？
+ 可以！但通常不推荐新手手动升级。
+ 发行版提供的内核版本已经为兼容性、驱动、性能做过优化。

### 五、选择 Linux 发行版的建议（初学者篇）
| 需求场景 | 建议发行版 |
| --- | --- |
| 学习、培训 | Ubuntu Server (LTS) |
| 企业服务器 | Rocky Linux / Ubuntu |
| 桌面日常使用 | Linux Mint / Ubuntu Desktop |
| 渗透测试 | Kali Linux |
| 学习极客架构 | Arch Linux（进阶） |
| 嵌入式设备 | Raspberry Pi OS 等 |


### 六、示意图：Linux 内核与发行版关系图
```plain
                 [ Linux Kernel ]
                       |
       -------------------------------------------
      |           |                   |          |
   Debian       RedHat              Arch        SUSE
      |           |                   |          |
   Ubuntu     CentOS/Anolis/Rocky   Manjaro   openSUSE
      |
  Linux Mint
```

### 七、小结
+ Linux ≠ Ubuntu，它只是众多发行版之一；
+ 所有发行版本质上都围绕一个 Linux 内核；
+ 不同发行版侧重点不同，但使用基础大体一致（尤其是命令行）；
+ 本教程以 **Ubuntu Server LTS** 为教学系统，原因是稳定、文档丰富、易于部署。



