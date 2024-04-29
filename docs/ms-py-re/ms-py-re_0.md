# 前言

自计算机科学迈出第一步以来，文本处理一直是最重要的话题之一。经过几十年的研究，我们现在拥有了最多才多艺和无处不在的工具之一：正则表达式。验证、搜索、提取和替换文本的操作得以简化，这要归功于正则表达式。

本书最初将从鸟瞰角度介绍正则表达式，逐步深入更高级的主题，如 Python 中的正则表达式细节或分组、解决方法和性能。所有主题都将以 Python 特定的示例进行介绍，这些示例可以直接在 Python 控制台中使用。

# 本书涵盖的内容

第一章，“介绍正则表达式”，将从非 Python 特定的角度介绍正则表达式语法的基础知识。

第二章，“Python 中的正则表达式”，将介绍 Python 的正则表达式 API 及其特点。

第三章，“分组”，涵盖了提取信息部分、对特定部分应用量词以及执行正确交替的正则表达式功能。

第四章，“四处张望”，解释了零宽断言的概念和不同类型的四处张望机制。

第五章，“正则表达式的性能”，将涵盖不同的工具来衡量正则表达式的速度，Python 的正则表达式模块的细节，以及改进正则表达式性能的不同建议。

# 本书所需内容

为了理解本书，需要对任何支持的平台上的 Python 有基本的了解。能够使用带有 Python 命令行访问权限的控制台非常重要。

不需要先前对正则表达式的了解，因为将从零开始介绍。

# 本书的受众

本书适用于希望了解正则表达式一般情况以及如何在 Python 中具体利用它们的 Python 开发人员。

# 约定

在本书中，您会发现一些文本样式，用以区分不同类型的信息。以下是一些这些样式的示例，以及它们的含义解释。

文本中的代码词、数据库表名、文件夹名、文件名、文件扩展名、路径名、虚拟 URL、用户输入和 Twitter 句柄显示如下：“我们可以通过使用`include`指令来包含其他上下文。”

代码块设置如下：

```py
>>> import re
>>> pattern = re.compile(r'<HTML>')
>>> pattern.match("<HTML>")
```

当我们希望引起您对代码块的特定部分的注意时，相关行或项目会以粗体显示：

```py
>>> import re
>>> pattern = **re.compile(r'<HTML>')**
>>> pattern.match("<HTML>")
```

**新术语**和**重要单词**以粗体显示。屏幕上看到的单词，例如菜单或对话框中的单词，会以这样的方式出现在文本中：“点击**下一步**按钮会将您移动到下一个屏幕”。

### 注意

警告或重要说明会以这样的方式出现在一个框中。

### 提示

提示和技巧会出现在这样的形式中。