  保密

17计科2班第7小组
日期：2020.6.11


图书管理系统
[需求说明书]

1引言
1.1编写目的
编写本报告的目的是明确本系统的详细需求，供使用单位确认系统的功能和性能，并作为软件设计人员的设计依据和使用单位的验收标准。为明确软件需求、安排项目规划与进度、组织软件开发与测试，撰写本文档。  对图书管理系统软件功能的实现和评判进行描述；将作为软件开发过程的其他所有开发的基础；为开发人员、维护人员、客户人员间提供共同的协而创立基础；规范描述项目投资者就系统的功能和必须符合的条件达成的一致意见。
预期读者为客户、业务需求分析人员、测试人员、用户文档编写者、项目管理人员、系统分析员、软件架构师、软件工程师。
1.2背景
随着社会的进步，信息技术的广泛应用，数字化管理的优势日趋显著。针对中小型图书馆或图书室管理落后的情况，设计实现一个图书信息管理系统。通过与计算机的结合使用对中小型图书馆或图书室的各种图书信息进行管理可以给管理员和用户带来以下不同的方便：检索迅速、查找方便、可靠性高、存储量大、保密性好、寿命长、成本低等。这些优点能够极大地提高工作效率，也是图书馆等部门管理科学化、正规化的重要标志之一。而且计算机管理的成本不断降低。因此，开发一套这样的中小型图书管理软件已经很有必要，并且实现研究服务于实践的原则。
A. 图书管理系统 
B. 本项目的任务提出者：平顶山学院计算机学院（软件学院）  
   开发者：17计科2班第7小组  
   用户：平顶山学院全体老师和学生   
C. 该系统采用B/S架构，它的各子功能模块相互独立，使得与其它接口简单。
1.3定义
缩写、术语	解释
Library Management System(缩写：LMS)	图书管理系统
图书管理系统软件:它是我们软件组完全自主开发的图是管理系统软件，以图书馆管理部门和终端用户为业务对象的用Java语言编程来实现其功能的软件。
UML:统-建模语言(UML是Unified Modeling Languae的缩写)是用来对软件密集系统进行可视化建模的一种语言。UML为面向对象开发系统的产品进行说明、可视化、和编制文档的一种标准语言。
B/S结构: Browser/Server 结构,即浏览器和服务器结构。它是对C/S结构的一种变化或者改进的结构。在这种结构下,用户工作界面是通过www浏览器来实现极少部分事务逻辑在前端(Browser)实现,主要事务逻辑在服务器端(Server)实现，server 端访问数据库，形成所谓三层3-tier结构.
2任务概述
2.1软件标识
系统名称：信息采集及管理系统；
系统编号：HBXXCJXT
版本号：V1.0
2.2目标
本软件的目标是使图书管理系统管理电子化、系统化、简单化，以节省图书管理方面不
必要的资源浪费。该管理系统的最终用户为终端用户，管理人员和其他相关人员。本系统包括了图书馆内管理的一般功能。还包括一些其他的系统功能，诸如新书发布，旧书处理以及催还等。目标还包括:
1.减少人力资源的使用和降低管理费用，提高信息准确度和可靠性;
2.改进图书馆内管理和人员服务;
3.建立高效的信息传输和服务平台，提高信息处理速度和利用率;
4.系统设计优良，界面设计精美、友好、快捷,人性化设计,后台管理功能强大效率高;
5.更简便、信息化程度更高的图书管理流程;
2.3假定和约束
用户急需应用本软件系统，要求项目组在两个月内完成任务,初步实现的功能模块为信息发布、借书信息管理、还书信息管理、交流互动与用户管理等，开发人员初定为6人项目.
组，开发与运行的硬件平台要能够支持多用户并发访问。
本软件在开发的过程中，分为技术实现与软件工程两大部分，两大部分都有侧重点，若技术支持出现故障或疑难问题无法解决、程序开发出现偏差，会延误工程进度,影响工程的按期完工。若软件工程陈述出现问题，部分描述含混不清，则会影响系统的完整性与可继承性。在管理方面，如管理者没有预见性，开发模块之间的互动，从而影响工程的顺利开展，对出现的问题无法采用可行的解决手段，都会影响导致工程无法按期完工。
图书管理系统采用的是B/S结构的软件体系，服务器采用Asp.net技术，后台数据库采用mySQL。
开发期限：2020年6月20日完成；
编程语言：Java，JavaScript
系统环境：Eclipse；
安全和保密要求：数据库主键加密；后台系统身份认证
3需求规定 
3.1项目功能描述用
用户分为两类：读者、图书管理员。
图书管理员可以修改读者信息，修改数目信息，查看所有借还日志等；
读者仅可以修改个人信息、借阅或归还书籍和查看自己的借还日志。





3.1.1逻辑设计
1.图书书目表book_info

2.数据库管理员表admin

3.图书分类表class_info

4.节约信息表lend_info

5.借阅卡信息表reader_card

6.读者信息表reader_info


3.1.2 数据流图

3.2对性能的规定
3.2.1精度
图书管理系统对数据的精度要求是根据信息存储的形式、借书还书的结果等量化而制定的。查询时应保证查全率，所有相应域包含查询关键字的记录都应能查到;
查询时应保证查准率,查到的记录应与给定的单项或组合查询条件不完全匹配的模糊查询;录入数据合法性的检验应当精确;
密码允许输入6-8个字母或者数字:用户输入查询信息应不区分大小写。
3.2.2时间特性要求
由于此开发项目针对图书馆，使用频度较高，使用性要求比较高。为防止对信息资料和管理程序的恶意破坏，要求有较为可靠的安全性能。总之,要求稳定、安全、便捷，易于管理和操作。
1.查询速度:不超过10秒;
2.其它所有交互功能反应速度:不超过3秒;
3.可靠性:平均故障间隔时间不低于200小时。
4.响应时间。应在1~2秒内，对软磁盘和打印机的操作，以及数据的导入和导出也应在可接受的时间内完成;
3.2.3灵活性
作为独立运行的系统和其他管理系统集成的系统。
图书管理系统的设计是做为独立运行的系统而进行的。本系统具有独立的服务器系统和
数据库系统，具有完善数据输入输出功能和数据维护及查询的报表生成与打印系统。且发生故障时，能快速恢复系统和故障处理，方便系统升级和扩充，故障恢复时间不超过5小时。为了适应内外机构的数据要求,与图书管理系统前台借还系统交换信息，与国家管理机构相关系统的数据交换，本系统专门设计了与这些系统数据交换扩展接口。
本系统去采用浏览器标准界面，本身具有操作灵活的特点。
可能提供鼠标选择和键盘输入双重输入功能。方便用户操作和管理。
3.2.4不可抗拒性
因源网址关闭、失效、断电、信息删除、出错造成数据无法采集。
3.3功能展示
3.3.1首页登录
管理者账号：123456/123456 读者账号：10000/123456


3.3.2管理员系统
登录进入
3.3.2.1图书管理

3.3.2.2图书详情

3.3.2.3读者管理

3.3.2.4借还管理

3.3.3读者系统
3.3.3.1查看全部图书

3.3.3.2个人信息查看、可修改个人信息

3.3.3.3个人借阅情况查看


3.4数据管理能力要求
3.4.1概念设计
a．表的主键进行加密处理。
b．数据库表结构设计符合关系型数据库第三范式要求。
c．字段数据类型和约束条件设定可以确保数据安全、有效。
3.4.2 DBMS性能要求
a．使用MySQL数据库5.0+版本。
b．存储容量：满足用户对于数据库的需求。
c．安全性、保密性高。

3.5故障处理要求
正常使用时不应出错，若运行时遇到不可恢复的系统错误，也必须保证数据库完好无复。要在项目报名时的没隔一段时间进行数据备份，以免在资料意外丢失时，无法进行恢对系统故障的处理要求区分故障的严重程度,尽可能的对错误进行恢复。随时监控,在文档、报表处理，打印机，操作系统等软硬件出现故障时、具备保数据的功能，并及时反映到主机中。

a、记录采集、查重和格式化日志，预留人工故障排查接口，及时发现故障原因。
b、系统每天固定时间进行备份，可在数据读脏状态下进行回滚。
c、如遇不可抗拒力情况，如断电、系统崩溃。保证数据处于突发情况前的最新状态，并完成数据备份。
d、对失效或出错链接设置提示处理，智能跳过恶意链接（病毒、敏感、纯广告、被举报过的网址）。
3.6其他专门要求
3.6.1安全性要求
3.6.1.1访问安全性要求

该图书管理系统，用户主要分为管理员和读者，其中为登录系统的读者只可以搜索和查看图书信息，只有在成功登录系统后才能查看借阅信息，办理续借手续等操作。管理员只有成功登陆系统后才能进行对图书、读者及借还书的管理操作。

3.6.1.2数据安全性要求

该系统的相关数据都存储在数据库内，不能够随意由人们更改,读者只能通过系统查看图书和借阅信息，可以进行办理续借的手续，其他操作由管理员进行。管理员成功登录后可以对自己所管辖的信息进行更改，其他人一概没有权利进行任何更改操作。系统内部数据在定期更新时都要求有备份。
3.6.2可靠性要求
3.6.2.1容错性要求

整体系统运行稳定，有很强的防错、抗错能力，保证数据报送正常进行。在系统出现错误或者异常时，可以及时的保存数据，确保重要相关数据、相关信息不会丢失。

3.6.2.2 可恢复性要求

在进行数据信息录入或更新时，系统会间隔固定时间自动保存,在系统出现异常时，数据可自动回复发生异常前的数据。

3.6.2.3其他可靠性要求

操作可靠性:读者及管理人员访问网站时都能正常操作。
数据可靠性:数据信息是管理员定期更新的，具有实时、准确和可靠性。
3.6.3易用性要求
3.6.3.1界面友好性要求

该图书管理系统设计的界面友好，用户操作简单容易，在操作的页面上均有操作提示，
而其页面显示都是采用最便于用户使用的控件和布局方式。

3.6.3.2易操作性要求

无论是对于管理员还是读者该图书管理系统的操作都是简单便捷的,即有较高可操作和易操作性，在响应时间上又较短，所以可以较大的提高操作的效率。

3.6.3.3其他易用性要求

在系统中有需要时间信息的地方，均给出了日历，用户只需选择日期即可，不需自己再
去添加。
3.6.4性能要求
3.6.4.1数据访问性能要求

该图书管理系统利用数据缓存，既保证了数据库中原始数据的可靠性，又能够加强数据之间的交互效率。

3.6.4.2 数据传输性能要求

该图书管理系统数据在上传时会经过部分压缩，以加强数据的统- -保存和处理,还能节省数据所占用的空间，给数据库减小压力。
3.6.5可维护性要求
3.6.5.1公共数据要求

在数据更新时，不同的管理员在更新自己输入的信息时，需要先同步其他管理员已经录入好的信息，没有冲突才能将自己的录入。录入的数据全部按照一定 顺序进行排列储存所以维护比较容易。

3.6.5.2公共框架开发要求

采用微软公司推出的跨语言的平台aspnet框架，该框架有较好的可维护性。
3.6.6 可移植性要求
3.6.6.1适应性要求

该系统是基于网页界面，可以用于任何有浏览器的联网计算机，能实现跨平台操作,同时系统灵活性很强，可以随时进行内容修改和界面的更新。另外也适应多种数据传输方式，能够提供灵活的配置以适应业务需求。

3.6.6.2 易安装性要求

该系统安装简单，只需将可执行程序在具备预期的使用环境所示环境的主机.上运行即可在主服务器上安装成功后客户端只需通过互联网便可登录该系统的网站，进行相关操作。
4运行环境规定
4.1设备运行平台
开发环境：Windows 10，IntelliJ IDEA 2018.3
运行配置
1.首先安装Mysql5.7，设置用户名为root，密码为123456，并保证其在运行状态，并执行library.sql文件导入数据。
2.然后再配置Maven到环境变量中，在源代码目录下运行
# mvn jetty:run
3.使用浏览器访问http://localhost:8080即可进入系统。