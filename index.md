## 在Windows和Linux上安装Microsoft SQL Server
### Microsoft SQL Server是什么
Microsoft SQL Server是一个关系型数据库管理系统，Microsoft SQL Server 2019共有5个版本：Enterprise、Standard、Web、Developer、Express。各个版本的定义如下：

* Enterprise

  作为高级产品/服务，SQL Server Enterprise Edition 提供了全面的高端数据中心功能，性能极为快捷、无限虚拟化1，还具有端到端的商业智能，可为关键任务工作负荷提供较高服务级别并且支持最终用户访问数据见解。

* Standard 

  SQL Server Standard 版提供了基本数据管理和商业智能数据库，使部门和小型组织能够顺利运行其应用程序并支持将常用开发工具用于内部部署和云部署，有助于以最少的 IT 资源获得高效的数据库管理。

* Web

  对于为从小规模至大规模 Web 资产提供可伸缩性、经济性和可管理性功能的 Web 宿主和 Web VAP 来说，SQL Server Web 版本是一项总拥有成本较低的选择。

* Developer

  SQL Server Developer 版支持开发人员基于 SQL Server构建任意类型的应用程序。 它包括 Enterprise 版的所有功能，但有许可限制，只能用作开发和测试系统，而不能用作生产服务器。 SQL Server Developer 是构建和测试应用程序的人员的理想之选。

* Express

  Express 版本是入门级的免费数据库，是学习和构建桌面及小型服务器数据驱动应用程序的理想选择。 它是独立软件供应商、开发人员和热衷于构建客户端应用程序的人员的最佳选择。 如果您需要使用更高级的数据库功能，则可以将 SQL Server Express 无缝升级到其他更高端的 SQL Server版本。 SQL Server Express LocalDB 是 Express 的一种轻型版本，该版本具备所有可编程性功能，在用户模式下运行，并且具有快速的零配置安装和必备组件要求较少的特点。

### 安装前准备

Microsoft SQL Server 2019仅支持Windows操作系统和基于Linux的操作系统。如果你使用的是基于Unix的操作系统例如：macOS或基于Unix-like（除Linux外）的操作系统且无法迁移至Windows或Linux系统请联系我。

#### Windows用户

如果你使用的是Windows操作系统请检查你的计算机符合以下要求：

* 操作系统

  Windows10 TH1 1507或更高版本
  Windows Server 2016或更高版本

* 处理器

  X64架构  
  1.4GHz或更快

* 内存

  1GB以上

* 硬盘空间

  6GB以上
  
