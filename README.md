# [LoRa module](https://github.com/OS-Q/D113)

[![sites](OS-Q/OS-Q.png)](http://www.OS-Q.com)

#### 归属广域网络：[W17](https://github.com/OS-Q/W17)

#### 关于系统架构：[OS-Q](https://github.com/OS-Q/OS-Q)

## [设备描述](https://github.com/OS-Q/D113/wiki) 



LoRa module设备用于接入LoRa网络，该设备封装了相应的MAC层协议如loRaWAN/CLAA等，可以通过通信端口直接发送数据内容进入相应的通信网络，设备的通信和状态由模块维护。

关于LoRa通信调制芯片：[SX1276](https://www.semtech.com/products/wireless-rf/lora-transceivers/sx1276#download-resources) 和 [SX1278](https://www.semtech.com/products/wireless-rf/lora-transceivers/sx1278#download-resources) 

阿里云将推进 LoRa2.0 时代

### [设备资源](https://github.com/OS-Q/)

* [资源](src/)
* [文档](docs/)
* [工程](project/)

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

在通信管道中定义的三个LoRa设备：

* [LoRa-COM](https://github.com/OS-Q/D101) 
* [LoRa-USB](https://github.com/OS-Q/D109)
* [LoRa module](https://github.com/OS-Q/D113)

管道通信设备和终端通信设备的区别在于：管道设备驱动程序不需要基于系统开发，也不涉及固件的升级，更多是为了完成特定的数据收发和控制，所以对设备的处理能力和资源要求不高，最求较低的成本和适用性。

管道通信设备中处理单元不同，[LoRa-COM](https://github.com/OS-Q/D101) 趋紧物理接口封装，[LoRa-USB](https://github.com/OS-Q/D109)追求和上位机系统的适配驱动，如Linux系统平台通信，[LoRa module](https://github.com/OS-Q/D113)封装协议数据（不单纯LoRa，还可以是loraWAN的协议），分摊了连接平台的开发难度。


### [OS-Q : Operation System for edge devices](http://www.OS-Q.com/Edge/D113)
####  2019-5-21

