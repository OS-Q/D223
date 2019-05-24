# [LoRa Module](https://github.com/OS-Q/D113)

[![sites](OS-Q/OS-Q.png)](http://www.OS-Q.com)

#### 归属广域网络：[W17](https://github.com/OS-Q/W17)

#### 关于系统架构：[OS-Q](https://github.com/OS-Q/OS-Q)

## [设备描述](https://github.com/OS-Q/D113/wiki) 

最大特点就是在同样的功耗条件下比其他无线方式传播的距离扩大3-5倍，实现了低功耗和远距离的统一(低通信速率)。

LoRa Module设备用于接入LoRa网络，该设备封装了相应的MAC层协议如loRaWAN/CLAA等，可以通过通信端口直接发送数据内容进入相应的通信网络，设备的通信和状态由模块维护。

阿里云2019年将推进LoRa2.0 时代，以室内为主，LoRa开始在室内与IoT Wifi开始对比，而由于特性的优势，LoRa只需要一个网关便可以覆盖室内环境下面的所有角落，实现零盲点覆盖。未来LoRa的私有协议的应用会慢慢的受到挤压，而LoRaWAN标准协议的应用会越来越广泛。

##### 关于LoRa调制芯片：

[SX1276](https://www.semtech.com/products/wireless-rf/lora-transceivers/sx1276#download-resources) [SX1278](https://www.semtech.com/products/wireless-rf/lora-transceivers/sx1278#download-resources) 是Semtech公司2013年推出的产品，[SX1262](https://www.semtech.com/products/wireless-rf/lora-transceivers/SX1262#download-resources) [SX1268](https://www.semtech.com/products/wireless-rf/lora-transceivers/SX1268#download-resources)是Semtech公司2018年推出的产品，都是单纯的无线收发器件。

翱捷科技(ASR)的SiP整合方案 [ASR6501](http://www.asrmicro.com/asrweb/products/html/product2_1.html)

#### loRaWAN协议：

node和服务器正常交互需要先入网，需要有以下参数：

* NwkSKey（MIC校验时会用到）
* AppSKey （AES加解密用到）
* DevAddr (数据通讯使用的node短地址)
* DevEui (OTAA入网会用到)

##### 入网方式：

ABP (Activation By Personalization)：入网信息已固化在设备上，设备上电已经入网

OTAA(Over-The-Air Activation)，node端在做OTAA入网之前，需要先具备三个参数：

* APPEUI node自定义的8字节长地址
* APPKEY 服务器和node端都事先存好，用于对Join_acept message 做加解密处理
* DevNonce 2字节的随机数，用于生成随机的AppSKey和NwkSKey

### [设备资源](https://github.com/OS-Q/)

* [文档](docs/)
* [资源](src/)
	* [STM32L0 Keil工程](src/STM32L0)

### [组织关系](https://github.com/OS-Q/113)

* W17：[广域网络](https://github.com/OS-Q/W17)
	* D113：LoRa module
	* D114：[NB moduleA](https://github.com/OS-Q/D114)
	* D115：[NB moduleS](https://github.com/OS-Q/D115)
	* D116：[2G moduleA](https://github.com/OS-Q/D116)
	* D117：[2G moduleS](https://github.com/OS-Q/D117)
	* D118：[4G moduleA](https://github.com/OS-Q/D118)
	* D119：[4G moduleS](https://github.com/OS-Q/D119)

### [使用建议](https://github.com/sochub)

OS-Q中设定的LoRa设备和工程有5个，其中3个归属于[通信管道](https://github.com/OS-Q/M4)，一个归属[通信终端](https://github.com/OS-Q/M5)，一个归属[通信网关](https://github.com/OS-Q/M6)。

OS-Q中定义的其他LoRa设备：

* [LoRa-COM](https://github.com/OS-Q/D101)
* [LoRa-USB](https://github.com/OS-Q/D109)
* 终端设备[LoRa-Device](https://github.com/OS-Q/D148)
* 网关设备[LoRa-Router](https://github.com/OS-Q/D170)

管道通信设备和终端通信设备的区别在于：管道设备驱动程序不需要基于系统开发，也不涉及固件的升级，更多是为了完成特定的数据收发和控制，所以对设备的处理能力和资源要求不高，最求较低的成本和适用性。

管道通信设备中处理单元不同，[LoRa-COM](https://github.com/OS-Q/D101) 趋紧物理接口封装，[LoRa-USB](https://github.com/OS-Q/D109)追求和上位机系统的适配驱动，如Linux系统平台通信，[LoRa module](https://github.com/OS-Q/D113)封装相应的协议数据，分摊了连接平台的开发难度。


### [OS-Q : Operation System for edge devices](http://www.OS-Q.com/Edge/D113)
####  2019-5-21

