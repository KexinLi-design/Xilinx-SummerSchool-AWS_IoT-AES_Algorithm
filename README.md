# Xilinx-SummerSchool-AWS_IoT-AES_Algorithm
Xilinx-SummerSchool-AWS_IoT-AES_Algorithm

作品名称：基于SEA Board的AES加密算法在AWS物联网中的应用
<br />板卡型号：SEA开发板——Xilinx xc7s15ftgb196-1芯片
<br />成员姓名：杜娟    06017111  东南大学；李可欣  06017109  东南大学

<br />❀项目简介：
<br />❈设计目的
<br />    为了满足当下在信息安全领域的广泛需求，我们设计的是一个在物联网信息传输中的AES加密、解密装置。由FPGA的ADC串口输入待加密的外部信号（明文），通过拨码开关随时变更来调整加密密钥，同时我们利用FPGA的强大算力对明文和密钥进行AES算法，得到加密后的密文。然后，将加密后的数据通过QSPI串行通信接口发送到ESP32，最后将ESP32读取的数据传输到AWS云端，实现外部信号的加密可视化。
数据加密的基本过程就是对原来为明文的文件或数据按某种算法进行处理，使其成为不可读的一段代码为“密文”，使其只能在输入相应的密钥之后才能显示出原容，通过这样的途径来达到保护数据不被非法人窃取、阅读的目的。加密过程的逆过程为解密，即将该编码信息转化为其原来数据的过程。我们希望应用所学的知识，利用SEA Board的FPGA和ESP32综合实现AES加密及解密过程。同时，该项目让我们加强了对信息加密算法的了解，同时增强了自己的实践能力。
![](https://github.com/KexinLi-design/Xlinx-SummerSchool-AWS_IoT-AES_Algorithm/blob/master/%E5%9F%BA%E4%BA%8ESEA%20Board%E7%9A%84AES%E5%8A%A0%E5%AF%86%E7%AE%97%E6%B3%95%E5%9C%A8AWS%E7%89%A9%E8%81%94%E7%BD%91%E4%B8%AD%E7%9A%84%E5%BA%94%E7%94%A8_%E5%8A%A0%E5%AF%86%E6%A8%A1%E5%9D%97%E7%A4%BA%E6%84%8F%E5%9B%BE.png)

<br />❈应用领域及适用范围
<br />    该项目涉及领域的应用前景十分广泛，AES算法的研究从理论到应用，己经深入到了信息安全技术的各个领域，深入研究与开发新的AES算法实现和应用具有重要的理论和实践意义。随着密码技术的高速发展，高级加密标准 AES(Rijndae1)算法将逐渐取代 DES在 IPSec、SSL和ATM 中的使用，并广泛应用于虚拟专用网、远程访问服务器(RAS)、SONET(同步光网络)、高速ATM／Ethernet路由器、卫星通信、移动通信、电子金融业务等领域。此外，网络保密系统 、财政保密、电子游戏保密等方面也将采用AES加密算法，将现有的关于AES研究成果与其他领域的相关技术与应用相结合，从应用的角度拓展数据加密技术，从而获得新的应用，是 AES算法(Rijndea1)的发展方向。
<br />    AES标准用来替代原先的DES（Data Encryption Standard），已经被多方分析且广为全世界所使用。经过五年的甄选流程，高级加密标准由美国国家标准与技术研究院 （NIST）于2001年11月26日发布于FIPS PUB 197，并在2002年5月26日成为有效的标准。2006年，高级加密标准已然成为对称密钥加密中最流行的算法之一。高级加密标准算法从很多方面解决了令人担忧的问题。
该设计适用于对文本信息、数字信号等进行加密，从电脑上输入一段信息，再人为设定一个秘钥，就会得到输出的加密信息；如果得知秘钥和加密后的信息，也可以对加密信息进行解密。
![加密模块示意图](https://github.com/KexinLi-design/Xlinx-SummerSchool-AWS_IoT-AES_Algorithm/blob/master/%E5%9F%BA%E4%BA%8ESEA%20Board%E7%9A%84AES%E5%8A%A0%E5%AF%86%E7%AE%97%E6%B3%95%E5%9C%A8AWS%E7%89%A9%E8%81%94%E7%BD%91%E4%B8%AD%E7%9A%84%E5%BA%94%E7%94%A8_IoT%E7%A4%BA%E6%84%8F%E5%9B%BE.png)

<br />❈设计主要功能及特色
<br />   本设计充分考虑和综合了FPGA和ESP32各自的优点，实现的主要功能和创新点如下，
<br />（1）利用FPGA强大算力实现外部信号的采集和加密、解密算法的计算，采用ESP32板载WiFi模块实现AWS IoT功能；
<br />（2）该设计不仅完成了基于FPGA的AES算法验证，而且将AES算法充分使用在物联网信息传输加密、解密过程中，很好地迎合了当下人们的需求；
<br />（3）在AWS平台上搭建通讯环境实现物联网，使得该项目与主流物联网平台紧密结合。
