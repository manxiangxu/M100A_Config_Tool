#M100A LoRaWAN配置工具使用说明
---
##基本的界面如下图

![Alt text](http://ww2.sinaimg.cn/large/6c1ebe8egw1f9tszm33pwj20hl0j3djd.jpg)

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
工具使用的串口参数为：115200bps，8E1，无奇偶校验。不支持修改。

注意：由于PC环境的串口可能出现接触不可靠的情况，导致串口无法使用，当出现工具无法读取或写入配置到模块中时，可以尝试关闭软件重新打开。

##功能C区域
- DevEui 设备的唯一标识码
DevEui为8字节，**大端模式**。

##功能D区域
分为4个设置页面
+ ACTIVATION 节点激活方式
 - Activation有Over the Air（OTAA）空中激活和Personalization（ABP）自定义激活方式。
 - AppEui 应用标识：**大端模式**，用于OTAA激活方式。
 - AppKey 应用AES-128密钥：用于OTAA激活方式。
 - Device address 设备地址：**大端模式**，用于ABP激活方式。
 - NwkSKey 网络会话密钥：用于ABP激活方式。
 - AppSKey 应用会话密钥：用于ABP激活方式。
+ MAC LAYER LoRaWAN Mac 层
 - Tx power 模块射频发射功率
 - Datarate 模块射频数据速率
 - ADR 自适应数据速率
 - Network type LoRaWAN 网络类型
 - Channel mask 信道屏蔽
 - Transmission redundancy 传输冗余：指仅上行不需要确认的消息的重传次数（消息发送失败的情况）。
 - Receive delay 1：接收窗口1延迟时间。
 - Receive delay 2：接收窗口2延迟时间。
 - Join accept delay 1：OTAA激活方式时接收入网请求确认消息1的延迟时间。
 - Join accept delay 2：OTAA激活方式时接收入网请求确认消息2的延迟时间。
 - Rx2 Channels 接收窗口2 信道配置：
   Frequency 接收频率
   Datarate 接收数据速率
+ CHANNELS 信道
 - 模块支持配置16个信道的参数，用于LoRaWAN中的跳频。
 - FREQUENCY 值当前信道的射频频率。
 - DR_MIN 指信道的最低数据速率。
 - DR_MAX 指信道的最高数据速率。
 - Disable 按钮为取消使用该信道，会将频率设置为0，最大和最小数据速率设置为DR_SF12。
+ APPLICATION 模块内置应用的选择
 -  Application mode：模块运行应用的选择。
 -  Tx duty dycle：模块应用自动上行数据周期时间。
 -  Tx duty dycle random：模块应用自动上行数据周期随机时间。
 -  Enable debug printf：模块debug串口输出开关。
 
##功能E区域
- Write 为模块写入配置按钮
- Read 读取模块配置按钮 

---
###配置项的详细含义请查阅LoRaWAN白皮书