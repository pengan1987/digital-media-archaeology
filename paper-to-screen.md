# From Paper to Screen
Today marks the seventh session of our series: "From Paper to Screen." The primary objective of this class is to shed light on how video monitors have become the most crucial element in computer art. When visiting a new media art or digital art exhibition, our first impression often revolves around displays of various sizes. However, in the evolution of new media art and computer development, hard copies on paper have played a significant role. Particularly in computer-based visual creation, early artists using computers conducted many intriguing explorations through paper as a medium.

The familiar paradigm of using video monitors alongside keyboard-operated computers became the standard computer operation mode only around the mid-to-late 1970s. The starting point of this mode of operation is what I am about to discuss next: the Video Terminal. Before the changes in computer operation introduced by the Video Terminal, most people interacted with computers using teletypewriters, although I couldn't find a real teletypewriter. However, many devices and protocols inherited their principles of operation from teletypewriters. By understanding the workings of these devices, we can roughly infer the operational principles of teletypewriters.

## Bitmaps
Before we dive in, let's consider how computers handle graphics. We've noticed that most images generated or processed by computers are bitmaps. Today, bitmaps are the most common graphics on computers, such as the digital photos edited in Photoshop or digital paintings, which are typically bitmaps.

However, for older computers, bitmaps posed a significant issue—they required large amounts of memory. For quite some time, manipulating bitmaps on a computer was a luxurious function. Generally, the memory space occupied by a bitmap is the horizontal resolution multiplied by the vertical resolution, further multiplied by the color depth. For a 24-bit true-color image, each pixel occupies three bytes.

The screen resolution I'm using now is 1366x768, which is already quite an outdated specification. If my display is set to 24-bit true color, the memory consumed by a single screen is 1366x768x24 = 25,178,112 bits, roughly 24 Mbits, where each byte consists of 8 bits, approximately 3 MBytes—the minimum memory required to support this display specification.

Even until the mid-90s, mainstream graphics cards often had only 4 MBytes of memory, while those with 3D acceleration might have had 8 MBytes. Thus, handling full-screen true-color bitmaps on computers from the 80s to the early 90s was quite challenging. The "Web Style Guide, 2nd Edition" elaborates extensively on the display principles of color bitmaps [^1]. In the 90s, sacrificing color depth for higher resolution in commercial applications was common practice. The 16-bit "high-color" setting was prevalent, capable of displaying 65,536 colors, requiring only 2 bytes per pixel—about one-third less memory than 24-bit true color. On older devices, 8-bit or one-byte color storage allowed only 256 colors. An extreme case was the old Macintosh, which, in pursuit of higher display resolutions, entirely abandoned color, opting for monochrome displays. These models were produced until the 90s (the last one being the Macintosh Classic II).

When the original Macintosh was released, one of its most notable software was MacPaint, showcasing the bitmap capabilities of Macintosh. One of the most famous images was a digitized version of the artwork "Woman Combing Her Hair" by Japanese printmaker Hashiguchi Goyo. Although its resolution by today's standards wasn't high, it still vividly depicted the texture of clothing patterns and hair strands. In 1984, when most home computers could only display "scrolls and sprites," the Macintosh, capable of full-screen bitmap editing, was highly advanced. Apple designer Susan Kare explained the process of creating this image in an interview in 2000 [^2].

The old Macintosh with a monochrome screen had a resolution of 512x342 pixels, displaying only black and white colors. Therefore, each pixel occupied just one bit, totaling around 21.375 KBytes of memory. Despite this seemingly small capacity, the original Macintosh had only 128 KB of memory, without separate graphics memory. Consequently, nearly 1/6th of the memory was utilized for display purposes, leaving slightly more than 100 KB of memory available for applications and the operating system.

The first Macintosh was released in 1984. During that period, computer systems offering desktop publishing, CAD, and similar applications often opted for monochrome displays in exchange for higher resolution. On the PC platform, the Hercules Graphics Card (HGC), released in 1982, supported 720x348 monochrome images. Its higher graphics resolution made the HGC card the most commonly used model for PC software Chinese character systems in the 1980s.

For even older hardware, processing monochrome bitmaps was quite resource-intensive. They often used logic that could only display fixed letters, like the MDA monochrome graphics card that came standard with the IBM PC. As for home computers resembling gaming consoles, they usually compromised on display resolution to present color, and their display chips often restricted the number of colors within specific display blocks (blocks).

## Host and Terminal

Up until now, the situations we've mentioned have been limited to personal computers. However, another significant way people used computers at that time was by operating more powerful computer hosts through terminals. The combination of hosts and terminals, be it mainframes, minicomputers, or microcomputers, was widely used.

Large computers of that era often comprised several large cabinets, with one for the CPU, another for tape drives, and yet another for the hard disk. Sometimes even the CPU and memory were housed in separate cabinets. Computer users typically couldn't directly access the computer host, nor could they exclusively claim computer resources. Instead, they needed to share these resources among many users. The emergence of time-sharing systems allowed multiple users to simultaneously operate the same computer. Each user had a dedicated set of input-output devices, while the CPU and memory resources were shared. The device serving as the input-output interface for individual users, such as a teleprinter or the later-mentioned video display terminal, was at the extremity of the entire computer system and was hence referred to as the terminal.

In our third class on "Telecommunication Networks," we demonstrated the basic usage of terminals. The terminals we showcased were of relatively newer models, capable of displaying Chinese characters. However, they only supported the older GB2312 and GBK Chinese encodings and couldn't support UTF-8. The terminal I showcased today was connected via Ethernet to my laptop acting as a host. However, in most cases, terminals were connected through serial cables or dial-up Modem.

The two terminals displayed in our classroom were both connected to the same laptop. They were logged in as users set up in the Linux system. This situation closely resembled the working mode of large hosts, where two users independently operated two terminals, executing programs on the host simultaneously without being aware of each other's presence. This operating experience is quite reminiscent of the multiplayer online games or social networks on the internet today. In fact, the host/terminal model was the basis for the gradual emergence of the client-server (C/S model, typical in client-based online games) and the browser-server model (B/S model, typical in web-based multiplayer games) after the popularity of PCs and the internet[^3].

## Vector Graphics Terminals
Previously, we discussed how displaying bitmaps on computers demanded significant resources, making devices capable of displaying bitmaps quite expensive. For applications following the host/terminal architecture, bitmaps required higher bandwidth for transmission and were impractical on slower networks. Hence, a commonly used image display device during the era of large hosts was the vector graphics terminal.

Vector graphics terminals were the most commonly used electronic display devices for early computer graphics. An electron gun smoothly drew lines between specific points on the screen, requiring a smaller data transmission volume. It didn't need to transmit every pixel but only the starting and ending points of the path to display the graphics on the screen.

In the 1970s, common vector graphics terminals included the Imlac PDS-1 and Tektronix 4010 series. While their refresh rates were relatively low, they had higher resolutions; for instance, the Imlac PDS-1 had 1024x1024 locatable positions. Unlike television sets with fixed scan lines, their cathode ray tubes allowed the electron beam to scan only the required parts for drawing. Consequently, when displaying lines and charts, the common aliasing seen on low-resolution raster displays was almost non-existent.

The Tektronix 4010 utilized long-persistence phosphors to reduce costs, employing a storage tube. Once the electron gun traced the lines of a graphic on the screen, it no longer required repeated scanning to maintain the illumination, unlike standard CRTs. However, this type of tube could only perform full-screen erasures and redraws.

On the other hand, the Imlac PDS-1 used short-persistence phosphors like those found in standard television sets. Once the electron gun passed over a position, it quickly darkened, necessitating repeated scanning to maintain the screen's content. This required the terminal to incorporate a certain amount of memory to store screen content, increasing production costs. Nonetheless, it had a higher refresh rate and could execute games with animation effects that storage tubes couldn't support. The origin of the first-person shooter game "Maze War" was on the Imlac PDS-1.

In computer graphics literature, vector graphics terminals, represented by the Imlac PDS-1, which worked in a line drawing manner, used short-persistence phosphors and required refreshing to maintain the image, are commonly referred to as Random-Scan Displays. In contrast, terminals like the Tektronix 4010, utilizing long-persistence phosphors, are known as Storage Tube Displays or more frequently as Direct View Storage Tubes (DVSTs). Most CRT displays today, including televisions, scan sequentially and are thus known as Raster-Scan Displays.

Acquiring a vector graphics terminal is considerably challenging nowadays, but we can simulate it using software. On Linux systems, using the xterm that comes with most distributions, we can emulate Tektronix graphic terminals (xterm simulates the Tektronix 4014, a 19-inch model, while the original 4010 used an 11-inch screen). The command `xterm -t` starts xterm's built-in Tektronix emulation mode. Here, the backspace key doesn't erase characters already entered on the screen. When new content exceeds a screen, it overlays directly on the old content rather than replacing it. To clear the screen in this scenario, you must use the Linux `clear` command. These are specific features of Tektronix 4010 and similar storage tube displays.

In the 1970s, vector graphics terminals were widely used for engineering and scientific graphics. Tektronix developed a set of FORTRAN language subprograms for drawing, known as PLOT-10[^4]. While configuring PLOT-10 today can be complex, I demonstrated using the commonly available interactive plotting software Gnuplot on Linux. Gnuplot was initially released in 1986 and hence adequately supports Tektronix terminals.

In May 1976, an article by Charles J Fritchie, a chemistry professor at Tulane University, titled "Economical Graphics from Storage CRTs" appeared in Computer Graphics and Art magazine[^5], discussing attempts to use storage-type cathode-ray tubes as inexpensive computer graphics devices.

If we examine computer graphics magazines of that time, we'll find that many computer graphics were based on lines. This early form of computer graphics also influenced the depiction of virtual worlds in 1980s science fiction movies and paintings. In the science fiction works of that era, luminous line graphics often represented computer-generated virtual worlds[^6].

Another essential vector display device was PLATO, the "Programmed Logic for Automatic Teaching Operations" terminal[^7]. The PLATO emulator in computer museums' websites today is a modern enthusiast's re-creation. While the website version supports color, the original PLATO terminal only had black and white display capabilities. Many prototypes of electronic games were incubated on the PLATO terminal. For instance, the earliest implementation of the Solitaire card game was on the PLATO platform. Additionally, the PLATO system was the starting point for many social and collaborative systems. For instance, PLATO Notes marked the beginning of groupware, and the well-known Lotus Notes got its name from this system[^8]. PLATO was also one of the earliest devices worldwide to use a touchscreen. The PLATO IV, in 1964, utilized a plasma display with a touchscreen.

## Pen Plotters
Another type of image output device that works using vector graphics is the pen plotter. The widely used engraving machine we have today is essentially a type of pen plotter, but instead of a pen tip, it uses a cutting blade. The model we're using on-site is the relatively common Keli engraving machine in China, which can be easily switched to use a regular ballpoint pen for drawing.

Plotter is one of the earliest computer graphics output devices. The first commercialized computer plotter was the 1959 Calcomp 565 drum plotter. Its drum moved the paper vertically, while the pen moved horizontally on a crossbar to position the pen tip and complete the drawing on a 2D plane.

Most engraving machines and plotters available today are controlled using HP-GL language. HP-GL, developed by HP in 1977 for the HP-8972 plotter, commonly uses two commands: PU (Pen Up) and PD (Pen Down), corresponding to lifting and lowering the pen, respectively. Usually, each PU or PD command is followed by two numbers, denoting the two-dimensional coordinates of the next destination for the pen tip. Lifting, lowering, horizontal movement, and vertical movement are the four basic actions present in almost all plotters.

Gnuplot, as introduced earlier, can generate HP-GL files for plotters. The open-source vector graphic design software, InkScape, can export AutoCAD DXF or HP-GL files for engraving machines and plotters. HP-GL is human-readable and writable, allowing us to write programs to generate HP-GL command sequences for artistic output through plotters.

In recent years, there has been a "renaissance" in the overseas digital art community, where artists and enthusiasts realize that using different pen tip materials and drawing trajectories can bring more variations to computer-generated art. In his work "Plotter Drawing" in 2015, Japanese artist Hiromasa Fukaji used an engraving machine and a Kuretake brush pen to create generative art with ink-like aesthetics[^9].

In January 2016, the hashtag #plottertwitter emerged on Twitter and became a code for enthusiasts to showcase their plotter artworks. Brian Boucheron, one of the initiators of #plottertwitter, compiled a vast amount of plotter-related information on his Github[^10], and Derrick Schultz was among the earliest artists to create works using the #plottertwitter tag[^11]. In the fall of 2021, Professor Golan Levin from Carnegie Mellon University initiated the "DrawingWithMachines" course, systematically discussing and teaching creative programming focused on plotters[^12].

In China, using plotters for generative art is still a relatively new topic, but the related equipment is not hard to find. Advertising companies often use engraving and cutting machines, which can be converted into plotters by simply changing the pen tip. Products like the AxiDraw, representing "writing robots," can also be found on platforms like Taobao.

## LOGO Language

While vector monitors and plotters are no longer common today, the logic of computer-generated vector graphics might not be entirely unfamiliar to everyone. Even today, many elementary and middle school computer classes still utilize LOGO language, known as turtle graphics. Its logic closely aligns with that of plotters, incorporating commands like PU (Pen Up) and PD (Pen Down) for lifting and lowering the pen, common to both LOGO language and plotter languages. The "turtle," once sold as an accessory for LOGO language, was essentially a kind of plotter itself.

On platforms like Taobao, we can still find items resembling "turtles," such as "drawing cars," but they might not directly support control through LOGO language anymore. However, creating patterns for plotter output using LOGO language remains feasible. UCBLogo[^13] stands out as the most actively maintained and well-documented LOGO language environment, perfect for initiating artistic creations. By importing images from UCB Logo into Inkscape, one can still use a plotter to draw patterns created with LOGO language[^14].

Seymour Papert, the designer of LOGO language, wrote "Mindstorms: Children, Computers, and Powerful Ideas," delving into the design philosophy of LOGO and the problems it aimed to solve. In the previous six sessions, we've peeled back the layers of computer art's magnificent shell, tracing back to its primitive state—while the mobile devices discussed in the first session were products of the 21st century, the content we're discussing in this session dates back to the 1960s. Exploring LOGO language, born in 1967, might evoke a different sense of discovery.

## Line Printers
When using printers today, one of the first parameters we typically consider is the paper size, such as A3, A4, or Letter paper. This is because most printers on the market, especially laser printers, are page printers. However, laser printers only emerged in the market around 1976 (IBM 3800, a large commercial laser printer). Prior to this, many printers did not offer whole-page output capabilities. They either functioned like typewriters, producing one character at a time, or operated as line printers, processing an entire line at once.

The most common printers that output a single character at a time today are dot matrix printers, commonly found in banks for passbook printing or for printing multi-part invoices. Thermal printers, frequently seen in stores and used for receipts in the courier industry, represent the most prevalent line printers.

Previously, line printers referred specifically to drum printers and chain/train printers used on larger computers. Their printing devices could cover the entire width of the paper, allowing printing of multiple characters simultaneously, making them faster than printers that could only output one character at a time. However, after the 1990s, their primary applications—generating results and log outputs for large computers—were gradually replaced by video displays. They weren't widely used on microcomputers, and works with similar but lower print volumes were typically handled by dot matrix printers. Even the printer used in our demonstration today is a dot matrix printer.

In terms of software, since line printers were once the most widely used devices on computers, both DOS and Linux default to treating printers as line printers when handling them. This means that regardless of content length, they default to line breaks after printing. Additionally, the computer's printer interface is also known as LPT (line print terminal) or lp (Unix and Linux terminology, an abbreviation for line printer).

Both character and line printers output characters of equal width, making it more convenient to create tables using computers. They also offered a different path for computer art creation distinct from vector graphics—using characters to form images. In 1968, Richard Williams developed ART1 at New Mexico State University on an IBM 360 computer, providing a user-friendly computer art creation tool for non-technical individuals[^15]. Notably, although the computer images created by ART1 resemble "ASCII Art" greatly, strictly speaking, it isn't "ASCII" because the IBM mainframes at that time used EBCDIC encoding, so the characters available were different from today's ASCII Art. In recent years, software engineers have even developed art1.js, porting ART1 to the Node.js[^16].

Line printers can directly print text output from a computer without concerns about paper, font sizes, or typesetting issues, and dot matrix printers can also function in this manner. In Linux, by using the ">" symbol to redirect output, you can print program or command results directly through the printer. For instance, the "echo" command outputs characters:
```bash
echo "hello world"
```
This command will display "hello world" on the screen. If we redirect it to the printer:
```bash
# The first command sets write permissions for the printer
chmod 664 /dev/usb/lp0
# The second command sends the text to the printer
echo "hello world" > /dev/usb/lp0
```
Similarly, the `cat` command can concatenate files and output them to the printer, such as printing a text file:
```bash
cat demo1.txt > /dev/usb/lp0
```
Furthermore, tools like Gnuplot can output charts as character images to printers as well[^17].

## Video Display Terminals

Until the 1970s, the primary means of interacting with computers was through teleprinters. Though vector-based display terminals were gradually accepted for industry applications like CAD, they remained too expensive for regular office use. In 1970, the Tektronix 4014 was priced at $8,450, which, adjusted for inflation, exceeds $40,000 today. In contrast, the commonly used teleprinter, ASR 33, ranged from $755 to $1,220, depending on the configuration[^18].

Teleprinters had evident limitations, such as requiring consumables like paper and ribbons and having slow output speeds. During the 1960s, some terminals, including the IBM 2260, used CRT displays to present text content instead of hard copies on paper. These terminals were referred to as Video Display Terminals (VDTs) or Video Display Units (VDUs).

An important event in the popularization of video display terminals was the publication in September 1973 of Don Lancaster's "TV Typewriter" in the magazine "Radio-Electronics." This invention brought a significant cost advantage to video terminals. Hobbyists needed only around $200 worth of components to create a computer terminal using a TV as a display screen. The "TV Typewriter" gained popularity among computer enthusiasts of the time. Coupled with newly introduced microcomputers like the Altair 8800, enthusiasts could conduct computer experiments at home that were previously only possible in large computer rooms. This invention also linked personal computers to television technology right from their inception.

Towards the late 1970s, the Intel 8080 microprocessor was used in the DEC VT100 terminal, the first ANSI escape sequence-based video terminal (unprintable control strings used for functionalities like underlining, reverse colors, etc.), becoming the de facto standard for text terminals. The display specifications of the VT100 terminal were 80 columns and 24 rows.

Most computer terminals today inherit this specification. Slight variations exist, such as the IBM PC DOS's standard specification of 80 columns and 25 rows, one row more than the VT100. In many cases, terminal emulation software on PCs uses this extra line as a status bar while keeping the usable space consistent with the VT100[^19].

The emergence of video terminals defined the main forms of human-computer interaction for the next 40 years—keyboard and monitor. Even today, we largely remain "trapped" in this interaction method.

For new media creators, text-based video terminals cannot display true graphics. Therefore, ASCII art or similar character-based graphics serve as the primary means of outputting images on these devices. While the output content remains fairly limited, text video terminals offer a clear advantage over printers—refresh speed, significantly faster than printers and vector terminals, enabling the creation of text animations.

If we look back to the 1990s, we find that the ASCII Art Ensemble, an influential group in net.art, produced iconic works like "Deep ASCII" (1998) and the "ASCII History of Moving Images" (1998). They employed techniques that converted movie clips into ASCII dynamic scenes, using ASCII Art to recreate famous movie segments.

The infrastructure for such creative work came from the demoscene community. The open-source ASCII Art library, AAlib, released in 1997, could convert any image or video into black-and-white ASCII Art. Similar libraries like Libcaca could generate color ANSI Art. Open-source media players like MPlayer and VLC could play video files in the form of text animations using AAlib or Libcaca[^22].

Aside from video conversion, native ASCII Art animations also have a rich practice. Simon Jansen, a software engineer from New Zealand, known as Asciimation, started making Star Wars-related ASCII animations in 1997, perhaps the most well-known among similar works[^23].

This class session comes to an end. We explored vector displays, plotters as vector graphic output devices, line printers, and electronic display terminals as text output devices. In these devices, we can see the most discussed and crucial medium in art history—paper—becoming part of computer systems and transforming into a "digitalized" medium. The paradigm of outputting on paper shifted to glass media—electronic display screens. In the next session, we'll step out of the digital computer world to explore how magic on analog media influenced new media art.

[^1]: GRAPHICS Color displays：https://webstyleguide.com/wsg2/graphics/displays.html
[^2]: Interview with Susan Kare：
https://web.stanford.edu/dept/SUL/sites/mac/primary/interviews/kare/trans.html
[^3]: What is Client-Server Architecture?
 https://contentdeliverance.com/client-server-architecture/
[^4]: Plot-10主页：http://www.gaeinc.com/plot10.html
[^5]: 《计算机图形与艺术》杂志的PDF下载：https://toplap.org/2012/09/27/pdfs-of-computer-graphics-and-art/
[^6]: 关于更多早期计算机图形的内容，可以参考Zeina Koreitem：Some Notes on Making Images with Computers
[^7]: 爱荷华州立大学Douglas W. Jones教授的PLATO资料站：http://homepage.cs.uiowa.edu/~dwjones/plato/
[^8]: 关于PLATO Notes和团队合作群件的起源，可以参考：David Wooley's "Plato Notes" are the Origins of Groupware, and "Lotus Notes" https://www.historyofinformation.com/detail.php?id=990
[^9]: Plotter Drawing - Hiromasa Fukaji：https://www.hiromasa-fukaji.com/
[^10]: awesome-plotters：https://github.com/beardicus/awesome-plotters
[^11]: Derrick Schultz - design and technology：https://dvschultz.github.io/design/bbvday.html
[^12]: DrawingWithMachines：https://github.com/golanlevin/DrawingWithMachines
[^13]: UCBLogo：https://people.eecs.berkeley.edu/~bh/logo.html
[^14]: Generating Plotter Art From Berkeley Logo：https://danmalec.com/2020/11/14/generating-plotter-art-from-berkeley-logo/
[^15]: Art1：https://ef1j.org/wiki/index.php?n=Main.Art1
[^16]: art1.js：https://github.com/piratefsh/art1.js
[^17]: How to plot at terminal using GNUPlot：https://codeyarns.com/tech/2011-01-19-how-to-plot-at-terminal-using-gnuplot.html
[^18]: ASR 33 Teletype Information：https://www.pdp8online.com/asr33/asr33.shtml
[^19]: IBM, sonic delay lines, and the history of the 80×24 display：http://www.righto.com/2019/11/ibm-sonic-delay-lines-and-history-of.html
[^20]: AA-project homepage：http://aa-project.sourceforge.net/
[^21]: libcaca - Caca Labs：http://caca.zoy.org/wiki/libcaca
[^22]: 《Linux多媒体黑客》中介绍了使用mplayer的AAlib支持以ASCII Art形式播放视频：
[^23]: STAR WARS ASCIIMATION：http://asciimation.co.nz/