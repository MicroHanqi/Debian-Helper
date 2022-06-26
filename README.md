# Debian新手指引:flashlight:
# 您可以在此处直接阅读！
By MicroCode  On 2022-3-19  

> **Last update: 2022-3-26**
>
> **Update log:**
>
> **2022-3-19 心血来潮写下了第一句话**
>
> **2022-3-20 完成了第一部分的有关内容**
>
> **2022-3-23 完成了第二和第三部分的片面内容，并整改了一些小错误**
>
> **2022-3-25 更改了不通顺的句子，并修改了一些错误**
>
> **2022-3-26 完成了第三部分，并在原来的基础上增加了分区**
>
> **2022-3-26 第四部分动工，并且完善了第二部分**



# 0. 欢迎！:happy:

## “有朋自远方来，不亦乐乎。”

Debain ，是一个属于大家的系统，任何人都可以去使用它享受它品味它。无论你是身经百战的老鸟，还是初入毛庐的新手；无论你是一位编码机器，还是颅内编译器植入者，在这里，我们都有一个统一的身份，就是用户。Debian欢迎你，欢迎你加入这个大家庭。但你需要明白，万事开头难，重在坚持，持之以恒很艰难，半途而废很简单。使用好，会使用Linux是一个漫长的过程，在这一过程，我们需要不断积累沉淀，提升自我。正如一句名言所说：“成功是一段路程，而非终点，所以只要在迈向成功的过程中一切顺利，便是成功。”让我们一起步入Linux殿堂，去好好品味享受它吧！

**谢谢你看完了我这么多罗嗦的东西！:drum:**



# 1. 什么是Debian和GNU/Linux？:sunflower:

## “夜来风雨声，花落知多少？”

***Debian：***Debian是一个自由的开源的操作系统，他是Linux的分支。Debian计划创建于 1993 年。Debian项目是由一组人的创造和分配作为开源软件免费的操作系统。这个软件称为Debian GNU /  Linux或者干脆Debian的。它支持多种平台，包括英特尔和PowerPC，ARM，MIPS，和其他人。目前，Debian的系统使用的Linux内核。 Linux是一个软件是由Linus Torvalds开始，支持数以千计的程序员的世界各地。

***GNU/Linux：***Linux是一种计算机操作系统： 一系列能让您与计算机进行交互操作并运行其它程序的程序。 操作系统由多种基础程序构成。它们使计算机可以与用户进行交流并接受指令，读取数据或将其写入硬盘、磁带或打印机，控制内存的使用，以及运行其它软件。操作系统最重要的组成部分是内核。在GNU/Linux系统中，Linux就是内核组件。而该系统的其余部分主要是由GNU工程编写和提供的程序组成。因为单独的 Linux  内核并不能成为一个可以正常工作的操作系统，所以我们更倾向使用 “GNU/Linux” 一词来表达人们通常所说的 “Linux”。Linux是以 Unix操作系统为原型创造的。自从诞生之日起，它就被设计成一种多任务、多用户的系统。这些特点使Linux完全不同于其它著名的操作系统。事实上Linux比您所能想象到更加特别。与其它操作系统绝然相反的是，没人真正拥有Linux，其大部分开发工作都是由无偿的志愿者完成的。 后来演变为GNU/Linux系统的开发工作开始于1984年。当时，自由软件基金会开始研发被称为GNU的自由的类Unix操作系统。 

**你已经了解了一些关于Linux的知识，你已经跨入大门了！:drum:**

# 2. 我如何获取/安装Debian？:notebook_with_decorative_cover:

## “千里之行，始于足下。”

***获取Debian***，你需要知道一些关于Debian镜像的一些知识。其中，amd64代表的是64位CPU，i686则是32位CPU，千万不要搞混了。Debian的发行版分“Sid不稳定版”“Testing测试版”和“Stable稳定版”。其中，“Stable稳定版”包比较旧，此版本最稳定；“Testing测试版”相比前面的版本系统较新，稳定性也没有差到哪里去；“Sid不稳定版”改版本的软件最新。但是包含了许多的Bug；日常使用推荐“Testing测试版”如果是生产环境的话建议使用“Stable稳定版”。然而“Testing测试版”和“Stable稳定版”又分“Non-Free”，这个是给需要特殊驱动的设备使用的，里面包含了私有驱动。其中除了“Sid不稳定版”官方不提供下载（可以通过更新来解决，包括Stable升级到Testing，下面会讲。），其他两个版本官方都有下载地址。

获取Debian无非就三种方案：1.通过官方进行下载。2.通过镜像站。我们先来讲第一种通过官方进行下载：

首先进入Debian官网：https://www.debian.org/ 然后点击更多，你会在右侧看到蓝色的下载按钮。点击一下可以跳转到下载页面。我们只需要关心第一个，下载一个安装映像。里面提供两个选项，它们分别是：“一个小型安装映像”和“较膨大的完整安装镜像”。前者体积很小，但是它的全部安装过程都是需要网络连接的。后者顾名思义，就是减少了前者所依赖网络的先决条件。注意了，在这里下载并不会找到“Non-Free”版本的iso文件**（特殊情况下）**，如需下载请看方案2。你需要做的就算选择架构，然后下载到你的电脑上，并进行刻录。

我们再来讲讲第二种通过镜像站来下载镜像：

很多人会疑问，不是通过官方就可以了吗，为什么还需要镜像站？这是因为大多数厂商的服务器架设在国外，普通人访问较为缓慢。这时就需要一个位于国内的镜像服务器来帮助我们了。下面是国内主流的镜像站：

> 1. 清华大学开源软件镜像站：https://mirrors.tuna.tsinghua.edu.cn/
> 2. 中科大镜像站：https://mirrors.ustc.edu.cn/
> 3. 阿里巴巴开源镜像站：https://developer.aliyun.com/mirror/
> 4. 上海交通大学源镜像服务：https://mirror.sjtu.edu.cn/
>
> 我们任意挑选一个进入，进去之后大同小异，以清华大学为例，我们选择“获取下载链接”然后会看到“Debian”和“Debian-Non-Free”，在前面我们已经阐述他们的区别了，所以这里就不过多赘述。我们选择适合自己电脑的版本和是否包括桌面环境，然后点击镜像进行下载。然后等它下载到你的电脑上，并进行刻录。**（一般我们选择普通版即可。）**

***安装Debian***，其实也非常简单，我们只需要将刻录好的系统优盘，插入到你的电脑并选择从U盘启动即可。如果在安装过程中出现了：“固件缺失”之类的问题，你需要下载“Non-Free”版本的系统镜像。然后一步一步来到分区这里，我会详细的告诉你如何分区：

首先为何分区？在 Linux 中，每一个硬件设备都映射到一个系统的文件，对于硬盘、光驱等 IDE 或 SCSI 设备也不例外。Linux 把各种 IDE 设备分配了一个由 hd 前缀组成的文件；而对于各种 SCSI 设备，则分配了一个由 sd 前缀组成的文件。

下面我来提供一些分区方案：

> **分两个区**
>
> 实际上，很多时候我们只需要分两个区：`/`和交换分区，日常使用基本不会有任何影响，甚至于交换分区对于现在的电脑来说都不是必要的，我们完全可以只分配一个根分区。linux只需要一个/根分区就可以正常运行。
>
> **常用分区方式**
>
> 引导分区 挂载点/boot 分区格式ext4 1G以内即可
>
> 交换分区 无挂载点 分区格式选择交换分区（swap） 最大不建议超过真实内存大小，除非内存小于2G，你的内存大于4G，推荐2G即可，没必要有些人推荐的与内存相当。
>
> 主目录　挂载点/　分区格式ext4 大小大约20-40G
>
> 家目录　挂载点/home 分区格式ext4 剩下的所有空间
>
> **（这里只列出了常用的，磁盘为100GB，请看情况更改，站在新手角度上面考虑的。）**

下面到了选择桌面的地方，你可能会犹豫不决，没关系，你可以看看下面：

> **1. KDE**
>
> KDE 是 K Desktop Environment 的缩写，中文译为“K桌面环境”。KDE 是基于大名鼎鼎的 Qt的，最初于 1996 年作为开源项目公布，并在 1998 年发布了第一个版本，现在 KDE 几乎是排名第一的桌面环境了。许多流行的 Linux 发行版都提供了 KDE 桌面环境，比如 Ubuntu、Linux Mint、OpenSUSE、Fedora、Kubuntu、PC Linux OS 等。DE 和 Windows 比较类似，各位初学者相信都是 Windows 的用户，所以切换到 KDE 也不会有太大的障碍。
>
> **2. GNOME**
>
> GNOME 是 the GNU Network Object Model Environment 的缩写，中文译为“GNU网络对象模型环境”。GNOME 于 1999 年首次发布，现已成为许多Linux发行版默认的桌面环境（不过用得最多的是 Red Hat Linux）。GNOME 的特点是简洁、运行速度快，但是没有太多的定制选项，用户需要安装第三方工具来实现。
>
> **3. Unity**
>
> Unity 是由 Ubuntu 的母公司 Canonical 开发的一款外壳。之所以说它是外壳，是因为 Unity 运行在 GNOME 桌面环境之上，使用了所有 GNOME 的核心应用程序。
>
> **4. MATE**
>
> 上面我们提到，GNOME 3 进行了全新的界面设计，这招致一些用户的不满，他们推出了其它的桌面环境，MATE 就是其中之一。
>
> **5. Cinnamon**
>
> 与 MATE 类似，Cinnamon 是由 Linux Mint 团队因为不满 Gnome 3 的改进而开发的另一种桌面环境。但  Cinnamon 与 MATE 不同之处在于，Cinnamon 建立在 Gnome 3 的基础上。Cinnamon  是新的，而且在积极开发之中，但这款出色的桌面环境没有因新颖而在功能方面有所减弱。
>
> **6. Xfce**
>
> Xfce 是类 UNIX 操作系统上的轻量级桌面环境。虽然它致力于快速与低资源消耗，但仍然具有视觉吸引力且易于使用。
>
> **7. 适用于较老硬件设备的 Linux 桌面环境**
>
> 图形化桌面环境的弊端在于它们要占用相当一部分的系统资源来保证正常运行。在 Linux 发展之初，Linux 的标志和卖点之一就是它可以运行在处理能力较弱的老旧 PC 上，这些 PC 无力运行较新的 Windows 桌面。
>
> 然而随着 KDE 和 GNOME 桌面环境的普及，情况发生了变化。运行 KDE 或 GNOME 桌面要占用的内存资源和较新的 Windows 桌面环境旗鼓相当。
>
> 如果你的 PC 已经有些年代了，也不要泄气。Linux 开发人员已经联手让 Linux  返璞归真。他们开发了一些低内存开销的图形化桌面应用，提供了能够在老旧 PC  上完美运行的基本功能。尽管这些图形化桌面环境并没有大量专为其设计的应用，但它们仍然能运行许多基本的图形化程序，支持如文字处理、电子表格、数据库、绘图以及多媒体等功能。
>
> 下表列出了一些可在配置较低的 PC 和笔记本电脑上运行的轻量级 Linux 图形化桌面环境。
>
> 
>
> | 桌面环境 | 说明                                                         |
> | -------- | ------------------------------------------------------------ |
> | Fluxbox  | 一个没有面板的轻型桌面，仅有一个可用来启动程序的弹出式菜单。 |
> | Xfce     | 和 KDE 很像的一个桌面，但少了很多图像以适应低内存环境。      |
> | JWM      | Joe 的窗口管理器（Joe’s Window Manager），非常适用于低内存低硬盘空间环境的超轻型桌面。 |
> | Fvwm     | 支持如虚拟桌面和面板等高级桌面功能，但能够在低内存环境中运行。 |
> | fvwm95   | 从 fvwm 衍生而来，但看起来更像是 Windows 95 桌面。           |
>
> **注意了，以上可能不完全，忘大家多多包涵！**

相信你看完上面，应该心里有自己的选择了。等待进度条跑完，你已经成功安装了Debian！

**至此，你已经成功步入了Debian的大门！:drum:**

# 3. 安装了系统我要怎样更新？:package:

## “欲渡黄河冰塞川，将登太行雪满山。”

***更改镜像源&更新***：刚刚拿到新的系统，你可能会抱怨软件包太旧。这不是你的问题，原因是Debian系统在开发时，都在向稳定可靠的方面考虑。所以在软件包上会守旧。前面阐述了Debian分为“Sid不稳定版”“Testing测试版”和“Stable稳定版”。其中我想说的是对于Sid，如果你不是Arch后遗症，不是风滚草滚傻的，不是在Debian上用yay的就别更新，Bug太多。对于剩下的两个分支，我推荐“Testing测试版”。因为它不但激进而且稳定。下面让我们来看看，如何升级到/更新到其他分支（**注意，你需要将软件源配置文件中的所有内容替换成下面你要选择的内容！）**：

***更新系统：***

在Debian更新系统，你只需要执行`sudo apt-get update`和`sudo apt-get upgrade`即可，如果你是更新发行版/分支，那么请执行`sudo apt-get dist-upgrade`,其中apt-get可以换为apt。



***从“Stable稳定版”更新到其他分支：***

***首先是从“Stable稳定版”更新到“Testing测试版”:***

你只需要修改你的镜像源即可，这里拿清华源为例子：

Debian 的软件源配置文件是 `/etc/apt/sources.list`。将系统自带的该文件做个备份，将该文件替换为下面内容，即可使用 TUNA 的软件源镜像。

```Testing镜像源
#从“Stable稳定版”更新到“Testing测试版”
# 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
deb https://mirrors.tuna.tsinghua.edu.cn/debian/ testing main contrib non-free
# deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ testing main contrib non-free
deb https://mirrors.tuna.tsinghua.edu.cn/debian/ testing-updates main contrib non-free
# deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ testing-updates main contrib non-free

deb https://mirrors.tuna.tsinghua.edu.cn/debian/ testing-backports main contrib non-free
# deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ testing-backports main contrib non-free

deb https://mirrors.tuna.tsinghua.edu.cn/debian-security testing-security main contrib non-free
# deb-src https://mirrors.tuna.tsinghua.edu.cn/debian-security testing-security main contrib non-free
```

在添加完成后，你需要进行系统更新：你只需要执行`sudo apt-get update`，`sudo apt-get upgrade`和`sudo apt-get dist-upgrade`，这三个命令即可。其中apt-get可以换为apt。这一过程会有点缓慢。更新完成后别忘记重启

***其次，是由“Stable稳定版”更新到“Sid不稳定版”***

你只需要修改你的镜像源即可，这里拿清华源为例子：

Debian 的软件源配置文件是 `/etc/apt/sources.list`。将系统自带的该文件做个备份，将该文件替换为下面内容，即可使用 TUNA 的软件源镜像。

```Sid镜像源
#从“Stable稳定版”更新到“Sid不稳定版”
# 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
deb https://mirrors.tuna.tsinghua.edu.cn/debian/ sid main contrib non-free
# deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ sid main contrib non-free
```

在添加完成后，你需要进行系统更新：你只需要执行`sudo apt-get update`，`sudo apt-get upgrade`和`sudo apt-get dist-upgrade`，这三个命令即可。其中apt-get可以换为apt。这一过程会有点缓慢。更新完成后别忘记重启

***然后是从“Testing测试版”更新到“Sid不稳定版”:***

你只需要修改你的镜像源即可，这里拿清华源为例子：

Debian 的软件源配置文件是 `/etc/apt/sources.list`。将系统自带的该文件做个备份，将该文件替换为下面内容，即可使用 TUNA 的软件源镜像。

```Sid镜像源
#从“Testing测试版”更新到“Sid不稳定版”
# 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
deb https://mirrors.tuna.tsinghua.edu.cn/debian/ sid main contrib non-free
# deb-src https://mirrors.tuna.tsinghua.edu.cn/debian/ sid main contrib non-free
```

在添加完成后，你需要进行系统更新：你只需要执行`sudo apt-get update`，`sudo apt-get upgrade`和`sudo apt-get dist-upgrade`，这三个命令即可。其中apt-get可以换为apt。这一过程会有点缓慢。更新完成后别忘记重启。

**至此，你距离熟练掌握Linux的使用，又进了一步！:drum:**

