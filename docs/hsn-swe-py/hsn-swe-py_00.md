# 前言

最终，本书的目的是阐明务实的软件工程原则以及它们如何应用于 Python 开发。因此，本书的大部分内容都致力于探索和实施我认为是现实范围的，但可能是不切实际的项目：一个分布式产品管理和订单履行系统。在许多情况下，功能是从头开始开发的，从最基本的概念和假设出发，这些概念和假设构成了系统的基础。在现实世界的情况下，很可能会有现成的解决方案来处理许多实现细节，但我认为揭示底层理论和要求是至关重要的，以便理解为什么事情会发生。我认为，这是编程和软件工程之间的本质区别的一个重要部分，无论涉及哪种编程语言。

在许多方面，Python 是一种罕见的语言——它是一种动态语言，但又是强类型的。它也是一种面向对象的语言。这些特点使得它成为一种非常灵活，有时甚至是强大的语言。虽然这可能是我的观点，但我坚信很难找到另一种语言，既像 Python 一样通用，又像 Python 一样易于编写和维护代码。Python 在语言官方网站上列出了许多成功案例，这一点并不让我感到意外（[`www.python.org/about/success/`](https://www.python.org/about/success/)）。同样，我并不感到意外的是 Python 是至少两家大型公共云提供商——亚马逊和谷歌的核心支持语言之一。即便如此，它仍然经常被认为只是一种脚本语言，我真诚地希望本书也能证明这种观点是错误的。

# 本书的受众

这本书旨在针对具有一定 Python 经验的开发人员，希望将他们的技能从“只是编写代码”扩展到更加“软件工程”方向。假定读者已经掌握了 Python 基础知识——函数、模块和包，以及它们与项目结构中文件的关系，以及如何从其他包中导入功能。

# 本书涵盖的内容

第一章，*编程与软件工程*，讨论了编程（仅仅是编写代码）与软件工程之间的区别——学科、思维方式以及它们的影响。

第二章，*软件开发生命周期*，详细研究了软件开发生命周期，特别关注与软件工程相关的输入、需求和结果。

第三章，*系统建模*，探讨了对系统及其组件的功能、数据流和进程间通信方面进行建模和绘图的不同方式，以及这些信息对于软件工程的意义。

第四章，*方法论、范式和实践*，深入探讨了当前的过程方法论，包括一些敏捷过程的变体，以及审视每种方法的优缺点，然后审查**面向对象编程**（**OOP**）和函数式编程范式。

第五章，*hms_sys 系统项目*，介绍了本书中用于练习软件工程设计和开发思维的示例项目背后的概念。

第六章，*开发工具和最佳实践*，调查了一些更常见（或至少是容易获得的）开发工具——用于编写代码和以减少持续开发工作和风险的方式进行管理。

第七章《设置项目和流程》演示了一个示例结构，可用于任何 Python 项目或系统，并介绍了在建立与源代码控制管理、自动化测试和可重复构建和部署流程兼容的共同起点时的思考过程。

第八章《创建业务对象》开始了`hms_sys`项目的第一次迭代，定义了核心库业务对象数据结构和功能。

第九章《测试业务对象》在设计、定义和执行可重复自动化测试业务对象代码之后，结束了`hms_sys`项目的第一次迭代。

第十章《思考业务对象数据持久性》探讨了应用程序中对数据持久性的常见需求，一些更常见的机制，以及选择“最佳匹配”数据存储解决方案的标准，以满足各种实施需求。

第十一章《数据持久性和 BaseDataObject》通过设计和实现一个通用的抽象数据访问策略，可以在项目的任何组件中重复使用，开始了`hms_sys`项目的第二次迭代。

第十二章《将对象数据持久化到文件》通过具体实现抽象的数据访问层（DAL），将业务对象数据持久化到本地文件，继续了第二次迭代的工作。

第十三章《将数据持久化到数据库》实现了一个具体的数据访问层，该层可以从常用的 NoSQL 数据库 MongoDB 中存储和检索数据，并将该方法与等效的基于 SQL 的数据访问层的要求进行了比较。

第十四章《测试数据持久性》通过实施针对第二次迭代中构建的两种不同数据访问层策略的自动化测试，来结束`hms_sys`项目的第二次迭代。

第十五章《服务的解剖》分析了独立服务的常见功能要求，并通过构建抽象服务/守护程序类来实现，这些类可重复使用以创建各种具体的服务实现。

第十六章《工匠网关服务》通过分析系统组件的通信需求，几种实现这些通信的选项，保护它们，并最终将它们融入项目的核心服务的具体实现，开始了`hms_sys`项目的第三次迭代。

第十七章《处理服务事务》考虑了`hms_sys`组件之间所有必要的业务对象通信，提取了它们的一些共同功能，并介绍了实现它们所需的过程。

第十八章《测试和部署服务》总结了本书中`hms_sys`的开发，并调查和解决了服务/守护程序应用程序的一些常见自动化测试问题。

第十九章《Python 中的多处理和高性能计算》介绍了编写可以在单台计算机上扩展到多个处理器，或在集群计算环境中扩展到多台计算机的 Python 代码的理论和基本实践，并提供了在常见高性能计算系统上执行 Python 代码的起点代码结构变化。

# 为了充分利用本书

您应该特别了解以下内容：

+   如何下载和安装 Python（在撰写本书时使用了 3.6.x，但这里的代码预计在 3.7.x 中可以少量或不需要修改地工作）

+   如何编写 Python 函数

+   如何编写基本的 Python 类

+   如何使用 pip 安装 Python 模块，以及如何将模块导入您的代码

# 下载示例代码文件

您可以从[www.packt.com](http://www.packtpub.com)的帐户中下载本书的示例代码文件。如果您在其他地方购买了本书，您可以访问[www.packt.com/support](http://www.packtpub.com/support)并注册，以便直接将文件发送到您的邮箱。

您可以按照以下步骤下载代码文件：

1.  登录或注册[www.packt.com](http://www.packtpub.com/support)

1.  选择 SUPPORT 选项卡

1.  单击“代码下载和勘误”

1.  在搜索框中输入书名，然后按照屏幕上的说明进行操作

下载文件后，请确保使用最新版本的解压缩软件解压缩文件夹：

+   WinRAR/7-Zip 适用于 Windows

+   Zipeg/iZip/UnRarX 适用于 Mac

+   7-Zip/PeaZip 适用于 Linux

该书的代码包也托管在 GitHub 上**[`github.com/PacktPublishing/`](https://github.com/PacktPublishing/Hands-On-Software-Engineering-with-Python)****[Hands-On-Software-Engineering-with-Python](https://github.com/PacktPublishing/Hands-On-Software-Engineering-with-Python)**。我们还有其他代码包来自我们丰富的图书和视频目录，可在**[`github.com/PacktPublishing/`](https://github.com/PacktPublishing/)**上找到。去看看吧！

# 下载彩色图片

我们还提供了一个 PDF 文件，其中包含本书中使用的屏幕截图/图表的彩色图片。您可以在这里下载：[`www.packtpub.com/sites/default/files/downloads/9781788622011_ColorImages.pdf`](https://www.packtpub.com/sites/default/files/downloads/9781788622011_ColorImages.pdf)。

# 使用的约定

本书中使用了许多文本约定。

`CodeInText`：表示文本中的代码词、数据库表名、文件夹名、文件名、文件扩展名、路径名、虚拟 URL、用户输入和 Twitter 句柄。例如："在`src`目录中是项目的包树。"

代码块设置如下：

```py
def SetNodeResource(x, y, z, r, v):
    n = get_node(x,y)
    n.z = z
    n.resources.add(r, v)
```

当我们希望引起您对代码块的特定部分的注意时，相关行或项目会以粗体显示：

```py
 def __private_method(self, arg, *args, **kwargs):
        print('%s.__private_method called:' % self.__class__.__name__)
        print('+- arg ...... %s' % arg)
        print('+- args ..... %s' % str(args))
        print('+- kwargs ... %s' % kwargs)
```

任何命令行输入或输出都以以下方式编写：

```py
$python setup.py test
```

**粗体**：表示新术语、重要单词或屏幕上看到的单词，例如菜单或对话框中的单词，也会在文本中以这种方式出现。例如："从管理面板中选择系统信息。"

警告或重要提示会以这种方式出现。提示和技巧会以这种方式出现。