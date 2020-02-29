## 在Windows和Linux上安装Microsoft SQL Server

这个页面描述了Microsoft SQL Server在Windows和基于Linux的操作系统上的几种安装方式，常见问题的解决方案和部分资源的下载链接。
如果你按照页面中的的过程无法安装Microsoft SQL Server或安装Microsoft SQL Server失败且你的问题不在常见问题中或使用页面中的解决方案无法解决你的问题。请联系我（联系方式在页面的最后）。

### Microsoft SQL Server是什么
Microsoft SQL Server是一个关系型数据库管理系统，Microsoft SQL Server 2019共有5个版本：Enterprise、Standard、Web、Developer、Express。各个版本的定义如下：

* Enterprise  
  作为高级产品/服务，SQL Server Enterprise Edition 提供了全面的高端数据中心功能，性能极为快捷、无限虚拟化，还具有端到端的商业智能，可为关键任务工作负荷提供较高服务级别并且支持最终用户访问数据见解。

* Standard  
  SQL Server Standard 版提供了基本数据管理和商业智能数据库，使部门和小型组织能够顺利运行其应用程序并支持将常用开发工具用于内部部署和云部署，有助于以最少的 IT 资源获得高效的数据库管理。

* Web  
  对于为从小规模至大规模 Web 资产提供可伸缩性、经济性和可管理性功能的 Web 宿主和 Web VAP 来说，SQL Server Web 版本是一项总拥有成本较低的选择。

* Developer  
  SQL Server Developer 版支持开发人员基于 SQL Server构建任意类型的应用程序。 它包括 Enterprise 版的所有功能，但有许可限制，只能用作开发和测试系统，而不能用作生产服务器。 SQL Server Developer 是构建和测试应用程序的人员的理想之选。

* Express  
  Express 版本是入门级的免费数据库，是学习和构建桌面及小型服务器数据驱动应用程序的理想选择。 它是独立软件供应商、开发人员和热衷于构建客户端应用程序的人员的最佳选择。 如果您需要使用更高级的数据库功能，则可以将 SQL Server Express 无缝升级到其他更高端的 SQL Server版本。 SQL Server Express LocalDB 是 Express 的一种轻型版本，该版本具备所有可编程性功能，在用户模式下运行，并且具有快速的零配置安装和必备组件要求较少的特点。

### 安装前准备

Microsoft SQL Server 2019仅支持Windows操作系统和基于Linux的操作系统。如果你使用的是基于Unix的操作系统例如：macOS或基于Unix-like（除Linux外）的操作系统且无法迁移至Windows或Linux系统请联系我（联系方式在页面的最后）。

如果你希望安装中文版的Microsoft SQL Server 2019，请将帮助中的网址中的en-us改为zh-cn。

#### Windows用户

如果你使用的是Windows操作系统请检查你的计算机符合以下要求：

* 操作系统  
  Windows10 TH1 1507或更高版本  
  Windows Server 2016或更高版本

* 处理器  
  X64架构  
  1.4GHz或更快

* 内存  
  1GB或以上

* 硬盘空间  
  6GB或以上
  
* 软件  
  Edge浏览器

* 网络  
  互联网连接  

#### Linux用户

如果你使用的是基于Linux操作系统请检查你的计算机符合以下要求：

* 处理器  
  x64架构  
  2GHz或更快  
  2个核心或以上

* 内存  
  2GB或以上

* 硬盘空间  
  6GB或以上
  
* 文件系统  
  EXT4或XFS

* 网络  
  互联网连接

### 在Windows上安装Microsoft SQL Server 

下面的内容将描述一般的在Windows操作系统上安装Microsoft SQL Server的过程，使用Docker容器拉取和运行Microsoft SQL Server的过程，使用安装介质安装Microsoft SQL Server的过程和安装Microsoft SQL Server所有特性的过程。

如果你完全不知道如何安装Microsoft SQL Server，不会使用Docker和网络连接速度较快，请参考一般的在Windows操作系统上安装Microsoft SQL Server的过程。

如果你知道如何使用Docker,请Docker容器拉取和运行Microsoft SQL Server的过程。

如果你的网络连接速度较慢或不稳定，请参考使用安装介质安装Microsoft SQL Server的过程。

如果你需要安装Microsoft SQL Server的所有特性，请参考安装Microsoft SQL Server所有特性的过程.

#### 一般的在Windows操作系统上安装Microsoft SQL Server的过程

演示环境：

* 使用VMware Workstation 15 Pro搭建的环境

* 操作系统Windows10 Pro 1909

* 4核心处理器，4GB内存和40GB外存

1 下载SQL Server 2019 Installer

1.1 进入Windows桌面  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/1.1.1.png "图片1.1.1")(图片1.1.1)

1.2 按下Windows键，打开Start Menu  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/1.2.1.png "图片1.2.1")(图片1.2.1)

1.3 在Type here to search栏键入{edge}，点击Microsoft Edge打开Microsoft Edge浏览器  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/1.3.1.png "图片1.3.1")(图片1.3.1)  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/1.3.2.png "图片1.3.2")(图片1.3.2)

1.4 在Edge的地址栏键入{[https://www.microsoft.com/en-us/sql-server/sql-server-downloads](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)}，按下enter键  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/1.4.1.png "图片1.4.1")(图片1.4.1)  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/1.4.2.png "图片1.4.2")(图片1.4.2)

1.5 向下翻页，找到并点击Download 2019 Developer edition now 按钮  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/1.5.1.png "图片1.5.1")(图片1.5.1)

1.6 在What do you to do with SQL2019-SSEI-Dev.exe(5.6MB)?对话框中点击Run按钮，等待下载完成  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/1.6.1.png "图片1.6.1")(图片1.6.1)

1.7 在UAC对话框中点击Yes按钮（你的计算机可能没有开启UAC功能如果没有弹出UAC对话框则跳过当前步）（你在计算机上安装的安全软件可能会阻止你打开SQL Server 2019，请暂时关闭你计算机上的安全软件或使安全软件允许打开SQL Server 2019）  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/1.7.1.png "图片1.7.1")(图片1.7.1)

2 安装SQL Server Installation Center

2.1 等待软件启动，在SQL Server Installer中点击Custom  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/2.1.1.png "图片2.1.1")(图片2.1.1)  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/2.1.2.png "图片2.1.2")(图片2.1.2)

2.2 在MEDIA LOCATION栏设置SQL Server Installer下载SQL Server media的目标位置(你也可以使用默认目标位置)，点击Install按钮  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/2.2.1.png "图片2.2.1")(图片2.2.1)

2.3 等待下载并安装SQL Server Installation Center  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/2.3.1.png "图片2.3.1")(图片2.3.1)

3 安装Microsoft SQL Server

3.1 在SQL Server Installation Center中点击Installation  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.1.1.png "图片3.1.1")(图片3.1.1)

3.2 在SQL Server Installation Center中点击New SQL Server stand-alone installation or add features to an existing installation  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.2.1.png "图片3.2.1")(图片3.2.1)

3.3 等待SQL Server 2019 Setup启动，在SQL Server 2019 Setup中点击Next >按钮  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.3.1.png "图片3.3.1")(图片3.3.1)  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.3.2.png "图片3.3.2")(图片3.3.2)

3.4 在SQL Server 2019 Setup中点击I accept the license terms and Privacy Statement复选框，点击Next按钮  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.4.1.png "图片3.4.1")(图片3.4.1)  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.4.2.png "图片3.4.2")(图片3.4.2)

3.5 在SQL Server 2019 Setup中点击Use Microsoft Update to check for updates(recommended)复选框，点击Next >按钮  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.5.1.png "图片3.5.1")(图片3.5.1)  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.5.2.png "图片3.5.2")(图片3.5.2)

3.6 在SQL Server 2019 Setup中点击Next >按钮  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.6.1.png "图片3.6.1")(图片3.6.1)

3.7 在SQL Server 2019 Setup中的Features:框中点击Database Engine Services，SQL Server Replication，Full-Text and Extractions for Search，SQL Client Connectivity SDK的复选框，点击SQL Server 2019 Setup中的Next >按钮  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.7.1.png "图片3.7.1")(图片3.7.1)  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.7.2.png "图片3.7.2")(图片3.7.2)  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.7.3.png "图片3.7.3")(图片3.7.3)

3.8 在SQL Server 2019 Setup中点击Next >按钮  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.8.1.png "图片3.8.1")(图片3.8.1)

3.9 在SQL Server 2019 Setup中点击Next >按钮  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.9.1.png "图片3.9.1")(图片3.9.1)

3.10 在SQL Server 2019 Setup中点击Add Current User按钮，点击Next >按钮  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.10.1.png "图片3.10.1")(图片3.10.1)  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.10.2.png "图片3.10.2")(图片3.10.2)

3.11 在SQL Server 2019 Setup中的Configuration file path:栏设置配置文件路径（你也可以使用默认路径），点击Install按钮  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.11.1.png "图片3.11.1")(图片3.11.1)

3.12 等待安装  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.12.1.png "图片3.12.1")(图片3.12.1)

3.13 在SQL Server 2019 Setup中点击Close按钮  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/3.13.1.png "图片3.13.1")(图片3.13.1)

4 安装SQL Server Management Tools

4.1 切换到SQL Server Installation Center窗口，在SQL Server Installation Center点击Install SQL Server Management Tools  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.1.1.png "图片4.1.1")(图片4.1.1)

4.2 将浏览器打开的网页([https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?redirectedfrom=MSDN&view=sql-server-ver15](https://docs.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?redirectedfrom=MSDN&view=sql-server-ver15))向下翻页，找到并点击Download SQL Server Management Studio (SSMS)  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.2.1.png "图片4.2.1")(图片4.2.1)

4.3 在What do you to do with SSMS-Setup-ENU.exe (539 MB)?对话框中点击Save按钮，等待下载完成，在SSMS-Setup-ENU.exe finish downloading.对话框中点击Run  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.3.1.png "图片4.3.1")(图片4.3.1)  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.3.2.png "图片4.3.2")(图片4.3.2)

4.4 在UAC对话框中点击Yes按钮（你的计算机可能没有开启UAC功能如果没有弹出UAC对话框则跳过当前步）（你在计算机上安装的安全软件可能会阻止你打开SSMS-Setup-ENU，请暂时关闭你计算机上的安全软件或使安全软件允许打开SSMS-Setup-ENU）  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.4.1.png "图片4.4.1")(图片4.4.1)

4.5 保存你正在进行的工作，在Microsoft SQL Server Management Studio中点击Restart  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.5.1.png "图片4.5.1")(图片4.5.1)

4.6 进入Windows桌面  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.6.1.png "图片4.6.1")(图片4.6.1)

4.7 按下Windows键，打开Start Menu  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.7.1.png "图片4.7.1")(图片4.7.1)

4.8 在Type here to search栏键入{edge}，点击Microsoft Edge打开Microsoft Edge浏览器  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.8.1.png "图片4.8.1")(图片4.8.1)  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.8.2.png "图片4.8.2")(图片4.8.2)

4.9 在Edge中点击右上角的…按钮  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.9.1.png "图片4.9.1")(图片4.9.1)

4.10 在…Menu中点击Downloads  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.10.1.png "图片4.10.1")(图片4.10.1)  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.10.2.png "图片4.10.2")(图片4.10.2)

4.11 在Downloads Menu中点击SSMS-Setup-ENU.exe项  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.11.1.png "图片4.11.1")(图片4.11.1)

4.12 在UAC对话框中点击Yes按钮（你的计算机可能没有开启UAC功能如果没有弹出UAC对话框则跳过当前步）（你在计算机上安装的安全软件可能会阻止你打开SSMS-Setup-ENU，请暂时关闭你计算机上的安全软件或使安全软件允许打开SSMS-Setup-ENU）  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.12.1.png "图片4.12.1")(图片4.12.1)

4.13 在Microsoft SQL Server Management Studio中的Location:栏设置安装路径（你也可以使用默认路径），点击Install按钮  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.13.1.png "图片4.13.1")(图片4.13.1)

4.14 等待安装  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.14.1.png "图片4.14.1")(图片4.14.1)

4.15.1 保存你正在进行的工作，在Microsoft SQL Server Management Studio中点击Restart  
![img](https://raw.githubusercontent.com/LIDAUHaipengLiu/LIDAUHaipengLiu.github.io/master/Image/4.15.1.png "图片4.15.1")(图片4.15.1)

## 联系方式

GitHub：LIDAUHaipengLiu

Email：ai.haipengliu@gmail.com

WeChat：wxid_x97qmntom5no22
