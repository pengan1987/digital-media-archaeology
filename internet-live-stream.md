# 互联网和流媒体
在今天，当我们提到“互联网”这件事情，大多数时候都在讨论WWW，以至于许多时候人们会误认为WWW和HTML的出现是互联网的开始，甚至认为其是互联网上唯一的应用。但是，在互联网所依赖的TCP/IP协议上面‍‍，有许多不同的应用层协议，HTTP协议只是这些应用层协议之一。而即使是使用HTTP作为应用层协议的诸多情形中，也随着传输数据的不同而表现出不同的应用形态。

## 强大的现代Web标准
现代Web标准包括两个最基本的组件，HTML和Javascript，它们经历过若干次的扩充，特别是2008年的HTML5和2015年的ECMAScript 2015（ES6）出现之后，这些标准变得非常强大而且复杂。网页里的电脑博物馆[^1]中的许多功能都使用现代Web技术实现，它采用了HTML5、现代JavaScript标准以及WebAssembly。“博物馆”中大多数老电脑的模拟器都使用WebAssembly运行，WebAssembly技术出现的很晚，2017年才开始被主流浏览器支持，它可以把软件编译成接近于CPU机器代码的字节码（bytecode），速度要比基于文本的普通JavaScript代码更快一些。

此外网页里的电脑博物馆还使用了2011年出现的WebSocket技术提供实时通信，“千禧年的中文Linux”线上展的远程桌面就是运用使用了WebSocket的noVNC[^2]来实现的。另一个在网页里的电脑博物馆中用到的现代Web技术是WebGL，它同样出现在2011年，在“3D之舞：90年代的VRML”中，通过X_ITE库[^3]将VRML创建的3D内容转换为现代浏览器支持的WebGL，并嵌入到HTML5网页中进行展示的。

网页里的电脑博物馆充分受益于当代Web技术，但是前面提到的软件功能却并非只有通过当代的Web技术才能实现。实际上，无论是浏览器中的远程桌面、还是浏览器中的三维图形，早在现代Web技术出现之前的90年代或者是2000年代都已经被实现了，但其原始的解决方案却被现代浏览器所抛弃，使之只能在专门搭建的“博物馆”网站中观看，‍‍这也是网页里的电脑博物馆所希望为观众展现的一个戏剧化的冲突及问题。

## 浏览器插件
在现代Web标准出现之前，在浏览器中提供丰富的Web内容通常都离不开浏览器插件。在上节课里，我们会看到一些移动设备上的作品利用了Flash或者VRML等90、2000年代典型的Web技术。而这些在移动设备上使用Web技术的创作，正是受到90年代繁荣的Net Art的影响。

浏览器插件从开发技术和运行环境上来讲主要有两个大的‍‍类别：其中一类是NPAPI插件，主要被Netscape网景浏览器及衍生自网景的开源浏览器Mozilla和Firefox支持；‍另外一类就是ActiveX，主要被微软的Internet Explorer及各类IE“套壳”的浏览器，如MyIE、傲游（Maxthon，最初为衍生自MyIE的MyIE2）支持。ActiveX能够提供的功能和NPAPI大致相同，但许多网络银行的U盾只能在Internet Explorer使用，这是因为它们配套的驱动程序只能使用ActiveX插件来访问。

2000年代常见的上网环境通常会配置包括VRML、Java Applet、QuickTime、Flash、Shockwave（Director）、Silverlight在内一系列不同格式网络媒体的支持插件。在HTML5普及‍‍之前，它们对于通过Web展示多媒体内容是必不可少的存在。

从1999年起，英特尔曾经搭配使用Pentium III处理器的电脑发售Intel Web Outfitter Tool Kit光盘，中文叫做“爱网族工具包”。这张光盘里面的主要内容就是各类浏览器插件，其中就包括了常见的Real Player、Flash Player、Shockwave等浏览器插件，也包括了支持三维图形的Superscape Viscape SVR插件，展示全景图的IPIX Player插件，以及RealSlideshow幻灯片插件等等。

这些浏览器插件种类众多，但它们提供的功能大概可以分为三类：其一是交互图形，比如Flash；其二是能够在网络上传输的流式音视频，典型的有Real Player、Windows Media Player和Quicktime等；再就是提供Web上的三维图形功能，比如VRML观看插件Cosmo Player和Cortona等。

如果你希望调查一些典型的浏览器插件及其内容，强烈建议以BlueMaxima's Flashpoint[^4]作为研究的起点。它是目前成果最丰富的网页游戏保存计划，保存了30余种为不同浏览器插件平台创作的内容。

## 交互图形：Macromedia Flash和Shockwave
Flash是国内社群最熟悉的网络插件，它有两个主要的用途：一个是用来做游戏，另外一个就是用来做动画。值得一提的是Flash动画在中国和韩国的流行程度远高过西方发达国家，我猜测一个原因是和制作动态影像所需器材的价格有关：2000年代制作网络视频所需的摄像机、采集卡等硬件对于爱好者来说是一个不小的负担，而Flash则是不需要额外硬件投入，使用普通电脑就可以操作的动态影像制作工具。在家用摄像机更加普及的西方国家，Flash更多用来做游戏、网页横幅、登陆页（Landing page）等较强交互和视觉表现需求的Web内容。

Shockwave一般是用Marcomedia Director制作的，它比Flash的交互功能更加强大，支持原生3D等高级图形功能，并且支持Xtras。Xtras是一种编译过的Shockwave的插件，里面可以使用原生的二进制代码，用来支持额外的音视频文件格式或提供开发者定制的功能。但Shockwave文件也因此比Flash体积更大，流量和资源消耗也更多，因此Flash在网络交互内容上占据了主导地位，而Shockwave更多时候用来制作光盘软件的多媒体内容。

以Flash和Shockwave为平台，艺术家们制作了许多网络艺术作品，如奥地利艺术家LIA[^5]创作的RE-MOVE[^6]；德国艺术家Esther Hunziker使用Flash制作的UN_FOCUS[^7]；美国艺术家Nathaniel Stern使用Flash制作交互部分，同时包含了Quicktime视频片段的Hektor网站[^8]。

可能熟悉Flash的读者会好奇为什么Hektor会使用QuickTime提供视频内容，毕竟Flash及其FLV视频格式曾经是网络上主流的流媒体视频格式之一，特别是H.264出现之前，以Youtube为代表的网络视频网站都是使用Flash及FLV格式提供网络视频的。这是因为Hektor完成于2000年，此时的Flash还几乎不支持视频播放，直到2002年的Flash Player 6才开始支持在SWF文件中内置视频，而2003年的Flash Player 7才开始支持FLV视频格式。

## 数字格式可用性的挑战
虽然上面提到的作品都保存完好，但对今天的观众来说却很难完整访问。新款的浏览器几乎都不能正常打开上面的网站。为浏览器插件制作的内容会受到多方面的限制：

- 浏览器版本变化导致插件不可用，如Chrome 42（2015年）开始禁用NPAPI插件
- 浏览器插件文件格式本身的版本变化让内容不可用，如新版Windows Media Player就无法打开许多NetShow内容，QuickTime 7.3.1（2007年）不再支持mov文件内嵌的Flash轨道等等。
- 网络传输协议的变化（如SSL加密）让旧版插件无法正常传输内容，许多旧版浏览器插件不支持2008年出现的TLS 1.2加密

因此网络艺术远比我们认为的脆弱，对于相关的研究者和收藏家们来说，数字保存是摆在他们面前第一道门槛。他们不仅要保存文件本身，也要维持整个技术栈是可用的。如果仅仅保存文件本身却没有可以打开它的软件和硬件，便无法忠实、完整的观看当时的作品，这种保存也就是没有意义的。

今年五月，《Input》以“佳士得的沃霍尔NFT基本上是个赝品”[^9]为题发文，援引沃霍尔数据恢复项目（Warhol Data Recovery Project）参与者，卡内基梅隆大学Golan Levin教授在推特上的批评，指出佳士得所拍卖的是“近似的二次复制品”（2nd-generation near-copies）。佳士得的拍卖版本将原图由320x200像素不忠实的放大到了6000x4500像素，因此只能算作一种展览副本（exhibition copy）。

在Golan Levin教授的推特中，展示了一个有所妥协，但相对忠诚的展览实例：在卡内基梅隆大学创意咨询（Creative Inquiry）工作室30周年纪念展览上，他们与安迪沃霍尔美术馆合作，使用了现代PC和PNG图片作为视频源，通过模拟式混合视频线（即AV线），输出到一台1985年生产的原装Amiga电脑显示器上。让观众以尽可能接近原始的状态观看到安迪沃霍尔当年在Amiga电脑上完成的数字绘画作品。数字保存的挑战可能让我们很难、甚至永远无法将某件作品恢复到其原始的状态，但我们应当清醒并严谨地选择我们应当做哪些妥协。

## 流式影音：RealPlayer和Quicktime
HTML5相比之前的HTML标准最明显的变化就是加入了video和audio标签，支持HTML5的浏览器可以不依赖第三方插件播放网页里的视频和音频内容。但是直到2009年，Firefox和Chrome才加入这项标签的支持，而微软的Internet Explorer是要到2011年的IE9才加入这项功能。因此，整个2000年代所有在网络上提供的视频内容几乎都要通过浏览器插件来播放。除了上面提到的Flash和FLV，苹果的Quicktime和Real Networks的Real Player（2000年到2004年曾改名RealOne Player）则是最常用到的流媒体播放插件。

RealPlayer的第一个版本发布于1995年，最初的版本只支持音频播放，叫做RealAudio Player，它是第一款可以在拨号网络的低带宽（比如28.8Kbps）提供音频串流的媒体播放器。在1996年建站的音乐教育网站CafeMuse[^10]上，我们还可以找到一些早期的网上音频资源，这些音频以16Kbps的低码率提供了可以接受的音乐质量。而加利福尼亚大学尔湾分校（University of California, Irvine）的曾振锻（Dan Tsang）则保存了他在KUCI 88.9广播电台主持的左翼时评节目Subversity在1998年~2003年间播出的RealAudio格式录音[^11]，所有的音频文件同样是以16Kbps保存，可以在拨号上网的低带宽条件下收听。

QuickTime是另外一个常见的在网上提供音视频内容的插件。相比之下，以QuickTime格式提供的音、视频串流的网站没有使用Real Player的多，但Quicktime却提供了一些RealPlayer不具备的特性。其中最重要的就是QuickTime VR（QTVR），在90年代到2000年代初，QTVR是提供线上虚拟现实展览最常见的手段，如汉斯·鲁道夫·吉格尔（HR Giger）博物馆在2001年的QuickTime VR虚拟展览[^12]，除了受限于90年代的网络带宽而通常图像的分辨率较低之外，其通过QTVR实现的功能与前两年热门的“360°全景看房”几乎完全一致。

与现在的许多VR展览类似，QuickTime VR也是可以实现热点导航的，通过鼠标点击画面里的热点，可以在不同场景见跳转。惠灵耶稣会大学NASA未来教室（Wheeling Jesuit University/NASA Classroom of the Future）[^13]的QTVR月球基地场景就使用了热点导航功能。

QuickTime VR既可以用来展示场景，也可以用来制作3D环物展示，‍‍QTVR展示的物体并不是真的是三维建模，‍‍使用转台拍摄的一组照片，再通过软件相应鼠标交互，模拟视角的切换。直到今天，许多网站上的360°商品展示仍然在使用类似的方式制作，同时我们也仍然能够买到用于拍摄3D环物的转台。加拿大历史博物馆制作于2001年的埃及探秘（Mysteries of Egypt）[^14]VR展览使用了QuickTime VR的3D环物展示功能。

与Flash和Shockwave类似，艺术家们也曾经用QuickTime和RealPlayer的流式影音功能制作过一系列网络艺术作品。Cory Arcangel在2003年的《数据日记》（Data Diaries）中使用了QuickTime视频和闪烁的方格作为主要的呈现手段。

1995年，一群艺术家创建了KUNSTRADIO ON LINE网站[^15]，用来在线发布奥地利国家广播电台 (ORF) 的文化频道 Oesterreich 1的广播艺术（Radio Art）节目KUNSTRADIO的存档。在这个网站中，使用了Real Audio音频格式和RTSP协议在网络上传送音频节目。

美国艺术家Caroling Geary则在她的网站[^16]上发布了大量使用QuickTime VR制作的作品，许多使用类似技术制作的QuickTime VR全景图作品则被全景图像网站World Wide Panorama收藏和展示。

## 网络上的三维图形：VRML和X3D
在网络上传输三维内容的实践也出现在90年代，第一个在网上广泛应用的三维内容标准是VRML，它的起源可以追溯到W3C的早期参与者戴夫·拉格特（Dave Raggett）在1994年发布的论文《扩展WWW以支持独立于平台的虚拟现实》（Platform Independent Virtual Reality）[^18]。该论文中将VRML作为“VR markup language”（虚拟现实标记语言）的缩写，而在1995年VRML正式被标准化时，则改名为“Virtual Reality Modeling Language”（虚拟现实建模语言）。

VRML的功能相当丰富，可以支持三维模型、场景、动画等功能，也支持超链接在不同场景间跳转，还支持用户与场景的交互，并因此在90年代广泛用于搭建各类三维社交网络平台。如Cybertown、SAPARi等。在2001年，维护VRML标准的Web3D联盟（Web3D Consortium）[^19]推出了基于XML的新格式X3D，直到现在，X3D标准仍在在开发和维护中，其在Web标准中的地位类似于用于二维图形的SVG格式。

由于VRML和X3D长期依赖都依靠浏览器插件观看，没有得到主要浏览器维护者微软、苹果、谷歌的广泛支持，因此其应用范围逐渐偏离了在网络上传输三维图形的初衷，而成为科研和工程领域跨平台的三维图形标准。许多三维图形软件，都支持X3D和VRML格式的导入和导出。

在90年代末、2000年代初的新媒体艺术界也有着VRML的一席之地，1999年的欧洲媒体艺术节（European Media Art Festivals - EMAF）就在VRML-ART专题[^20]中展示了一系列使用VRML制作的作品

## 私有3D格式
VRML是一个开放的格式，虽然它本身的功能已经比较丰富，但其标准的演进却受制于Web3D联盟中各个厂家的制衡。因此许多开发商开发了它们自己的私有3D格式，如Cryo Interactive的SCOL（Standard Cryo Online Language）、Superscape Viscape和Adobe Atmosphere Player，但这些格式都没有像VRML那样广泛流行过。如果希望研究相关的内容，BlueMaxima's Flashpoint是一个非常好的起点。

## WWW之外的世界
在互联网上，还有几个WWW之外的重要的协议，如果说WWW是互联网的“表世界”，这些协议就算得上是互联网的“里世界”了。

其中一个协议是Gopher，是1993年由明尼苏达大学开发的以目录形式组织和查询信息的网络协议。是90年代万维网最重要的竞争者，主流的网页浏览器如Internet Explorer，Netscape等对Gopher网站的支持都延续到2000年代初。

另外一个非常重要的网络协议则是Telnet，是一种以仿真终端的形式访问远程软件系统的方式。在中文世界影响最大的Telnet网站要数台湾地区的PTT，而大陆也有一些曾有过广泛影响的Telnet BBS，如水木清华、北大未名、白云黄鹤（华中科技大学）、南大小百合、日月光华（复旦大学）等等，这类BBS通常是由大学运营并维护的。同时，北大侠客行等MUD游戏也是使用Telnet方式访问的。

另外值得一提的网络协议是Usenet，即新闻组。在Internet上运行的新闻组通过NNTP协议进行访问。目前国内已知的还在运行的Usenet新闻组就只有新帆新闻组[^21]一家了，而Google Groups也保存了诸多早期的Usenet信息，包括最早使用中文张贴内容的alt.chinese.text，是了解早期中文网民社群的重要资料来源之一。

## 参考资料
[^1]: 网页里的电脑博物馆： http://www.compumuseum.com
[^2]: noVNC官网：https://novnc.com/info.html
[^3]: Github上的X_ITE库：https://github.com/create3000/x_ite/wiki
[^4]: BlueMaxima's Flashpoint：https://bluemaxima.org/flashpoint/platforms/
[^5]: LIA的个人主页：https://www.liaworks.com/about/
[^6]: re-move by Lia：https://re-move.org/
[^7]: Un_Focus：https://estherhunziker.net/unfocus/
[^8]: Hektor网站： https://nathanielstern.com/artwork/hektor-net/
[^9]: Christie's Warhol NFT is basically a fake：https://www.inputmag.com/culture/what-exactly-is-christies-selling-in-its-warhol-amiga-nft-auction
[^10]: CafeMuse https://www.cafemuse.com/
[^11]: Subversity Archive on RealAudio 1998-2003：https://kuci.org/~dtsang/subversity/realaudio.htm
[^12]: Discover the MUSEUM HR GIGER with our QuickTime VR Tour：https://hrgiger.com/quicktime.html
[^13]: Lunar Base QuickTime VR：http://www.cotf.edu/BioBLAST/bioproject/qtvr/qtvrintro.htm
[^14]: Mysteries of Egypt - VR Gallery：https://www.historymuseum.ca/cmc/exhibitions/civil/egypt/egqtvr1e.html
[^15]: KUNSTRADIO：http://kunstradio.at/
[^16]: wholeO Onward Wholeo 2024 by Caroling and O Mlulu：https://wholeo.net/
[^17]: World Wide Panorama：https://www.worldwidepanorama.org/
[^18]: Platform Independent Virtual Reality：https://www.w3.org/People/Raggett/vrml/vrml.html
[^19]: Web3D联盟网站： https://www.web3d.org/
[^20]: VRML-ART： http://2016.emaf.de/emaf.de/_emaf/www.emaf.de/1999/german/vrml-art.html
[^21]: 新帆新闻组： news://news.newsfan.net
