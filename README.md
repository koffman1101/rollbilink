# Rollbilink
A free P2P internal network penetration router system specifically designed for Raspberry Pi, Orange Pi, x86_64 computers and virtual machines. It supports the open-source hardwares listed in the following table.
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
ROLLBILINK® is a free public welfare project. It is specifically designed for popular open-source hardware and x86_64 computers. It can turn Raspberry Pi, Orange Pi R1 LTS, various PCs, laptops, servers, even VirtualBox and VMware virtual machines into routers that support P2P internal network penetration.

The term "ROLLBILINK" has a dual meaning:

+ It is derived from the homophonic sound of the Chinese phrase "若比邻[ruò bǐ lín]" and metaphorically implies that no matter where you are, it enables you to use the internal network as conveniently as if you were at home.
+ It is composed of three words: ROLL | BI | LINK, which respectively represent output, business intelligence and link, indicating an intelligent network link that can serve business activities.
# Principle
Unlike most reverse proxy solutions based on protocol identification and port mapping, ROLLBILINK® is a true router. It connects to the ISP operator network via PPPoE dial-up, DHCP or static address configuration on the upper layer, and provides DHCP services on the lower layer, supporting wired and WLAN links, allocating IP addresses for customers and handling basic L3 routing forwarding tasks. At the same time, it also has some exciting new features.

+ The ROLLBILINK® router first establishes a secure link to the scheduling server. Through this server, different nodes can discover each other based on security policies and establish transparent P2P tunnels across the NAT.
+ The ROLLBILINK® network is star-shaped. Each virtual local area network has exactly one service node and multiple client nodes. Each client node and service node are interconnected through a transparent P2P tunnel. Nodes within the same virtual local area network can communicate with each other.
+ The ROLLBILINK® router is designed based on the L3/L4 layers and is transparent to the application layer. It can be installed and used immediately, and once installed, users will forget about it. There is no need for users to have knowledge of the network.
+ Supports both UDP and TCP P2P tunneling protocols. The built-in routing algorithm prioritizes the use of UDP. It has stronger ability to traverse NAT, faster speed, and can make the best use of bandwidth.
+ The ROLLBILINK® router can handle L3 forwarding normally. Therefore, it can replace a home router or be used as a secondary router.
+ When the ROLLBILINK® router is deployed as a secondary router or in a bypass mode, it will not affect the existing network topology of the users.
# Usage
+ Download the release file that has been compressed with xz.
+ Extract the file.
+ Use Rufus or other tools to write it onto the micro SD card.
+ Insert the micro SD card into the Raspberry Pi and power it on to start.
+ Configure one Raspberry Pi as a server and the other as a client.

For complete usage instructions, please visit the [Author's Homepage ](http://www.rollbilink.com).
# License
This project is completely free and will not incorporate any form of advertisements.
