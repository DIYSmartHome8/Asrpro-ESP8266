# Asrpro-ESP8266<br>
天问离线语音模块ASRPro接入Homeassistant<br>
一直想找个离线的语音方案，最近朋友们推荐ASRPRO，说里面能跑神经网络，牛逼的很。<br>
体验了吧，确实太方便了。然后就有了这个分享。<br>
全开源：包含Gerber，3D Step，天问源码，ESPhome源码，稍后整理依次更新。。。<br>
#1、简介<br>
板子包含ASRPro，ESP8266，一个温湿度传感器（但实测发现，温度显示不正常，建议大家空贴。）一个红外接收，两个红外发送，用的IO跟红外伴侣一样。我这个例程，其实就是拿红外伴侣来改的。<br>
#2、框图<br>
![Image text](https://github.com/DIYSmartHome8/Asrpro-ESP8266/blob/main/IMG/No.1.jpg)<br>
温湿度传感器可能由于LDO或模块发热，数据不对，又或者是要校准什么的，没找到原因，所以不建议贴。<br>
#3、3D图<br>
![Image text](https://github.com/DIYSmartHome8/Asrpro-ESP8266/blob/main/IMG/No.2.jpg)<br>
#4、成品长这样<br>
![Image text](https://github.com/DIYSmartHome8/Asrpro-ESP8266/blob/main/IMG/No.3.jpg)<br>
碰巧是全黑的，所以我叫它小黑同学<br>
这个喇叭的线，这样焊接的，盖子开多了，有摇断的风险<br>
喇叭是直接卡进去的，买了两种喇叭，有一种尺寸不对<br>
![Image text](https://github.com/DIYSmartHome8/Asrpro-ESP8266/blob/main/IMG/No.4.jpg)<br>
喇叭定位及孔大小是按这个尺寸设计的<br>
![Image text](https://github.com/DIYSmartHome8/Asrpro-ESP8266/blob/main/IMG/No.5.jpg)<br>
#5、天问Block<br>
非常简单，通过串口把识别到的命令发给ESP8266，8266再通过WIFI传给Homeassistant<br>
![Image text](https://github.com/DIYSmartHome8/Asrpro-ESP8266/blob/main/IMG/No.6.jpg)<br>
#6、ESP8266部分<br>
ESP8266用Esphome处理，也非常简单，yaml及串口源码均已开源。
#7、最终效果视频<br>
顺带介绍了没用官方下载电路时的烧录时机
https://www.bilibili.com/video/BV1GF4m1N7by
