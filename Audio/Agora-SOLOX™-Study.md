# Agora SOLO X™ 学习总结

![Agora SOLO X™  原文](https://mp.weixin.qq.com/s/R0BSDPSwuorAvtj4Y96KIw)


**丢包** : 包没有在规定的时间到达。 

**丢包原因**：现有网络条件、带宽限制以及差异化、系统的调度等。

**FEC**(Forward Error Correction）: 前向纠错

**PLC**（Packet Loss Concealment）: 丢包补偿技术

**RTT**(Round-Trip Time): 往返时延

**Agora SOLO™** :对重点信息加冗余，对非重点信息则去冗余

一帧2包（packet 1、packet 1'），每个包都可以恢复8kbps的窄带音频信号，同时收到就可恢复出一个 16kbps 的宽带高质量音频信号。

**Agora SOLO™ 特点**

接近完美的抗丢包编解码，因为没有完美的编解码器。

* 第一，更低延时。无需回传信道丢包信息，默认发送多倍数据；

* 第二，更高质量。收到一个包质量可达到普通编解码器水平，收到两个包质量即可达到高质量编解码的水平；

* 第三，面向多人环境；

* 第四，简化策略。无需策略调整，不担心策略颗粒度问题。


**FEC抗丢包遇到的问题：** 
*  1、丢包率算不准 
*  2、loss info 的包仍可能会丢失，以及FEC带来的网络带宽是浪费
*  3、长 RTT时抗丢包方案的效果是比较有限
*  4、成本因素链路绕个远

**编解**：压缩、去冗余

**抗丢包**：加冗余实现抗丢包

**PESQ**(Perceptual evaluation of speech quality) 即：客观语音质量评估。 ITU-T P.862建议书提供的客观MOS值评价方法。

** SOLO X™** : Agora SOLO™ 编码器的抗丢包部分移植到了 OPUS .

