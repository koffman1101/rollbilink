# Rollbilink
ROLLBILINK® 是一个免费的路由级别的内网穿透项目。它专为流行的开源硬件和x86_64电脑设计，可以把树莓派（Raspberry Pi）、香橙派（Orange Pi R1 LTS）、各种PC机、笔记本电脑、服务器甚至VirtualBox和Vmware虚拟机变成支持P2P内网穿透的路由器。 

最有趣的是，你只要制作一台ROLLBILINK路由器，就可以和任何同样拥有ROLLBILINK路由器的人共享局域网——如同在互联网之上又搭建了一张安全的专线网络那样。

# 支持的硬件
ROLLBILINK®已经支持下列开源硬件和基于x86_64平台的硬件及虚拟机。

| 平台 |	处理器 |	核心 |	架构 |	操作系统  |
|----------------|---------|---------|---------|--------------------|
| Raspberry Pi 1 |	BCM2835 |	ARM1176 |	arm6hf |	Raspbian Lite (32bit) |
| Raspberry Pi 2 |	BCM2836 |	Cortex-A7 |	armhf |	Raspbian Lite (32bit) |
| Raspberry Pi 3 |	BCM2710 |	Cortex-A53 |	arm7hf |	Raspbian Lite (64bit) |
| Raspberry Pi 4 |	BCM2711 |	Cortex-A72 |	arm64 |	Raspbian Lite (64bit) |
| Raspberry Pi 5 |	BCM2712 |	Cortex-A76 |	arm64 |	Raspbian Lite (64bit) |
| Orange Pi R1 Plus LTS |	RK3328 |	Cortex-A53 |	arm64 |	Ubuntu 64bit server (bionic) |
| MediaTek |	MT7620N/A |	MIPS24Kec |	mips |	Linux 2.6.36 SDK |
| Computer |	x86 compatible series |	/ |	x86_64 |	Ubuntu 64bit server (bionic) |
| VirtualBox |	Same as the host |	Same as the host |	x86_64 |	Ubuntu 64bit server (bionic) |
| QEMU |	any |	any |	any |	Ubuntu 64bit server (bionic) |

# 项目简介
ROLLBILINK® 作者旨在创造一种可以利用闲置且廉价的硬件资源在互联网上灵活搭建虚拟局域网的方案。

术语 "ROLLBILINK" 有双层含义:

+ 它取自中文“若比邻”的谐音，隐喻无论身处何地，它都可以让你像在家里一样方便地使用内部网络。
+ 它由三个词元：ROLL | BI | LINK 组成，依次代表产出、商务智能以及链路，意指一种可以为商务行为服务的智能网络链路。

# 工作原理
不同于大多数基于协议识别和端口映射的反向代理方案，例如Zerotier、Linker、Frp等等，ROLLBILINK® 是一台完整的路由器。它向上以PPPoE拨号、DHCP或者静态地址配置的方式接入ISP运营商网络，向下则提供DHCP服务，支持有线和WLAN链路，为客户分配IP地址并且处理基础的L3路由转发业务。 同时，它还拥有一些令人兴奋的新特性。

+ 一个免费的公共调度服务器建在云上，是完全透明的，用户不会感知到它的存在。
+ ROLLBILINK® 路由器首先建立到调度服务器的安全链路。经由此服务器，不同的节点能够基于安全策略彼此发现并穿越NAT建立透明的P2P隧道。
+ ROLLBILINK® 网络是星型的。每个虚拟局域网有且只有1个服务节点和多个客户节点。每个客户节点和服务节点之间基于一条透明的P2P隧道互联。同一个虚拟局域网内的节点都可以互通。
+ 基于L3/L4层设计，对应用层透明。即装即用，装完既忘，无需用户了解网络知识。
+ 支持UDP和TCP两种P2P隧道协议。内置的选路算法优先使用UDP，它穿越NAT的能力更强、速度更快，还能最大程度地利用带宽。
+ ROLLBILINK® 路由器正常处理L3转发。因此可以平替家庭路由器或者作为二级路由器使用。
+ ROLLBILINK® 路由器作为二级路由器或者旁路方式部署时不会影响用户已有网络拓扑。

# 基本用法
+ 准备至少两台硬件，可以是树莓派，香橙派 R1 Lts或者电脑，虚拟机之类的。
+ 下载最新制作好的Release固件，通常是xz压缩的格式，或者ISO安装文件。
+ 解压xz格式的固件。
+ 用Rufus或者其它烧录工具将固件或ISO文件烧录到一张高速Micro SD卡上。
+ 对于树莓派全系和香橙派R1 Lts用户，将制作好的Micro SD卡插入卡槽，然后上电启动。
+ 对于x86_64电脑、工控机、虚拟机用户，基于同样的方法用Rufus制作一张USB启动盘，然后安装。
+ 将一台ROLLBILINK配置成Server，其它的ROLLBILINK配置成Client就可以联通了。

想了解更多信息，请访问 [作者的主页](http://www.rollbilink.com).

# 许可协议
本项目是完全免费的，可以随意分发，并且没有任何显式和植入式广告。
---
# Rollbilink
ROLLBILINK® is a free routing-level internal network penetration project. It is specifically designed for popular open-source hardware and x86_64 computers, and can turn Raspberry Pi, Orange Pi R1 LTS, various PCs, laptops, servers, even VirtualBox and VMware virtual machines into routers that support P2P internal network penetration.

Best of all, you just make a ROLLBILINK router and you can share your LAN with anyone who also has a ROLLBILINK router.</p>

# Hardware
It supports the open-source hardwares listed in the following table.

| Product |	Processor |	Core |	Architecture |	OS  |
|----------------|---------|---------|---------|--------------------|
| Raspberry Pi 1 |	BCM2835 |	ARM1176 |	arm6hf |	Raspbian Lite (32bit) |
| Raspberry Pi 2 |	BCM2836 |	Cortex-A7 |	armhf |	Raspbian Lite (32bit) |
| Raspberry Pi 3 |	BCM2710 |	Cortex-A53 |	arm7hf |	Raspbian Lite (64bit) |
| Raspberry Pi 4 |	BCM2711 |	Cortex-A72 |	arm64 |	Raspbian Lite (64bit) |
| Raspberry Pi 5 |	BCM2712 |	Cortex-A76 |	arm64 |	Raspbian Lite (64bit) |
| Orange Pi R1 Plus LTS |	RK3328 |	Cortex-A53 |	arm64 |	Ubuntu 64bit server (bionic) |
| MediaTek |	MT7620N/A |	MIPS24Kec |	mips |	Linux 2.6.36 SDK |
| Computer |	x86 compatible series |	/ |	x86_64 |	Ubuntu 64bit server (bionic) |
| VirtualBox |	Same as the host |	Same as the host |	x86_64 |	Ubuntu 64bit server (bionic) |
| QEMU |	any |	any |	any |	Ubuntu 64bit server (bionic) |

# Overview
The authors of ROLLBILINK® aim to create a solution that can flexibly build virtual local area networks on the Internet by utilizing idle and inexpensive hardware resources.

The term "ROLLBILINK" has a dual meaning:

+ It is derived from the homophonic sound of the Chinese phrase "若比邻[ruò bǐ lín]" and metaphorically implies that no matter where you are, it enables you to use the internal network as conveniently as if you were at home.
+ It is composed of three words: ROLL | BI | LINK, which respectively represent output, business intelligence and link, indicating an intelligent network link that can serve business activities.

# Principle
Unlike most reverse proxy solutions based on protocol identification and port mapping, ROLLBILINK® is a true router. It connects to the ISP operator network via PPPoE dial-up, DHCP or static address configuration on the upper layer, and provides DHCP services on the lower layer, supporting wired and WLAN links, allocating IP addresses for customers and handling basic L3 routing forwarding tasks. At the same time, it also has some exciting new features.

+ A free public scheduling server is built on the cloud and is completely transparent. Users will not be aware of its existence.
+ The ROLLBILINK® router first establishes a secure link to the scheduling server. Through this server, different nodes can discover each other based on security policies and establish transparent P2P tunnels across the NAT.
+ The ROLLBILINK® network is star-shaped. Each virtual local area network has exactly one service node and multiple client nodes. Each client node and service node are interconnected through a transparent P2P tunnel. Nodes within the same virtual local area network can communicate with each other.
+ The ROLLBILINK® router is designed based on the L3/L4 layers and is transparent to the application layer. It can be installed and used immediately, and once installed, users will forget about it. There is no need for users to have knowledge of the network.
+ Supports both UDP and TCP P2P tunneling protocols. The built-in routing algorithm prioritizes the use of UDP. It has stronger ability to traverse NAT, faster speed, and can make the best use of bandwidth.
+ The ROLLBILINK® router can handle L3 forwarding normally. Therefore, it can replace a home router or be used as a secondary router.
+ When the ROLLBILINK® router is deployed as a secondary router or in a bypass mode, it will not affect the existing network topology of the users.

# Usage
+ Prepare at least two pieces of hardware, which can be Raspberry Pi, Orange Pi R1 Lts or a computer, virtual machine or the like.
+ Download the latest release file that has been compressed with xz.
+ Extract the file.
+ Use Rufus or other tools to write it onto the micro SD card.
+ Insert the micro SD card into the card slot and power it on to start. (For Raspberry Pi and Orange Pi)
+ Create a USB bootable stick with the iso file and then install it on your computer or virtual machine.
+ Configure one Raspberry Pi as a server and the other as a client.

For complete usage instructions, please visit the [Author's Homepage](http://www.rollbilink.com).

# License
This project is completely free and will not incorporate any form of advertisements.
