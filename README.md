# 物聯網
物聯網是新一代訊息技術的重要組成部分，其英文名稱是：“The Internet of things”。顧名思義，物聯網就是萬物相連的互聯網。這有兩層意思：其一，物聯網的核心和基礎仍然是互聯網，是在互聯網基礎上的延伸和擴展的網路；其二，其用戶端延伸和擴展到了任何物品與物品之間，進行訊息交換和通訊也就是萬物相息。物聯網就是“萬物相連的互聯網”。

## 物聯網協定

Protocol |	CoAP  |	XMPP |	RESTful HTTP |	MQTT
---------|---------|---------|---------|---------
Transport |	UDP |	TCP |	TCP |	TCP
Messaging |	Request/Response |	Publish/Subscribe Request/Response |	Request/Response |	Publish/Subscribe Request/Response
2G, 3G, 4G Suitability (1000s nodes) | Excellent |	Excellent |	Excellent |	Excellent
LLN Suitability (1000s nodes) | Excellent |	Fair |	Fair |	Fair
Compute Resources | 10Ks RAM/Flash | 10Ks RAM/Flash | 10Ks RAM/Flash | 10Ks RAM/Flash
Success Storied	| Utility Field Area Networks |		Remote management of consumer white goods |	Smart Energy Profile 2 (premise energy management/home services) |	Extending enterprise messaging into IoT applications

### XMPP
XMPP是一種基於標准通用標記語言的子集XML的協議，它繼承了在XML環境中靈活的發展性。因此，基於XMPP的應用具有超強的可擴展性。經過擴展以後的XMPP可以通過發送擴展的信息來處理用戶的需求，以及在XMPP的頂端建立如內容髮布系統和基於地址的服務等應用程序。而且，XMPP包含了針對服務器端的軟件協議，使之能與另一個進行通話，這使得開發者更容易建立客戶應用程序或給一個配好系統添加功能。

### MQTT

![mqtt](./images/MQTT.png)

MQTT（Message Queuing Telemetry Transport，消息隊列遙測傳輸）是IBM開發的一個即時通訊協議，有可能成為物聯網的重要組成部分。該協議支持所有平台，幾乎可以把所有聯網物品和外部連接起來，被用來當做傳感器和致動器（比如通過Twitter讓房屋聯網）的通信協議。

[MQTT相關庫](./protocol/MQTT.lib.md)
[MQTT相關庫介绍](./protocol/MQTT.lib.md)

###CoAP

![coap](./images/coap.jpg)

CoAP是受限制的應用協議(Constrained Application Protocol)的代名詞。在最近幾年的時間中，專家們預測會有更多的設備相互連接，而這些設備的數量將遠超人類的數量。在這種大背景下，物聯網和M2M技術應運而生。雖然對人而言，連接入互聯網顯得方便容易，但是對於那些微型設備而言接入互聯網非常困難。在當前由PC機組成的世界，信息交換是通過TCP和應用層協議HTTP實現的。但是對於小型設備而言，實現TCP和HTTP協議顯然是一個過分的要求。為了讓小設備可以接入互聯網，CoAP協議被設計出來。 CoAP是一種應用層協議，它運行於UDP協議之上而不是像HTTP那樣運行於TCP之上。 CoAP協議非常的小巧，最小的數據包僅為4字節。

###RESTful HTTP

REST 指的是一組架構約束條件和原則。滿足這些約束條件和原則的應用程序或設計就是RESTful。

Web 應用程序最重要的REST 原則是，客戶端和服務器之間的交互在請求之間是無狀態的。從客戶端到服務器的每個請求都必須包含理解請求所必需的信息。如果服務器在請求之間的任何時間點重啟，客戶端不會得到通知。此外，無狀態請求可以由任何可用服務器回答，這十分適合雲計算之類的環境。客戶端可以緩存數據以改進性能。


###Thread

![thread](./images/thread.jpg)

Thread是一種基於簡化版IPv6的網狀網絡協議，該協議由行業領先的多家技術公司聯合開發，旨在實現家庭中各種產品間的互聯，以及與互聯網和雲的連接。 Thread易於安裝、高度安全，並且可擴展到數百台設備。 Thread基於低成本、低功耗的802.15.4芯片組開發。目前正在使用的大量產品，只需一次簡單的軟件升級，便可支持Thread。

##相關Web技術

##Z-Wave

> Z-Wave是一種新興的的基於射頻的、低成本、低功耗、高可靠、適於網絡的短距離無線通信技術。工作頻率为908.42MHz(美國)~868.42MHz(歐洲)，採用FSK(BFSK/GFSK)調製方式，數據傳輸速率為9.6 kbps，信號的有效覆蓋範圍在室內是30m，室外可超過100m，適合於窄帶寬應用場合。隨著通信距離的增大，設備的複雜度、功耗以及系統成本都在增加，相對於現有的各種無線通信技術，Z-Wave技術將是最低功耗和最低成本的技術，有力地推動著低速率無線個人區域網。
##Zigbee

> ZigBee是基於IEEE802.15.4標準的低功耗局域網協定。根據國際標準規定，ZigBee技術是一種短距離、低功耗的無線通信技術。這一名稱（又稱紫蜂協議）來源於蜜蜂的八字舞，由於蜜蜂(bee)是靠飛翔和“嗡嗡”(zig)地抖動翅膀的“舞蹈”來與同伴傳遞花粉所在方位信息，也就是說蜜蜂依靠這樣的方式構成了群體中的通信網路。其特點是近距離、低複雜度、自組織、低功耗、低數據速率。主要適合用於自動控制和遠程控制領域，可以嵌入各種設備。簡而言之，ZigBee就是一種便宜的，低功耗的近距離無線組網通訊技術。
###Websocket

> WebSocket protocol 是HTML5一種新的協定。它是實現了瀏覽器與服務器全雙工通信(full-duplex)。

###SOAP

> 簡單對象訪問協定是交換數據的一種協定規範，是一種輕量的、簡單的、基於XML（標準通用標記語言下的一個子集）的協定，它被設計成在WEB上交換結構化的和固化的信息。

###6LoWPAN

> IETF 6LoWPAN取得的突破是得到一種非常緊湊、高效的IP實現，消除了以前造成各種專門標準和專有協定的因素。這在工業協定（BACNet、LonWorks、通用工業協調監控與數據採集）領域具有特別的價值。這些協定最初開發是為了提​​供特殊的行業特有的匯流排和連結(從控制器區域網匯流排到AC電源線)上的互操作性。
###UDP

> UDP協定的全稱是用戶數據報協定，在網路中它與TCP協定一樣用於處理數據包，是一種無連接的協定。在OSI模型中，在第四層——傳輸層，處於IP協定的上一層。 UDP有不提供數據包分組、組裝和不能對數據包進行排序的缺點，也就是說，當信息發送之後，是無法得知其是否安全完整到達的。 UDP用來支持那些需要在計算機之間傳輸數據的網路應用。包括網路影片會議系統在內的眾多的客戶/服務器模式的網路應用都需要使用UDP協定。 UDP協定從問世至今已經被使用了很多年，雖然其最初的光彩已經被一些類似協定所掩蓋，但是即使是在今天UDP仍然不失為一項非常實用和可行的網路傳輸層協定。
###uIP

> uIP 由瑞典計算機科學學院（網路嵌入式系統小組）的Adam Dunkels開發。其原始碼由Ç語言編寫，並完全公開。

> uIP 協定堆疊去掉了完整的TCP/IP 中不常用的功能，簡化了通訊流程，但保留了網路通信必須使用的協定，設計重點放在了
IP/TCP/ICMP/UDP/ARP 這些網路層和傳輸層協定上，保證了其代碼的通用性和結構的穩定性。


###DTLS

> DTLS(Datagram Transport Layer Security)即數據包傳輸層安全性協定。 TLS不能用來保證UDP上傳輸的數據的安全，因此Datagram TLS試圖在現存的TLS協定架構上提出擴展，使之支持UDP，即成為TLS的一個支持數據包傳輸的版本。 DTLS 1.0基於TLS 1.1, DTLS 1.2基於TLS 1.2。
###NFC

> NFC近場通信技術是由非接觸式射頻識別（RFID）及互聯互通技術整合演變而來，在單晶片上結合感應式讀卡器、感應式卡片和點對點的功能，能在短距離內與兼容設備進行識別和數據交換。工作頻率為13.56MHz.但是使用這種手機支付方案的用戶必須更換特製的手機。目前這項技術在日韓被廣泛應用。手機用戶憑著配置了支付功能的手機就可以行遍全國：他們的手機可以用作機場登機驗證、大廈的門禁鑰匙、交通一卡通、信用卡、支付卡等等。
###WiFi

> Wi-Fi是一種可以將個人電腦、手持設備（如pad、手機）等終端以無線方式互相連接的技術，事實上它是一個高頻無線電信號。無線保真是一個無線網絡通信技術的品牌，由Wi-Fi聯盟所持有。目的是改善基於IEEE 802.11標準的無線網路產品之間的互通性。有人把使用IEEE 802.11系列協定的區域網就稱為無線傳真。甚至把無線傳真真等同於無線網際網路（Wi-Fi是WLAN的重要組成部分）。
###Eddystone

>  Google已經推出了一項名為Eddystone的開源低功耗藍牙（BluetoothLE）beacon平台，並且能夠在iOS、Android等系統上輕鬆使用。

主頁: [Beacons](https://developers.google.com/beacons/)

##物聯網相關平台

###Yeelink

主页: [http://www.yeelink.net/](http://www.yeelink.net/)

###SiteWhere

> The Open Platform for the Internet of Things ™

> 這個項目提供了一個完整的平台，來管理物聯網設備、收集數據並用外部系統進行數據整合。 SiteWhere發行版本可以下載或在亞馬遜雲端平台中使用。它還整合了多個大數據工具，包括MongoDB和ApacheHBase。

主頁: [http://www.sitewhere.org/](http://www.sitewhere.org/)


###DeviceHive

> 該項目提供一個支持連接設備到互聯網的機器對機器通訊框架。它包括支持創​​建網路易於使用基於web的管理軟件、應用安全規則和監控設備。該網站提供內置有DeviceHub的樣本項目，而且它也有一個"遊樂場"部分，允許用戶使用DeviceHub在線去看它是如何工作的。

主頁: [http://www.devicehive.com/](http://www.devicehive.com/)

###Devicehub.net

> Devicehub.net描述自己為“物聯網的開源支柱”。它是一個基於雲端的服務，存儲物聯網相關的數據，提供數據的可視化並允許用戶在網頁上控制物聯網設備。開發者使用該服務創建追蹤健康信息的應用程序，監視孩子的位置，自動化家電，追蹤車輛數據，監測天氣等等。
> 
主页: [http://devicehub.net/](http://devicehub.net/)

###IoT Toolkit

> 這個項目背後的組織正使用各種工具工作，來整合多個物聯網相關的傳感器網路和協定。雖然主要的項目時一個智能對象應用程序，但該組織也工作在一個HTTP對Coap的情景下，一個帶有嵌入式軟體代理的應用程序框架等等。在矽谷，他們也發起了一個“遇見”組織，針對物聯網開發有興趣的人。

主页: [http://iot-toolkit.com/](http://iot-toolkit.com/)

###Mango(芒果)

> “芒果”自稱是“世界上最流行的開源的機器對機器軟體”。基於網路對它支持多個平台。它的主要功能包括支持多協定和數據資料庫、元點、使用者自定義事件、導入/導出等等。

###Nimbits

> Nimbits可以存儲和處理特定的數據類型，數據可以是時間標記的或地理標記的。作為服務的公用平台是可用的，或者你也可以下載這個軟件並部署它到谷歌應用引擎、或亞馬遜EC2上的J2EE服務器上、或一個樹莓派上。它支持多種編程語言，包括Arduino、JavaScript、HTML或Nimbits.io Java庫。

###OpenRemote

> OpenRemote為基於家居的愛好者、集成商、分銷商和製造商提供了四種不同的集成工具。它支持十幾種不同的現有協定，允許用戶創建幾乎任何類型的智能設備（他們能夠想到和使用任何支援java的設備來控制它）。該平台是開源的，但在設計和產品開發過程中，該公司也出售各種支援、電子書等工具來進行幫助。

###ThingSpeak

> ThingSpeak可以處理HTTP請求，並存儲和處理數據。這個開放數據平台的主要功能包括開放應用程序、實時數據收集、地理位置數據、數據處理和可視化、設備狀態信息和插件。它可以集成多個硬體和軟體平台，包括Arduino、樹莓派、ioBridge/RealTime.io、Electic lmp、移動和網路應用、社會網絡和MATLAB數據分析。除了開源版本，還提供託管服務。

###NodeMCU

> 一款開源快速硬體原型平台，包括韌體和開發板，用幾行簡單的Lua腳本就能開發物聯網應用

##物聯網相關嵌入式操作系統

> 實時系統（Real-time operating system,RTOS）的正確性不僅依賴系統計算的邏輯結果，還依賴於產生這個結果的時間。實時系統能夠在指定或者確定的時間內完成系統功能和外部或內部、同步或異步時間做出響應的系統。因此實時系統應該在事先先定義的時間範圍內識別和處理離散事件的能力；系統能夠處理和儲存控制系統所需要的大量數據。

###Windows 10 IoT

> 主要面向工業設備、移動設備、小型設備，都支援通用驅動、通用應用

項目首頁: [https://dev.windows.com/en-us/iot](https://dev.windows.com/en-us/iot)

###Contiki

**相關支持**: ``CoAP``,``TCP/IP網絡支援``,``RPL路由``,``6Lowpan 報文壓縮``,``Rime無線協議棧``

> Contiki是一個適用於有內存的嵌入式系統的開源的、高可移植的、支持網路的多任務操作系統。包括一個多任務核心、TCP/IP 堆疊、程序集以及低工耗的無線通訊堆疊。 Contiki 採用C語言開發的非常小型的嵌入式操作系統，運行只需要幾K的內存。

Contiki 是一個小型的，開源的，極易移植的多任務電腦操作系統。它專門設計以適用於一系列的內存受限的網絡系統，包括從8位電腦到微型控制器的嵌入系統。它的名字來自於托爾·海爾達爾的康提基號。

Contiki只需幾kilobyte的代碼和幾百字節的內存就能提供多任務環境和內建TCP/IP支援。

###LwIP

> LwIP是Light Weight (轻型)IP协议，有无操作系统的支持都可以运行。LwIP实现的重点是在保持TCP协议主要功能的基础上减少对RAM 的占用，它只需十几KB的RAM和40K左右的ROM就可以运行，这使LwIP协议栈适合在低端的嵌入式系统中使用。

> lwIP协议栈主要关注的是怎么样减少内存的使用和代码的大小，这样就可以让lwIP适用于资源有限的小型平台例如嵌入式系统。为了简化处理过程和内存要求，lwIP对API进行了裁减，可以不需要复制一些数据。

###FREERTOS

> FreeRTOS是一个迷你操作系统内核的小型嵌入式系统。作为一个轻量级的操作系统，功能包括：任务管理、时间管理、信号量、消息队列、内存管理、记录功能等，可基本满足较小系统的需要。

> 由于RTOS需占用一定的系统资源(尤其是RAM资源)，只有μC/OS-II、embOS、salvo、FreeRTOS等少数实时操作系统能在小RAM单片机上运行。相对μC/OS-II、embOS等商业操作系统，FreeRTOS操作系统是完全免费的操作系统，具有源码公开、可移植、可裁减、调度策略灵活的特点，可以方便地移植到各种单片机上运行，其最新版本为8.0.0版。

###mbed OS

![mbed OS](./images/mbedos.png)

**相关支持**: ``BLE``,``Celluar``,``WIFI``,``Zigbee``,``6LoWPAN``

> 一款基于ARM Cortex-M处理器的设备所设计的免费操作系统，配有安全、通讯和设备管理模块，支持低功率智能蓝牙标准、2G、3G与CDMA通信技术、Thread、Wi-Fi、802.15.4/6LoWPAN、TLS/DTLS、CoAP、HTTP、MQTT以及轻量级的M2M。而只需32-64kbRAM和256 kb闪存的配置，适合在小设备上运行。

> mbed™ OS is an operating system for IoT devices and is especially well-suited to run in energy constrained environments. The OS includes the connectivity, security and device management functionalities required in every IoT device.

 - Connectivity protocol stack support for Bluetooth® low energy, Cellular, Ethernet, Thread, Wi-fi®,  Zigbee IP, Zigbee NAN, 6LoWPAN
 - Automation of power management
 - Software asset protection and secure firmware updates for device security & management
 - Supports a wide range of ARM Cortex-M based hardware platforms from major MCU vendors
 - Support for OMA Lightweight M2M protocol for device management
 - Updatable and secure devices at the edge capable of additional processing and functionality
 - Banking-class end-to-end IP security across the communication channels through TLS & DTLS 
 - Future proof designs by supporting all the key open standards for connectivity and device management

###emOS

> embOS是一个优先级控制的多任务系统，是专门为各种微控制器应用于实时系统应用的嵌入式操作系统．是一个具有最小RAM和ROM占用的、高速的、多功能的高性能工具。

> 贯穿embOS的整个开发过程，微控制器有限的资源一直是开发者所顾忌的。五年来，该RTOS的内部结构已经被优化为不同客户的不同应用中，以满足工业需要。对不同微控制器的完全源码，使开发者很方便用实时操作系统构建实时程序。embOS是高度模块化的，只有需要的函数才被调用，占用的ROM非常小。 最小的内存占用：1kb ROM,30字节 RAM;由于提供源码文件，你可以用embOS灵活定制系统以满足实际需求。
任务之间可以通过旗语、邮箱和事件安全便利地通讯。

###Salvo

> Salvo™ is the first Real-Time Operating System (RTOS) designed expressly for very-low-cost embedded systems with severely limited program and data memory. With Salvo, you can quickly create low-cost, smart and sophisticated embedded products. Pumpkin™ has currently certified Salvo for use with:

- 8051 family and its derivatives
- ARM® ARM7TDMI® and Cortex™-M3
- Atmel® AVR® and MegaAVR™
- Epson S1C17 family
- Motorola M68HC11
- TI's MSP430 Ultra-Low Power Microcontroller
- Microchip PIC12|14000|16|17|18 PICmicro® MCUs
- Microchip PIC24 MCUs and dsPIC® DSCs
- Microchip PIC32™ MCUs
- TI's TMS320C2000 DSPs

###μC/OS-II

> uC/OS II(Micro Control Operation System Two) 是一个可以基于ROM运行的、可裁减的、抢占式、实时多任务内核，具有高度可移植性，特别适合于微处理器和控制器，是和很多商业操作系统性能相当的实时操作系统(RTOS)。

> 为了提供最好的移植性能，uC/OS II最大程度上使用ANSI C语言进行开发，并且已经移植到近40多种处理器体系上，涵盖了从8位到64位各种CPU(包括DSP)。 uC/OS II可以简单的视为一个多任务调度器，在这个任务调度器之上完善并添加了和多任务操作系统相关的系统服务，如信号量、邮箱等。其主要特点有公开源代码，代码结构清晰、明了，注释详尽，组织有条理，可移植性好，可裁剪，可固化。内核属于抢占式，最多可以管理60个任务。从1992年开始，由于高度可靠性、移植性和安全性，uC/OS II已经广泛使用在从照相机到航空电子产品的各种应用中。

###TinyOS

协议支持: ``CoAP``

[TinyCoAP](http://tinyos.stanford.edu/tinyos-wiki/index.php/CoAP_-13)

> TinyOS是UC Berkeley（加州大学伯克利分校）开发的开放源代码操作系统，专为嵌入式无线传感网络设计，操作系统基于构件（component-based）的架构使得快速的更新成为可能，而这又减小了受传感网络存储器限制的代码长度。

> TinyOS的构件包括网络协议、分布式服务器、传感器驱动及数据识别工具。其良好的电源管理源于事件驱动执行模型，该模型也允许时序安排具有灵活性。TinyOS已被应用于多个平台和感应板中。

####支持硬件

 - Atmel ATmega128, a 8-bit RISC microcontroller.
 - Texas Instruments MSP430 a 16-bit low power microcontroller.
 - Intel XScale PXA271 a 32-bit RISC microcontroller.

###MQX

> Freescale MQX™ RTOS a full-featured complimentary real-time operating system including the MQX™ Kernel, TCP/IP stack (RTCS), embedded MS-DOS file system (MFS), USB host/device stack, and more. The MQX™ multitasking kernel provides pre-emptive scheduling, fast interrupt response, extensive inter-process communication and synchronization facilities. MQX RTOS includes its own peripheral drivers.

###QNX

> QNX是由加拿大QSSL公司（QNX Software System Ltd.）开发的分布式实时操作系统。该操作系统既能运行于以Intel X86、Pentium等CPU为核心硬件环境下，也能运行于以PowerPC、MIPS等CPU为核心的硬件环境。QNX操作系统符合POSIX基本标准和实时标准，使其应用可以方便的进行移植。


###openWRT

> OpenWrt 可以被描述为一个嵌入式的 Linux 发行版，（主流路由器固件有 dd-wrt,tomato,openwrt三类）而不是试图建立一个单一的、静态的系统。OpenWrt的包管理提供了一个完全可写的文件系统，从应用程序供应商提供的选择和配置，并允许您自定义的设备，以适应任何应用程序。

> 对于开发人员，OpenWrt 是使用框架来构建应用程序，而无需建立一个完整的固件来支持；对于用户来说，这意味着其拥有完全定制的能力，可以用前所未有的方式使用该设备。

###RIOT
项目首页: [http://riot-os.org/](http://riot-os.org/)
平台: ``MSP430``, ``ARM7``, ``Cortex-M0``, ``Cortex-M3``,``Cortex-M4``,``x86``
> RIOT自称为“友好的物联网操作系统”。RIOT是FeuerWhere项目的分支，首次亮相在2013年。它的目的是既开发者友好又资源友好。它支持多种架构，包括MSP430、ARM7、Cortex-M0、Cortex-M3、Cortex-M4和标准的x86电脑。

 - Arduino Due
 - UDOO Board (Cortex-M3 part)
 - Nordic nrf51822 (DevKit)
 - mbed NXP LPC1768
 - TelosB
 - Zolertia Z1
 - Texas Instruments EZ430-Chronos
 - STM32F4DISCOVERY
 - STM32F3DISCOVERY
 - STM32F0DISCOVERY
 - WSN 430 (v1.3b and v1.4)
 - HiKoB FOX
 - ScatterWeb MSB-A2
 - ScatterWeb MSB-430H

##[Open Hybrid](http://www.openhybrid.org/index.html) 

> Open Hybrid是一个针对于物理计算与物联网的开源增强现实平台，它基于Web与Arduino。

##[Sora](https://github.com/Microsoft/Sora) 

> Sora是微软研究院的一个软件无线电项目。Sora项目旨在开发一个最先进的软件无线电系统，能够快捷而有效地实现当前最前沿的无线通信技术。

##[Eliot](https://github.com/c3d/eliot)
> Eilot是一个为物联网设计的轻量级扩展语言，被设计用于使配置简易化、控制一个传感器或者执行器的设备群。

#物联网相关库

##CoAP协议

###libcoap

语言: ``C``

主页: [http://sourceforge.net/projects/libcoap/](http://sourceforge.net/projects/libcoap/)

> Lightweight application-protocol for devices that are constrained their resources such as computing power, RF range, memory, bandwith, or network packet sizes. This protocol, CoAP, is developed in the IETF working group "CoRE", <http://6lowapp.net>.

###jCoAP

语言: ``Java``

主页: [https://code.google.com/p/jcoap/](https://code.google.com/p/jcoap/)

> jCoAP is a Java Library implementing the Constrained Application Protocol (CoAP)


###Node-CoAP

语言: ``Javascript`` (Nodejs)

主页: [https://github.com/mcollina/node-coap](https://github.com/mcollina/node-coap)

> node-coap is a client and server library for CoAP modelled after the http module.

###coap

语言: ``Python``

主页: [https://github.com/openwsn-berkeley/coap](https://github.com/openwsn-berkeley/coap)

> A CoAP Python library

> This package implements the Constrained Application Protocol (CoAP) developed by the IETF CORE working group.

###Californium (Cf) CoAP 

语言: ``Java``

主页: [https://github.com/mkovatsc/Californium](https://github.com/mkovatsc/Californium)

> Californium (Cf) is an open source implementation of the Constrained Application Protocol (CoAP). It is written in Java and targets unconstrained environments such as back-end service infrastructures (e.g., proxies, resource directories, or management services) and less constrained environments such as embedded devices running Linux (e.g., smart home controllers or vehicle sensors). Californium (Cf) has been running code for the IETF standardization of CoAP and was recently reimplemented to straighten changed design decisions, but also to improve its performance with focus on scalability. The new implementation was successfully tested at the ETSI CoAP#3 and OMA LWM2M Plugtests in November 2013.

##REST

###cJSON

语言: ``C``

主页: [http://sourceforge.net/projects/cjson/](http://sourceforge.net/projects/cjson/)

> JSON(JavaScriptObject Notation)是一种轻量级的数据交换格式。它基于JavaScript的一个子集。JSON采用完全独立于语言的文本格式，但是也使用了类似于C语言家族的习惯。这些特性使JSON成为理想的数据交换语言。易于人阅读和编写，同时也易于机器解析和生成。

##其他

###cURL

语言: ``C``

主页: [http://curl.haxx.se/](http://curl.haxx.se/)

> curl是利用URL语法在命令行方式下工作的开源文件传输工具。它被广泛应用在Unix、多种Linux发行版中，并且有DOS和Win32、Win64下的移植版本。

###HiveMQ

语言: ``Java``

主页: [http://www.hivemq.com/](http://www.hivemq.com/)

> HiveMQ 是一个企业级的 MQTT 代理，主要用于企业和新兴的机器到机器M2M通讯和内部传输，最大程度的满足可伸缩性、易管理和安全特性。提供免费的个人版。HiveMQ 提供了开源的插件开发包。


#物联网相关书籍

##中高级

书名 | 作者 | 日期 | 类型
------------ | ------------- | ------------ | ------------
 - | - | - |  -


##初级

书名 | 作者 | 日期 | 类型 
------------ | ------------- | ------------ | ------------
[Learning Internet of Things](https://www.packtpub.com/application-development/learning-internet-things) | Peter Waher | 2015.02 | Book & Ebook|
[一步步搭建物联网系统](http://designiot.phodal.com) | Phodal Fengda & Fortware | 2014.11 | 电子书 | -


##相关书籍

###WEB

书名 | 作者 |  日期  | 类型
------------ | ------------- | ------------ | ------------
 RESTful Web APIs | Leonard Richardson & Mike Amundsen |  2014.06 | -
 REST实战 | 韦伯 & 帕拉斯泰迪斯 | 2011.09. | -

###硬件

书名 | 作者 | 日期 | 类型 |
------------ | ------------- | ------------ | ------------
 Arduino从基础到实践 | Michael McRoberts | 2013.03 |  -
 Arduino Cookbook | Michael Margolis | 2011.04 | -
 Raspberry Pi用户指南 | Eben Upton | 2013.08  | -

## License

![cc](https://i.creativecommons.org/l/by-nc/4.0/88x31.png)

本作品采用[知识共享署名-非商业性使用 4.0 国际许可协议](http://creativecommons.org/licenses/by-nc/4.0/)进行许可。

© 2014 [Phodal Huang](http://www.phodal.com). 
