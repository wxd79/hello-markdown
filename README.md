# Markdown介绍

- [Markdown介绍](#markdown介绍 )
  - [1. Markdown是什么](#1-markdown是什么 )
    - [1.1. Markdown的特点](#11-markdown的特点 )
    - [1.2. Markdown vs 各路英豪](#12-markdown-vs-各路英豪 )
    - [1.3. 编辑方式](#13-编辑方式 )
      - [1.3.1. VSCode + MPE](#131-vscode-mpe )
    - [1.4. 使用方式](#14-使用方式 )
      - [1.4.1 Gitlab](#141-gitlab )
      - [1.4.2 Redmine](#142-redmine )
  - [2. 基础语法](#2-基础语法 )
    - [2.1. 标题](#21-标题 )
    - [2.2. 段落](#22-段落 )
    - [2.2.1. 斜体](#221-斜体 )
    - [2.2.2. 粗体](#222-粗体 )
    - [2.2.3. 粗斜体](#223-粗斜体 )
    - [2.2.4. 通常强调](#224-通常强调 )
    - [2.2.5. 转义](#225-转义 )
    - [2.3. 列表](#23-列表 )
      - [2.3.1. 有序列表](#231-有序列表 )
      - [2.3.1. 无序列表](#231-无序列表 )
    - [2.4. 引用](#24-引用 )
    - [2.5. 代码块](#25-代码块 )
    - [2.6. 链接](#26-链接 )
    - [2.7. 图片](#27-图片 )
    - [2.8. 表格](#28-表格 )
  - [3. 功能增强插件](#3-功能增强插件 )
    - [3.1. 作图](#31-作图 )
      - [3.1.1. Mermaid](#311-mermaid )
    - [3.1.2. Markdown自动生成图片的优势](#312-markdown自动生成图片的优势 )
    - [3.2. TOC](#32-toc )
    - [3.3. 数学公式](#33-数学公式 )
  - [4. 参考资料](#4-参考资料 )

## 1. Markdown是什么

Markdown是一种轻量级的标记语言，可用于将格式设置元素添加到纯文本文档中。  
Markdown 由[John Gruber](https://daringfireball.net/projects/markdown/)于2004年创建，如今已成为世界上最受欢迎的标记语言之一。

直观的来说，Markdown是`纯文本文件`，如果你用记事本打开我现在用的这个文档，所以它看上去大概是这个样子：

```markdown

# Markdown介绍

[TOC]

## 1. Markdown是什么

Markdown是一种轻量级的标记语言，可用于将格式设置元素添加到纯文本文档中。  
Markdown 由[John Gruber](https://daringfireball.net/projects/markdown/)于2004年创建，如今已成为世界上最受欢迎的标记语言之一。

直观的来说，Markdown是`纯文本文件`，如果你用记事本打开我现在用的这个文档，所以它看上去大概是这个样子：

然而因为遵守了Markdown规范的文档，就可以被软件/网站等表示（或者称为渲染）成现在诸位看到的样子：

### 1.1. Markdown的特点

![overview](./images/overview.png)

- **功能强大**  
    可以创建网站、文档、便笺、书籍、演示文稿、电子邮件等等。
- **规则简单**  
    基本语法规则简单，大多数人可以快速上手
- **开放共享**
  - 没有版权限制
  - 没有操作系统限制
  - 可以直接在版本管理工具中进行Diff/Merge等操作
- **应用广泛**
  - GitHub、Stack Overflow、Reddit等网站
  - VSCode、IDEA、Eclipse等IDE
  - 软件
    - Mac：MacDown、iA Writer、Marked、...
    - Windows：Ghostwriter或Markdown Monster、...
    - iOS/Android：iA Writer、...
    - Linux：ReText、...

### 1.2. Markdown vs 各路英豪

```

然而因为遵守了Markdown规范的文档，就可以被软件/网站等表示（或者称为渲染）成现在诸位看到的样子：

### 1.1. Markdown的特点

![overview](./images/overview.png)

- **功能强大**  
    可以创建网站、文档、便笺、书籍、演示文稿、电子邮件等等。
- **规则简单**  
    基本语法规则简单，大多数人可以快速上手
- **开放共享**
  - 没有版权限制
  - 没有操作系统限制
  - 可以直接在版本管理工具中进行Diff/Merge等操作
- **应用广泛**
  - GitHub、Stack Overflow、Reddit等网站
  - VSCode、IDEA、Eclipse等IDE
  - 软件
    - Mac：MacDown、iA Writer、Marked、...
    - Windows：Ghostwriter或Markdown Monster、...
    - iOS/Android：iA Writer、...
    - Linux：ReText、...

### 1.2. Markdown vs 各路英豪

可能诸位有这些疑问：

> 我已经有MS Office Word了，为什么还要用Markdown？  
> PDF文件不好吗？为啥用Markdown？  
> 同样是标记语言Markdown比HTML区别在哪里？  

- Markdown vs MS Office Word、PDF
  - 优势
    - 不依赖付费软件。
    - 应用范围更广泛
    - 结构简单，体积小巧
    - 不会被病毒利用
    - 没有不同版本间的兼容问题。
  - 弱势
    - 排版功能不如Word、PDF强大
    - 本地图片需要额外保存，不能和文档一同处理。
- Markdown vs HTML
  - 应用范围不一样
  - Markdown可以轻松转换成Html，甚至通过一些插件在浏览器里直接打开。

### 1.3. 编辑方式

由于本身就是纯文本文件，所有的文本编辑器都可以轻松编辑Markdown文件。
而且主流的软件开发IDE更是通过插件的方式，提供了渲染等更高级的功能。
如：IDEA、Eclipse、VSCode等。
下面以VSCode为例，看看如何通过插件扩展VSCode的Markdown支持。

#### 1.3.1. VSCode + MPE

VSCode中增强Markdown功能的插件很多，其中目前最有名的，当属插件`shd101wyy.markdown-preview-enhanced`(简称：MPE)。

MPE插件：  
![mpe](./images/mpe.png)

安装后，可以通过右上角插件提供的渲染视图查看Markdown文档。
修改Markdown文件时，渲染视图会实时联动。  
![mpe-veiw](./images/mpe-view.png)

在渲染视图上右击，可以将渲染好的Markdown文件保存成PDF等其他格式的文件。
![mpe-veiw](./images/mpe-saveas.png)

MPE插件还提供了很多酷炫的markdown功能。详细内容可以参考 [3. 功能增强插件](#3-功能增强插件 )。

### 1.4. 使用方式

Markdown的应用非常广泛，但是在云应用流行的今天，最常用的莫过于利用其方便的格式控制能力。在网站上快捷方便的控制文字的格式，自动生成网页等。
支持Markdown格式控制的网站数不胜数。这里简单介绍两个。

#### 1.4.1 Gitlab

代码托管网站，大多都原生支持Markdown文件作为项目的介绍文档。
几乎所有的这类网站，默认都将项目根目录下的`README.md`作为项目的介绍文档。默认作为项目的主页展示。
这些网站包括：[Github](http://github.com)、[Gitlab.com](https://about.gitlab.com/)、[Gitblit](http://gitblit.github.io/gitblit/)、[Gitee](https://gitee.com/)等等。

这里以Gitlab为例：

在项目的根目录生成`README.md`的文件。
并将本文的内容拷贝进去。

- 在项目的主页面，Gitlab会直接根据`README.md`的内容生成项目介绍页面：  
    ![Gitlab](./images/gitlab.png)
- 在输入文字的界面（如Commit说明、Merge Request说明、issus说明等）也都支持Markdown  
    ![Gitlab-commit1](./images/gitlab-commit1.png)  
    ![Gitlab-commit2](./images/gitlab-commit2.png)  
    ![Gitlab-commit3](./images/gitlab-commit3.png)

#### 1.4.2 Redmine

Redmine作为项目管理网站，也是目前软件项目管理的当红明星。
如果你使用Markdown记录项目文档，在Redmine中打开也可以直接展示。

![redmine](./images/redmine.png)

## 2. 基础语法

Markdown之所以能够风靡世界，最重要的原因还是其基本规则非常简单。  
在扩展名上，通常Markdown采用`.md`或者`.markdown`作为扩展名。  
在内容上Markdown文本的书写遵照下述格式要求：

### 2.1. 标题

Markdown中使用`#`符号（后跟半角空格）标记文章的标题。几级标题就使用几个`#`号。
如图：

![标题](./images/title.png)

> 有些功能在Markdown中的实现方法不止一种。  
例如：一、二标题级别也可以用下一行接续```-----```和```======```来实现，这里不一一介绍。  
有兴趣可以参考网络上大量的相关文档。  
如：[Markdown百度百科](https://baike.baidu.com/item/markdown/3245829?fr=aladdin)

### 2.2. 段落

段落的规则有三点：

- 一般文字直接书写
- 段内换行：上行结尾加两个半角空格
- 另起一段：单独的空行

在Markdown中，普通文字直接书写。  
在段落之中如果需要另起一行，除了正常的换行之外，在上一行的末尾要添加两个半角空格。

如果要像现在这样创建一个新的段落，两段文字中间留一个空行。
> 注意：空行中不要有空格/tab等任何字符。  

- 示例：

    ```markdown
    一行文字，注意本行最末尾以两个半角空格结尾。  
    另起一行。本行结尾没有两个空格，会和下一行合并显示。
    下一行文字。

    另起一段，我是一个新的段落。
    ```

- 效果：  
    一行文字，注意本行最末尾以两个半角空格结尾。  
    另起一行。本行结尾没有两个空格，会和下一行合并显示。
    下一行文字。

    另起一段，我是一个新的段落。

### 2.2.1. 斜体

用`*`围起要用斜体表示的文字。

- 示例：

    ```markdown
    用*斜体*表示强调效果
    ```

- 效果：  
    用*斜体*表示强调效果

> 除了`*`之外，还可以用下划线`_`。

### 2.2.2. 粗体

用`**`围起要用粗体表示的文字。

- 示例：

    ```markdown
    用**粗体**表示强调效果
    ```

- 效果：  
    用**粗体**表示强调效果

> 除了`**`之外，还可以用双下划线`__`。

### 2.2.3. 粗斜体

用`***`围起要用粗斜体表示的文字。

- 示例：

    ```markdown
    用***粗斜体***表示强调效果
    ```

- 效果：  
    用***粗斜体***表示强调效果

> 除了`***`之外，还可以用三下划线`___`。

### 2.2.4. 通常强调

除了用字体变化表示外，Markdown还定义了一个通用的强调效果。
该效果的显示方式不同的软件的展示方法不完全一致，但是都是表示强调的效果。
使用方法上，用 **\`** 围起相应的文字即可。

- 示例：

    ```markdown
    这是`通常强调`的效果
    ```

- 效果：  
    这是`通常强调`的效果

### 2.2.5. 转义

想表示特殊字符的时候使用反斜线进行转义。

- 示例：

    ```markdown
    \# 虽然使用了“#”，但本行文字不是标题
    ```

- 效果：  
    \# 虽然使用了“#”，但本行文字不是标题

### 2.3. 列表

Markdown定义了两种列表：

- 有序列表
- 无序列表

#### 2.3.1. 有序列表

**有序列表**用`1.`开头（后面跟半角空格）如：

- 示例：

    ```markdown
    1. 阶段1
    1. 阶段2
        1. 步骤1
        1. 步骤2
        1. 步骤3
        1. 步骤4
    1. 阶段3
        1. 步骤1
        1. 步骤2
    1. 阶段4
    1. 阶段5
    ```

- 效果：  
    1. 阶段1
    1. 阶段2
        1. 步骤1
        1. 步骤2
        1. 步骤3
        1. 步骤4
    1. 阶段3
        1. 步骤1
        1. 步骤2
    1. 阶段4
    1. 阶段5

> 不必自行增加编号，渲染软件会自动编号。

#### 2.3.1. 无序列表

无序列表用`-`开头（后面跟半角空格）其余规则跟有序列表完全一致。如：

- 示例：

    ```markdown
    
    - 四季
      - 春
      - 夏
      - 秋
      - 冬
    - 星期
      - 星期日
      - 星期一
      - 星期二
      - 星期三
      - 星期四
      - 星期五
      - 星期六
    
    ```

- 效果：  
  - 四季
    - 春
    - 夏
    - 秋
    - 冬
  - 星期
    - 星期日
    - 星期一
    - 星期二
    - 星期三
    - 星期四
    - 星期五
    - 星期六

> 无序列表的引导标记也可以使用`+`或者`*`，但不推荐在一篇文章内混合使用。

### 2.4. 引用

用`>`表示引言、补充说明等。

- 示例：

    ```markdown
    鲁迅曾经说过：
    > 希望是附丽于存在的，有存在，便有希望，有希望，便是光明。
    ```

- 效果：  

    鲁迅曾经说过：
    > 希望是附丽于存在的，有存在，便有希望，有希望，便是光明。

引用是可以嵌套的：

- 示例：

    ```markdown
    前面写到：
    > 鲁迅曾经说过：
    >> 希望是附丽于存在的，有存在，便有希望，有希望，便是光明。
    ```

- 效果：  
    前面写到：
    > 鲁迅曾经说过：
    >> 希望是附丽于存在的，有存在，便有希望，有希望，便是光明。

### 2.5. 代码块

像源代码之类，需要原样展示，不需要进行解释的内容，可以使用代码块功能。
即将内容围在两组连续的\`\`\`符号之间
代码块后面可以跟随相应语言的名称，例如Java，在支持的软件中，会利用颜色字体等对关键字进行强调处理。

- 示例：  
    ![method](./images/method.png)
- 效果：  

    ```java
    System.out.println("Hello Markdown!");
    ```

### 2.6. 链接

使用```[标题](链接地址)```的格式，就可以实现超链接：

- 示例：

    ```markdown
    [大连华信](https://www.dhc.com.cn)
    ```

- 效果：  
    [大连华信](https://www.dhc.com.cn)

### 2.7. 图片

图片的格式和链接非常相似，图片的开头要多加一个半角惊叹号：```![标题](链接地址)```

- 示例：

    ```markdown
    ![大连华信25周年](http://pmo2845ee.hkpic1.websiteonline.cn/upload/banner4_7son.jpg)
    ```

- 效果：  
    ![大连华信25周年](http://pmo2845ee.hkpic1.websiteonline.cn/upload/banner4_7son.jpg)

### 2.8. 表格

在Markdown中表示表格也是很方便的。
一个完整的表格例子如下：

- 示例：

    ```markdown
    
    | 姓名 | 性别 | 工作 |
    | :--- | ---: | :---: |
    | 左对齐内容 | 右对齐内容 | 居中内容 |
    | 唐僧 | 男 | 西天取经团队领导 |
    | 孙悟空 | 男 | 护送唐僧 |
    | 猪八戒 | 男 | 同上 |
    | 沙僧 | 男 | 同上 |
    
    ```

- 效果：

    | 姓名 | 性别 | 工作 |
    | :--- | ---: | :---: |
    | 左对齐内容 | 右对齐内容 | 居中内容 |
    | 唐僧 | 男 | 西天取经团队领导 |
    | 孙悟空 | 男 | 护送唐僧 |
    | 猪八戒 | 男 | 同上 |
    | 沙僧 | 男 | 同上 |

Markdown中的表格使用`|`分割不同字段之间的内容。
Markdown表格依次分成`表头`、`对齐方式`、`内容`三部分。

第一行固定为`表头`，是表格的标题：

```markdown
| 姓名 | 性别 | 工作 |
```

第二行负责控制后面内容的`对齐方式`：

- 左对齐：`:---`
- 右对齐：`---:`
- 居中对齐：`:---:`

```markdown
| :--- | ---: | :---: |
```

> 其中的`---`不一定必须是三个，可以是一个或多个都可以。表格各列之间也不必一致。（但如果保持一致看上去一般更美观）

从第三行开始是实际的表格`内容`：

```markdown
|左对齐内容 | 右对齐内容 | 居中内容 |
| 唐僧 | 男 | 西天取经团队领导 |
| 孙悟空 | 男 | 护送唐僧 |
| 猪八戒 | 男 | 同上 |
| 沙僧 | 男 | 同上 |
```

## 3. 功能增强插件

前面介绍的内容，都是Markdown的基础功能。  
基本上在所有支持Markdown的软件/网站等环境中，都可以支持。  
但是作为程序员，面对Markdown这么优秀的基础，自然是不满足于基本的功能的。  
于是乎各路高手折腾出各种各样优秀的扩展功能，其中一些佼佼者，已经被大多数Markdown环境所吸收，使用这些扩展功能，可以给你的Markdown文档带来令人惊叹的强大功能。  
这里简单挑几个跟我们日常工作关联较大的，略加介绍。

### 3.1. 作图

Markdown的作图增强语法插件有很多，最著名的有[Mermaid](https://mermaid-js.github.io/mermaid/#/)、[Sequence](https://bramp.github.io/js-sequence-diagrams/)和[Flow](https://flowchart.js.org/)。  
下面以Mermaid为例，简单显示几个作图的例子。

#### 3.1.1. Mermaid

[Mermaid](https://mermaid-js.github.io/mermaid/#/)是一个基于Javascript的图表和图表工具，可以呈现基于Markdown的文本定义来动态地创建和修改图表。  
它允许您使用文本和代码创建图表，简化了复杂图表的维护。  

- 流程图

    ```mermaid
    graph LR
        A[方形] -->B(圆角)
        B --> C{条件a}
        C -->|a=1| D[结果1]
        C -->|a=2| E[结果2]
        C -->|a=3| F[结果3]
        Z[横向流程图]
    ```

- 时序图

    ```mermaid
    sequenceDiagram
        autonumber
        Alice->>John: Hello John, how are you?
        loop Healthcheck
            John->>John: Fight against hypochondria
        end
        Note right of John: Rational thoughts!
        John-->>Alice: Great!
        John->>Bob: How about you?
        Bob-->>John: Jolly good!
    ```

- 甘特图

    ```mermaid
            gantt
            dateFormat  YYYY-MM-DD
            title 软件开发甘特图
            section 设计
            需求                      :done,    des1, 2021-01-06,2021-01-08
            原型                      :active,  des2, 2021-01-09, 3d
            UI设计                     :         des3, after des2, 5d
            UE设计                     :         des4, after des3, 5d
            section 开发
            需求理解                             :crit, done, 2021-01-06,24h
            框架设计                             :crit, done, after des2, 2d
            Source开发                                 :crit, active, 3d
            紧急任务                              :crit, 5d
            大数据平台                                   :2d
            section 测试
            功能测试                              :active, a1, after des3, 3d
            压力测试                               :after a1  , 48h
            测试报告                               : 8h
    ```

### 3.1.2. Markdown自动生成图片的优势

实际使用中最方便的是，简单的修改Markdown的文本，图中相应的内容就可以实时跟随变化。  
如下图，不管是增加元素还是调整流程图的方向，右侧的图片都实时做出了反应。  
![实时更新的图](./images/change.gif)

### 3.2. TOC

在文章的开头生成整篇文章的索引可以有助于读者快速了解文章的主要脉络，并快速定位到自己需要的内容。  
但是手动维护目录是一件费时费力还不讨好的工作。有幸的是VSCode插件`alanwalk.markdown-toc`可以帮助我们快速自动的实现这个过程。

- 使用方法
  1. 在VSCode中安装TOC插件
      ![TOC-plugin](./images/toc-plugin.png)
  1. 在希望插入目录的位置单独一行输入：`[TOC]`
- 效果  
    ![toc](./images/toc.png)

### 3.3. 数学公式

部分Markdown软件（例如MPE）支持自动转换数学公式。

- $f(x) = sin(x)/3π$
- $$ f(x,y) = \sum_{n=1}^{100} sin(2πnx)+cos(πny)+ß $$

动态过程参考：
![数学公式](https://cloud.githubusercontent.com/assets/1908863/14398210/0e408954-fda8-11e5-9eb4-562d7c0ca431.gif)

## 4. 参考资料

- [Markdown中文网](http://markdown.p2hp.com/index.html)
- [百度百科-markdown](https://baike.baidu.com/item/markdown/3245829?fr=aladdin)
- [Github](http://github.com)
- [Stack Overflow](https://stackoverflow.com/)
- [Gitlab.com](https://about.gitlab.com/)
- [Gitblit](http://gitblit.github.io/gitblit/)
- [Gitee](https://gitee.com/)
- [VSCode](https://code.visualstudio.com/)
- [VSCode MPE插件](https://shd101wyy.github.io/markdown-preview-enhanced/#/)
- [mermaid](https://mermaid-js.github.io/mermaid/#/)
- [Sequence](https://bramp.github.io/js-sequence-diagrams/)
- [Flow](https://flowchart.js.org/)
