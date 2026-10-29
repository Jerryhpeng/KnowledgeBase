NVMe读写按下图发送流程进行读写Admin命令：
![[Pasted image 20261029213325.png]]
NVMe Admin命令发送流程：
1、NVMe寄存器初始化完毕后Rdy信号拉高后，就进入到发送Admin命令阶段：
- 主机应通过发送 **Identify** 命令，获取 Controller 的数据结构（Controller Data Structure），来确定控制器的配置信息；
- 主机应针对每个 **Namespace** 分别发送 Identify 命令，并指定 Namespace 数据结构（Namespace Data Structure），以确定各个 Namespace 的配置信息。[[NVM-Express-1_3d-2019.03.20-Ratified.pdf#page=223&selection=220,0,231,1|NVM-Express-1_3d-2019.03.20-Ratified, 页面 223]]
- 