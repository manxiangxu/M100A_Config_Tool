#M100A 非LoRaWAN配置工具使用说明
---
2016/9/26 更新 v0.1.3

---

##基本的界面如下图

![Alt text](http://ww3.sinaimg.cn/large/6c1ebe8egw1f9tsst777tj20hk0g6whk.jpg)



##功能A区域
- config 配置
该功能支持导入和保存配置参数文件，使用方式推荐先导入提供的参考配置参数文件，然后在参考配置基础上进行修改，最后保存为另外一个配置参数文件。
load为导入配置文件，save为保存配置文件。
- about
工具版本介绍

##功能B区域
- 串口选择
通过点击下拉列表来选择与模块连接的串口号。
- OPEN/CLOSE 按钮
串口打开和关闭按钮，串口打开状态下工具的配置参考能修改，串口关闭的状态下工具的配置参数不能修改。
工具使用的串口参数与模块的串口配置必须一致，工具的串口设置在功能D区域的USART页面里设置，工具要使用设置的新串口参数需要重新开启工具的串口来应用新串口配置参数。

注意：由于PC环境的串口可能出现接触不可靠的情况，导致串口无法使用，当出现工具无法读取或写入配置到模块中时，可以尝试关闭软件重新打开。

##功能C区域
- DevEui 设备的唯一标识码
DevEui为8字节，**大端模式**。

##功能D区域
分为2个设置页面
+ MAC LAYER
 -  Frequency 模块射频通信频率
 - SyncWord 模块射频的同步字。
 - PreambleLength 模块射频的前导码长度。
 - Tx power 模块射频发射功率
 - Datarate 模块射频数据速率（扩频因子）
 - BandWidth 模块射频的带宽
 - HeaderMode 模块射频的消息头模式
 - Coding Rate 模块射频的编码率
 - CRC Enable 模块射频的CRC使能控制。
 - RX IQ signal 模块的射频接收IQ信号是否反转
 - TX IQ signal 模块的射频发射IQ信号是否反转
 -  Debug Out Switch：模块debug串口输出开关。
+ USART
 - Baud 模块的通信串口波特率
 - Data Bits 模块的通信串口数据位
 - Stop Bits 模块的通信串口停止位
 - Parity Bits 模块的通信串口校验位
 
##功能E区域
- Write 为模块写入配置按钮
- Read 读取模块配置按钮 

---