# 【建设LaTeX史上最宏伟的中文FAQ工程，见证我们LaTeX中文社区的新生力量，大家是历史创造者。】

**更新前请仔细阅读：**
1. **大家不要刷格式##，可以微调，主要完成内容更新，格式我们后期集中调整。**
2. **一级标题已经设置好了，二级标题大家可以采用序号的方式进行编号。**
3. **每周末，根据编辑历史，没有内容贡献的用户，将取消其权限并移出群。**
4. **感谢大家的参与，** **请大家加入我们的微信群！方便大家沟通！（协作平台与微信名片统一，便于清理和沟通）**

![图片](../images/weixin.jpg)
**模块冠名（按照各个模块更新贡献多少，观其量，冠其名）**

|**模块**|冠名|**备注**|
|:----:|:----:|:----:|
| | |
| | |
| | |
| | |
| | |
| | |
| | |


## 一、背景知识与基本概念

### 1. 什么是TeX？

TeX是由著名的计算机科学家 [Donald E. Knuth](https://www-cs-faculty.stanford.edu/~knuth/)（高德纳）发明的排版系统，他在他的书的前言中曾提到「TeX旨在创造美丽的书籍，特别是那些包含很多数学公式的书」。（如果说TeX仅仅是为了更方便些数学方面的书而生的，那么它就不会像今天这么使用广泛了：事实上，TeX是一个很好的文字排版工具）。
Knuth是美国加州斯坦福大学计算机编程专业的名誉教授，他在1978年开发了第一个版本的TeX用来处理他的“计算机编程艺术”的修订。这个想法特别受欢迎，所以1982年他推出了TeX的第二个版本，也就是们今天所用的TeX的基础。
Knuth开发了一套“识字编程”来编写TeX，他还提供了免费的TeX资源，以及可以将网络资源转化为可以编译或者打印的东西的工具；Knuth做了什么，对人们来说从来都不是什么神秘的事情。TeX以及它的文档都是高度可移植的。
对于感兴趣的程序员来说，TeX有其迷人之处：没有什么能比得上一个人可以构建这样一个程序，至今它的持续时间比大多数的程序都好，而且已经被移植到了许多不同的计算机构架和操作系统中——许多现代编程所追求的属性。经过处理的“可读”的TeX程序源代码可以在 [TDS structured](https://texfaq.org/FAQ-tds) 版本中找到。

### 2. TeX 中常见术语的解释
* **引擎**

LaTeX/TeX解析引擎，其实就是一个编译器，它输入一个.tex文件作为输入，根据源文件的内容送入解析引擎和渲染引擎进行处理，并将排版的成果——文档编译输出，LaTeX/TeX的解析引擎目前有pdflatex、xelatex、lualatex等，它们都可以输出pdf文档文件（部分解析器可以输出dvi文件），用于在多平台进行分发甚至打印出版。
* **格式**

TeX是存在各种不同的封装格式的，比如原生的TeX或者LaTeX，我们所使用的LaTeX只是tex封装格式的其中一种，是目前流行的封装规范。
* **发行版**

 LaTeX/TeX都包含了成千上万个宏包，甚至有可能我们需要安装新的宏包，除了手动安装外，最好的方式就是利用发行版的宏包管理器，所谓发行版就是把LaTeX/TeX的相关组件打包，形成一个独立完善的LaTeX/TeX系统，目前流行的发行版有MiKTeX、proTeXt 以及TeXLive。

### 3. 不同的TeX封装格式的区别？
* **原生TeX**

TeX本身是一个基于控制序列的排版系统，它指示TeX如何在页面上放置文本。例如，\hskip指在文档中在文档中插入一定数量的水平空间，而\font是指给文档中的文字定义一种给定的字体。TeX是完全可编程的，它使用一种集成的宏脚本语言，支持变量，范围，条件执行，控制流和函数定义等。
* **TeX宏包（TeX格式）**

TeX的一些控制序列直接使用是单调乏味的；它们主要作为更高层次的构建快，因此更易于用户使用。例如，在基础TeX中没有办法能够制定一段文字应该排版为更大的字体，相反，你必须了解当前的字体和大小，然后加载一种同样字体但更大字号的字体。幸运的是，TeX是可编程的，它可以通过写一个宏将这些复杂性都隐藏在一个简单的，新的控制序列之后。例如，我们可以通过 \larger{my text}将“my text”定义为比当前更大的字体。
一些使用者会写一些完全由自己定义的宏集，然后再一些文档中重复使用，但，常见的还是依赖于由专家编写的TeX宏包——一些宏的集合。为了方便用户，这些宏包通常与基本的TeX引擎结合到一个独立的可执行的文件中。

* **TeXLive、MacTeX、MikTeX、CTEX**

TeXLive 由类 UNIX 系统上的 teTeX 发展并取而代之，最终成为跨平台的 TeX 发行版。TeXLive 自 2011 年起以年份作为发行版的版本号，保持了一年一更的频率。
MacTeX 是 macOS（OS X）系统下的一个定制化的 TeXLive 版本，与 TeXLive 同步更新。
MikTeX 是主要用于 Windows 平台的一个稳定发展的 TeX 发行版，目前已开发出跨平台版本。
中国的 LaTeX 用户应该对“CTeX 套装”比较熟悉，它是一个经过本地化配置的MikTeX，目前已不推荐使用。
### 4. TeX有哪些不同的封装格式

TeX是一种排版文件的计算机程序，它需要一个计算机文件，根据TeX的规则进行准备，并将其转换成一种可以在高质量打印机上打印的形式，比如激光打印机，可以打印出一份与高质量的书籍和期刊相媲美的打印文档。不包含数学公式或表格的简单文档可以很容易就生成，事实上，所有人都必须直接输入文本（只是遵循不同的符号规则）。输入数学公式时比较复杂的，但当考虑到产生一些数学公式的复杂性时，TeX是相对容易使用的，它可以产生大量的数学符号。
TeX包括各种不同的“方言”，其中包括LaTeX。Plain TeX是TeX中最基础的版本，也是其他“方言”的基础。为了用TeX生成文档，我们必须首先在计算机上创建一个合适的输入文件，我们将TeX程序应用到输入文件中，然后再用打印机打印由TeX程序生成的所谓的“DVI”文件。

* **Plain TeX(TeX)**

Knuth设计了一个名叫PlainTeX的基本格式，以与低层次的原始TeX呼应。这种格式是用TeX处理文本时相当基本的部分，以致于我们有时都分不清到底哪条指令是真正的处理程序TeX的原始命令，哪条是PlainTeX格式的。大多数声称只使用TeX的人，实际上指的是只用PlainTeX。
PlainTeX也是其它格式的基础，这进一步加深了很多人认为TeX和PlainTeX是同一事物的印象。
PlainTeX的重点还只是在于如何排版的层次上，而不是从一位作者的观点出发。对它的深层功能的进一步发掘，需要相当丰富的编程技巧。因此它的应用就局限于高级排版和程序设计人员。
注：有关Plain TeX的相关信息可见：[http://www.ntg.nl/doc/wilkins/pllong.pdf](http://www.ntg.nl/doc/wilkins/pllong.pdf)

* **LaTeX(latex)**

有两个版本，分别是LaTeX2e和LaTeX2.09，前者是当前使用的版本，后者是1994年最开使用的过时的版本。
[LeslieLamport](https://baike.sogou.com/lemma/ShowInnerLink.htm?lemmaId=73792246&ss_c=ssc.citiao.link)开发的LaTeX是当今世界上最流行和使用最为广泛的TeX格式。它构筑在PlainTeX的基础之上，并加进了很多的功能以使得使用者可以更为方便的利用TeX的强大功能。使用LaTeX基本上不需要使用者自己设计命令和宏等，因为LaTeX已经替你做好了。因此，即使使用者并不是很了解TeX，也可以在短短的时间内生成高质量的文档。对于生成复杂的数学公式，LaTeX表现的更为出色。
LaTeX自从二十世纪八十年代初问世以来，也在不断的发展。最初的正式版本为2.09，在经过几年的发展之后，许多新的功能，机制被引入到LaTeX中。在享受这些新功能带来的便利的同时，它所伴随的副作用也开始显现，这就是不兼容性。标准的LaTeX2.09，引入了“新字体选择框架”(NFSS)的LaTeX，SLiTeX，AMSLaTeX等等，相互之间并不兼容。这给使用者和维护者都带来很大的麻烦。
为结束这种糟糕的状况，Frank Mittelbach等人成立了LaTeX3项目小组，目标是建立一个最优的，有效的，统一的，标准的命令集合。即得到LaTeX的一个新版本3。这是一个长期目标，向这个目标迈出第一步就是在1994年发布的LaTeX2e。LaTeX2e采用了NFSS作为标准，加入了很多新的功能，同时还兼容旧的LaTeX2.09。LaTeX2e每6个月更新一次，修正发现的错误并加入一些新的功能。在LaTeX3p最终完成之前，LaTeX2e将是标准的LaTeX版本。
* **ConTeXt(context)**

ConTeXt是TeX的一种格式，是Hans Hagen和荷兰Pragma-ADE公司设计的一种高端的文档制造工具，官方网站为 [ConTeXtGarden](http://wiki.contextgarden.net/Main_Page)。ConTeXt就像LaTeX是基于TeX排班系统的文档制作系统，如果说LaTeX将作者从排版的细节中隔离出来，那么ConTeXt就是采用一种互补的方法来处理结构化的界面来处理排版，包括对颜色、背景、超链接、演示文稿、图形文本集成和条件编译的广泛支持， 对于数学、化学等科技文档的支持同等优秀甚至更为方便，而且其为了更容易实现各种华丽排版效果。它可以让用户对格式进行广泛的控制，同时又可以在不需要学习TeX宏语言的情况下轻松地创建新的布局和样式。 因此ConTeX的图形功能要远远强于TeX和LaTeX，可以制作非常漂亮的PD文档，特别适合做幻灯片和一些非正式的文档。
ConTeXt将MetaFun，MetaPost的超集以及一个强大的矢量图形系统整合起来。MetaFun可以作为一个独立的系7统来生成数据，但是它的优势在于用精确的图形元素来增强ConTeXt文档。
目前，ConTeXt主要分为两个版本，分别是Mark Ⅱ—后缀名为mkii，在pdfTeX上运行但不是主动开发阶段；和Mark Ⅳ—后缀名为mkiv，在LuaTeX上运行而且正在开发阶段。（LuaTeX的发展也是由于ConTeXt驱动）。
注：CTAN不支持ConTeXt的发布——潜在的用户可以去 [ConTeXt Garden](http://wiki.contextgarden.net/Main_Page)了解当前发行版的详细信息。

* **TeXinfo(TeX,makeinfo)**

TeXinfo是一个使用同一个源文件生成在线信息和打印输出的文档系统，所以只需要编写一个文档源文件，当工作被修改时，只需要修改源文件即可。其源文件的后缀名为texi或texinfo。
TeXinfo是一门宏语言，就像LaTeX一样，但是它的表达能力略弱，它的表观与TeX的其他宏语言相似，只不过它的宏要以@开头，而TeX系统中用\开头。
你可以在GNU Emacs中编写以及将TeXinfo文件转化成info文件，你也可以在makeinfo中将TeXinfo文件转换成info文件，然后再info中阅读，所以也不是必须依赖于Emacs。这个发行版包括一个Perl脚本，texi2html，可以将texinfo文件转换成HTML，这种语言比LaTeX更适合HTML，所以将LaTeX转换成HTML的痛苦就可以避免了。
当然，你也可以用pdfTeX将输入文件转换成PDF格式。
makeinfo可将texinfo文档转换成HTML，DocBook,，Emacs info,，XML和全文本。TeX（或者texi2dvi和texi2pdf），因为TeX加载了普通的TeX宏，而并不是TeXinfo，所以TeXinfo文档必须以“\input texinfo”开头来加载texinfo包。
* **Eplain(eplain)**

Eplain扩展并延伸了Plain TeX的定义，它并不像ConTeX 

### 5. LaTeX2.09和LaTeX2e有什么区别？

后者是前者的改进，从文件内容上看，两者最显著的不同在于LaTeX2.09使用\documentstyle命令定义文档类型以及所包含宏包，如

```
\documentstyle[twoside,epsfig]{article}
```
而LaTeX2e使用\documentclass命令设置文档类型，用\usepackage命令调用宏包。

### 6. Tex, LaTex, pdflatex, xelatex, xetex等的区别和关系，什么时候用什么编译器编译

LaTeX 其实是目前使用最广泛的 TeX 格式。xeTeX 是一种引擎（编译器），pdfLaTeX （xeLaTeX） 是命令，他们分别结合了 pdfTeX（xeTeX） 引擎和 LaTeX 格式。对于刚开始接触的人，建议处理英文时直接使用 pdfLaTeX，处理非英文时使用 XeLaTeX（并且用utf-8编码源文件） 

### 7. 文本文件编码解读

### 8. LaTeX源文件

LaTeX的源文件是*.tex文件，是指latex编译器处理输入文件的源码，latex编译器会对输入文件进行解析，构造解析树，进行渲染，然后输出处理后的文档，完成一次编译过程，由于LaTeX解析器可能对中文文件名处理存在兼容性问题，不建议将LaTeX的源文件的文件名设置为中文。
### 9. 连字符如何在TeX起作用

如果 LaTeX 遇到了很长的英文单词，仅在单词之间的位置断行无法生成宽度匀称的行时，就要考虑从单词中间断开。对于绝大部分单词，LaTeX 能够找到合适的断词位置，在断开的行尾加上连字符 - 。
如果一些单词没能自动断词，我们可以在单词内手动使用 \- 命令指定断词的位置，如：
I think this is: su\-per\-cal\-%
i\-frag\-i\-lis\-tic\-ex\-pi\-%
al\-i\-do\-cious.

### 10. Unicode和TeX

### 11. 常见的TeX文件扩展名与文件用途

常见的用户文件的扩展名与其用户如下：
  * .tex 文件。源文件，需用户编写。
  * .sty 宏包文件。宏包的名称就是去掉扩展名的文件名。
  * .cls 文档类文件。同样地，文档类名称就是文件名
  * .bib BibTeX 参考文献数据库文件。
  * .bst BibTeX 用到的参考文献格式模板。
  * .log 排版引擎生成的日志文件，供排查错误使用。
  * .aux LaTeX 生成的主辅助文件，记录交叉引用、目录、参考文献的引用等。
  * .toc LaTeX 生成的目录记录文件。
  * .lof LaTeX 生成的图片目录记录文件。
  * .lot LaTeX 生成的表格目录记录文件。
  * .bbl BibTeX 生成的参考文献记录文件。
  * .blg BibTeX 生成的日志文件。
  * .idx LaTeX 生成的供 makeindex 处理的索引记录文件。
  * .ind makeindex 处理 .idx 生成的格式化索引记录文件。
  * .ilg makeindex 生成的日志文件。
  * .out hyperref 宏包生成的 PDF 书签记录文件。
### 12. 什么是“决议”(resolutions)

### 13. 什么是（TeX）宏

### 14. 什么是LaTeX环境

### 15. 什么是LaTeX类和工具包

### 16. 什么是PK文件

### 17. 什么是TFM文件

### 18. 什么是编码

### 19. 什么是EC字体

### 20. 什么是虚拟字体

### 21. 什么是“Encapsulated PostScript”(EPS)

### 22. 什么是DVI驱动程序

### 23. 什么是DVI文件

DVI文件（device independent）为[TeX](https://baike.baidu.com/item/TeX)电子排版系统的输出文件。七十年代末，[Donald E. Knuth](https://baike.baidu.com/item/Donald%20E.%20Knuth)（高德纳）在看到其多卷巨著“The Art of ComputerProgramming”第二卷的校样时，对由计算机排版的校样的低质量感到无法忍受。因此决定自己来开发一个高质量的计算机排版系统，这样就有了TeX。TeX 的输出文件称为 DVI 文件，即是“Device Independent”。一旦 TeX 处理了你的文件，你所得到的 DVI文件就可以被送到任何[输出设备](https://baike.baidu.com/item/%E8%BE%93%E5%87%BA%E8%AE%BE%E5%A4%87)如打印机，屏幕等并且总会得到相同的结果，而这与这些输出设备的限制没有任何关系。这说明 DVI 文件中所有的元素，从页面设置到文本中字符的位置都被固定，不能更改。
### 24. 什么是“Berry命名方案”

### 25. 什么是TDS

TDS 全称 TeX Directory Structure，意为 TeX 目录结构，即 TeX 发行版的文件组织结构。大部分 TeX 发行版都将自身的文件组织成相近的路径结构，也就是 TDS。TDS 也称为 TEXMF 树，这是 TeX 与 METAFONT 的合称。很多系统的 TDS 结构都以 `texmf` 或者类似的词作为 TEXMF 树的根目录名，如在 TeX Live 中，安装目录下的 `texmf-dist`、`texmf-var` 等就是两个不同的 TEXMF 树。

下面是 TeX Live 中 `texmf-dist` 下的目录结构（有所删节，同时根据安装情况可能有所出入）：

```
bibtex/                     BibTeX 相关文件    bib/                        公用 bib 数据库
    bst/                        格式文件
doc/                        各类用户文档
    bibtex/                     BibTeX 相关文档
    fonts/                      字体文档
    generic/                    通用于各种格式的文档
        pgf/
            pgfmanual.pdf           PGF/TikZ 用户手册
            ...
        ...
    latex/                      用于 LaTeX 格式的文档
        ctex/
            ctex.pdf                ctex 宏集用户手册
            README.md               ctex 宏集简短介绍
        ...
    texlive/                    TeX Live 发行版自身的文档
    ...
fonts/                          字体相关文件
    opentype/                       OpenType 格式的字体
    source/                         字体源代码
    truetype/                       TrueType 格式的字体
    type1/                          Type1 格式的字体
    .../
scripts/                        可执行脚本
    l3build/                        LaTeX 构建、测试脚本
    latexmk/                        自动编译系统
    texdoc/                         文档查询系统
    ...
source/                         源代码
    bibtex/                         BibTeX 相关宏包代码
    fonts/                          字体源代码
    generic/                        通用于各种格式的宏包代码
    latex/                          用于 LaTeX 格式的宏包代码
        ctex/                           ctex 宏集源代码
            ctex.dtx
            ctex.ins
            ctexpuct.spa
        ...
    ...
tex/                            TeX 宏，可被引擎读入
    generic/                        通用于各种格式
    latex/                          用于 LaTeX 格式
        base/                           LaTeX 的基本宏文件
            article.cls
            book.cls
            report.cls
            latex.ltx
            ...
        beamer/                         beamer 宏包相关文件
        ctex/                           ctex 宏集相关文件
            ctexart.cls
            ctexbeamer.cls
            ctexbook.cls
            ctexrep.cls
            ctex.sty
            ...
        ...
    plain/                          用于 Plain TeX 格式
    xetex/                          用于 XeTeX 引擎
    xelatex/                        用于 XeTeX 引擎下的 LaTeX 格式
        xecjk/                          xeCJK 宏包相关文件
            xeCJK.sty
            ...
    ...
...
```

（来自刘海洋《LaTeX 入门》）

### 26. 从TeX编写（文本）文件

### 27. \special命令

### 28. Overleaf是什么？如何使用？

~~【这个答案严重误导！急需修订！】~~~~首先，经常使用的~~~~ ~~~~minted~~~~ ~~~~宏包不可使用，一般对~~~~ ~~~~lstlisting~~~~ ~~~~环境进行配置，比如MATLAB的配置可以参考~~[网址](http://www.latexstudio.net/archives/7483.html)~~。其次，其上传文件的个数是有限制，并且不支持两层及以上的文件夹，如果要将书籍的章以及其下的节分文件夹储存，则结构不清晰。最后，overleaf v2暂时不稳定，本地有TeXLive最好在本地进行内容的编写。回答时间2018-08-10。~~

以上所述不准确。

Minted 在 Overleaf v1、v2 都是可以用的，例子参照 https://www.overleaf.com/read/qphhfvnsddbs。Matlab 高亮也一样可以用 minted 完成，注意字母大小写：\begin{minted}{matlab}

Overleaf v1 的确有文件数目及项目大小限制，视收费与否而定：[https://www.overleaf.com/help/297](https://www.overleaf.com/help/297)
Overleaf v2 则相对宽松得多：所有项目（包括免费）都无文件大小上限，条件：每个项目限2000文件，以及可编辑纯文本文件不大于 5MB。详见[https://www.sharelatex.com/learn/Uploading_a_project#Limitations_on_Uploads](https://www.sharelatex.com/learn/Uploading_a_project#Limitations_on_Uploads)

Overleaf v1 是支持两层及以上的文件夹的，详情看 [https://www.overleaf.com/help/187](https://www.overleaf.com/help/187)
Overleaf v2 可以直接右键资料夹，再创建子资料夹。

Overleaf v2 目前还是比较稳定的（2018年9月将会全面上线）。当然如果是特定地区、单位限制的原因，则不方便在这里讨论。

【这里先预定个位置，以后可以写个篇幅比较长的功能介绍。若对 Overleaf 有任何问题，建议直接电邮 support@overleaf.com 询问，不必过多自行揣测。若是担心语言问题，Overleaf 技术支援人员有谙中文的。】

### 29. 编译器与编辑器的区别是什么

在 lshort-zh 中，确切解释了，所谓编译器，真正的名称叫排版引擎，是读入源代码并编译生成文档的程序，如 pdfTeX、XeTeX 等。
编辑器，其实是用户书写源代码的工具，例如 windows 下的记事本、ubuntu 下的 gedit 等等。目前很多编辑器都提供了"编译“按钮，本质上是基于命令行调用了编译器。

### 30. 未来有计划做到像Bakoma那样所见即所得吗？ 

LaTeX 的缺点之一，相比“所见即所得”的模式有一些不便，为了查看生成的文档，用户总要不停地编译。  

## 二、安装与配置问题
### 31. 如何安装 LaTeX

很多用户所谓的如何安装 LaTeX，实际上是一个无解的问题，因为 LaTeX 不是一款软件，相关概念不再赘述。用户可以直接安装 LaTeX 发行版，如 proTeXt , TeXLive 和 MacTeX (TeXLive在MacOS 的一个再次发行版)。

### 32. 如何下载 proTeXt 安装包

访问以下链接即可
[http://mirror.ctan.org/systems/protext/protext.exe](http://mirror.ctan.org/systems/protext/protext.exe)

### 33. 如何下载 TeXlive 安装包

访问以下网址获取 texlive 安装包镜像文件：
[http://mirror.ctan.org/systems/texlive/Images/texlive.iso](http://mirror.ctan.org/systems/texlive/Images/texlive.iso)
MacTeX安装包下载地址：
[http://mirror.ctan.org/systems/mac/mactex/MacTeX.pkg](http://mirror.ctan.org/systems/mac/mactex/MacTeX.pkg)

### 34. 如何安装 TeXlive

TeXlive 为用户提供了官方安装手册，其中文版地址是：
[https://tug.org/texlive/doc/texlive-zh-cn/texlive-zh-cn.pdf](https://tug.org/texlive/doc/texlive-zh-cn/texlive-zh-cn.pdf)
建议有余力的用户通读手册，以了解更多内容。
也可以参照以下网址
[https://www.tug.org/texlive/quickinstall.html](https://www.tug.org/texlive/quickinstall.html)

### 35. 如何挂载镜像文件：

目前市面上有很多虚拟光驱软件可供用户选择，例如 UltraISO。
特别一提，在 windows 8、windows 10 操作系统中，默认被双击后，镜像文件将会直接挂载。
在 Linux 操作系统中，可使用命令行挂载镜像文件：
```
mount -o loop ~/Download/TeXlive.iso ~/iso
```
### 36. 挂载镜像文件后该如何做？

windows 用户可以双击 install-tl-windows.bat 文件来进行安装。
linux 用户请在命令行执行 ./install-tl 进入 no gui 安装模式

### 37. 双击 install-tl-windows.bat 出现错误怎么办？

使用命令行。同时按下 win 键和 R 键，打开“运行”窗口，在窗口的“打开”处，输入 cmd 打开命令行窗口（黑窗）。
在黑窗内输入
```
cd /d [~]
```
后按 enter 键（即执行该命令），此处 [~] 代指 install-tl-windows.bat 所在目录，例如 C:/Downloads 等，注意命令中的空格。
进入目录后继续执行
```
install-tl-windows.bat -no-gui
```
开启纯命令行安装模式。默认状态下，点击 I 键 ( HIJK 的 I)，安装便会开始。若用户想改变安装路径或其他设置，只需根据屏幕提示进行更改即可。特别强调，安装路径一定是不带空格的纯英文路径。
### 38. 使用命令行安装TeXLive出现 goodbye 怎么办？

主要是缺少CMD所在的环境变量。
只需要在命令行中执行
```
path=%path%;C:\Windows\system32
```
后再尝试安装。或者因为下载文件损坏，上述方法不管用应重新下载。

### 39. 想在 linux 系统中使用 gui 模式安装该怎么做？

自行安装 perl，详细办法请上网自行搜索。然后执行命令
```
./install-tl -gui wizard  
```
或
```
./install-tl -gui perltk
```
### 40. 如何搭配 TeXLive 的环境变量？

Windows 用户一般不必担忧这个问题。因为 TeXLive 已经自动将环境变量写入，用户不必自己手动修改。
Linux 用户需要手动配置环境变量。例如，将
```
TEXDIR=/usr/local/texlive/2018
if [ -d $TEXDIR ]; then
  export PATH=$TEXDIR/bin/x86_64-linux;$PATH;
  export MANPATH=$TEXDIR/texmf-dist/doc/man;$MANPATH;
  export INFOPATH=$TEXDIR/texmf-dist/doc/info;$INFOPATH;
fi;
```
写入~/.profile。注意本例中的 2018 可以根据需要修改，例如部分用户还在使用 TeXLive 2017，就可将 2018 改为 2017等等。

### 41. 如何判断 TeXLive 安装成功？

在命令行中执行
```
tex -v
```
若命令行窗口中显示
TeXLive 2018
等内容，即说明安装成功。
### 42. 如何删除 TeXLive

windows 用户请找卸载批命令文件，如
C:\texlive\2018\tlpkg\installer\uninst.bat
linux 用户请直接删除文件夹，如执行
```
rm -rf /usr/local/texlive/2018
rm -rf ~/.texlive2018
```
并且手动清理环境变量

### 43. TeXLive 如何升级宏包？

建议使用命令行升级宏包。
首先指定源，执行命令
```
tlmgr option repository ctan
```
以自动寻求源，也可以手动指定源，例如执行命令
```
tlmgr option repository http://ftp.jaist.ac.jp/pub/CTAN/systems/texlive/tlnet
```
即指定了源为 http://ftp.jaist.ac.jp/pub/CTAN/systems/texlive/tlnet。
接下来，执行命令
```
tlmgr update --self
```
升级 tlmgr 本身。
然后，我们就可以升级宏包了。实际上，tlmgr 升级所有宏包的代码非常简单，执行命令
```
tlmgr update --all
```
值得一提的是，这样的做法也会同时删除本地的那些已被我们设定的源所剔除的宏包。如果用户想保留它们的话，可以执行
```
tlmgr update --all --no-auto-remove
```
但是 tlmgr 手册并不建议用户使用这样的方法。此外，为了防止更新后出现某些问题，我们还可以执行如下命令建立一个宏包备份：
```
tlmgr update --all --backup --backupdir E:\latexwork\backup
```
通过这句代码，我们就可以在更新宏包前将需要更新的宏包备份在 E:\latexwork\backup 中。一旦更新出现问题，我们可以执行
```
tlmgr restore --bakeupdir E:\latexwork\backup --all
```
来恢复全部宏包，或者我们也可以恢复某个宏包，如
```
tlmgr restore --bakeupdir E:\latexwork\backup mcmthesis
```
就可以用于恢复mcmthesis。
### 44. MikTeX 如何升级宏包

MikTeX 可以用界面升级宏包，有些用户经常升级失败是因为源不稳定造成的。建议到 [https://miktex.org/pkg/repositories](https://miktex.org/pkg/repositories) 找稳定的源。
### 45. TexLive对源的操作有哪些

查看源列表
```
tlmgr repository list
```
正常情况下，列表中至少有一个源地址，并且该源地址被标记为 main。
添加源
```
tlmgr repository add <path> [tag]
```
path 是源的地址，tag 是源的标签。例如添 http://ftp.jaist.ac.jp/pub/CTAN/systems/texlive/tlnet 并标记为 jp
```
tlmgr repository add http://ftp.jaist.ac.jp/pub/CTAN/systems/texlive/tlnet jp
```
标签可以省略
删除源
```
tlmgr repository remove path|tag
```
例如将刚才添加的 jp 删除
```
tlmgr repository remove jp
```
无视以前的列表，重新制定列表
```
tlmgr repository set path[#tag] [path[#tag] ...]
```
特别强调，TeXLive 要求源列表中至少存在一个被标记为 main 的源，否则一切操作都将失效。

### 46. 如何自动升级 TeXLive 宏包？

[这](http://pd10ibe5c.bkt.clouddn.com/TeXLive%E5%AE%8F%E5%8C%85%E6%AF%8F%E6%9C%88%E8%87%AA%E5%8A%A8%E6%9B%B4%E6%96%B0.zip)[里可以下载每月自动升级TeXLive宏包的脚本](http://pd10ibe5c.bkt.clouddn.com/TeXLive%E5%AE%8F%E5%8C%85%E6%AF%8F%E6%9C%88%E8%87%AA%E5%8A%A8%E6%9B%B4%E6%96%B0.zip)。
[这里是该脚本的说明](http://htharoldht.com/texlive-package-automatically-upgrades-every-month/)。
* 脚本源码
```
@echo off

if exist "C:\Windows\Tasks\AutoTeXLivePackageUpdaterMonthly.bat" goto run

move /y %0 "C:\Windows\Tasks"
schtasks /delete /tn "TeXLivePackage Updater Task" /f
schtasks /create /tn "TeXLivePackage Updater Task" /sc monthly /d /st 15:00:00 /tr "C:\Windows\Tasks\AutoTeXLivePackageUpdaterMonthly.bat"

:run
echo ============================开始============================
echo Writen By 有龙则灵_USTB

echo 是否更新TeXLive Package？
set Choice=
set /p Choice=请输入：y/n?
IF "%Choice%"=="y" (goto ya) else (goto n)

:ya
call tlmgr option repository http://mirror.ctan.org/systems/texlive/tlnet
echo ============================更新tlmgr============================
echo Writen By 有龙则灵_USTB
call tlmgr update --self
echo ============================显示待更新的宏包以及可自动安装的项============================
call tlmgr update --list
echo Writen By 有龙则灵_USTB

echo 是否更新TeXLive Package？
set Choice=
set /p Choice=请输入：y/n?
IF "%Choice%"=="y" (goto yb) else (goto n)

:yb
echo ============================更新所有宏包============================
call tlmgr update --all
echo ============================结束============================
echo Writen By 有龙则灵_USTB
pause
:n
```
* 脚本阐释
  * 利用 Windows 自带的 SchTasks 创建定时任务

第一部分用于将该脚本移动到定时任务的根目录，并创建一个计划任务项。
为什么不用 AT 呢？因为 AT 在 Win10 中已经被取缔了。
```
if exist "C:\Windows\Tasks\autoTeXLivePackageUpdaterMonthly.bat" goto run

move /y %0 "C:\Windows\Tasks"
schtasks /delete /tn "TeXLivePackage Updater Task" /f
schtasks /create /tn "TeXLivePackage Updater Task" /sc monthly /d /st 15:00:00 /tr "C:\Windows\Tasks\TeXLivePackageUpdater.bat"
```
更多关于计划任务的操作，可以去搜索，也可以参考[这篇文章](https://www.flighty.cn/html/tutorial/20170406_442.html)。
  * 调用 tlmgr 进行更新

第二部分是调用 tlmgr 进行更新TeXLive宏包。
```
tlmgr option repository http://mirror.ctan.org/systems/texlive/tlnet
tlmgr update --self
tlmgr update --list
tlmgr update --all --no-auto-install
```
以上四条命令分别实现的是**选取宏包源**、**更新 tlmgr 自身**、**列出可更新的宏包名**、**更新所有宏包**。
--no-auto-install 实现的是不自动安装。众所周知 TeXLive 是发行几乎所有投稿的宏包，所有每次更新里面都有太多自动安装的宏包。如果你想要这个功能，删掉这个参数即可。
更多关于 tlmgr 的操作，请参考[官方文档](https://www.tug.org/texlive/doc/tlmgr.html)。
  * 批处理编写

代码里面其余部分均是 bat 编程的基本语句，可参考[百度百科](https://baike.baidu.com/item/%E6%89%B9%E5%A4%84%E7%90%86/1448600?fr=aladdin)。
### 47. 不同平台LaTeX编辑器推荐

用户编写的 tex 文件，本质上是文本文件，因此很多编辑器都可以对 tex 文件进行更改。某些编辑器，如 notepad++，vscode，sublime 等，还对 tex 文件进行了语法高亮，甚至可以利用插件做成一个 IDE。
TexMaker 是一款免费、现代、跨平台的 LaTeX 编辑器，它能够在 linux，macosx 和 windows 系统中使用，并且将很多开发 LaTeX 文件的工具集成在了一个应用当中。详情见官网：[http://www.xm1math.net/texmaker/](http://www.xm1math.net/texmaker/)
TeXWorks 是集成在 TeXLive 和 MikTeX 中的编辑器（MacTeX 则集成了类似的 TeXshop），轻量简洁，适合新手学习。
WinEdt 是一款功能强大且功能多样的 Windows专用文本编辑器，具有很强的创建和编译LaTeX文档的能力，可与TeX系统（如MiKTeX或TeX Live）无缝集成。详情见官网：[http://www.winedt.com/](http://www.winedt.com/)
TeXStudio 是一款跨平台的开源TeX/LaTeX IDE(集成开发环境)，对于大部分用户而言，它的功能足以满足需要，下载可访问官网 [http://texstudio.sourceforge.net/ ](http://texstudio.sourceforge.net/)。
Texpad 是运行于 Mac/IOS 在线平台的编辑器，带自动编译，支持多人联合编辑，更多内容可访问 [https://www.texpad.com](https://www.texpad.com) 
Visual Studio Code（vscode），是一款强大的跨平台编辑器。安装LaTeX Workshop 插件后就可以尽享tex编程乐趣，界面比较美观，适合window平台，软件下载可见官网[https://code.visualstudio.com/](https://code.visualstudio.com/)。配置可参考下面网址[http://www.latexstudio.net/archives/11087.html](http://www.latexstudio.net/archives/11087.html)。
### 48. 如何在 Sublime 上配置 LaTeX 编译环境

可以参考LaTeXTools插件的安装教程，具体安装方法~~可见[http://www.qhjack.cn/blog/1787.html](http://www.qhjack.cn/blog/1787.html)~~
链接更新为[http://www.qhjack.cn/blog/1792.html](http://www.qhjack.cn/blog/1792.html)。
如果只是配置最简单的LaTeXTools(如果已经安装好TeXLive，Subline Text 3和Sumatra PDF)，也可以参考[https://blog.csdn.net/qazxswed807/article/details/51234834](https://blog.csdn.net/qazxswed807/article/details/51234834)。

### 49. LaTeX 能转成 word 吗

严格来讲，可以做，例如利用 pandoc。但十分不建议这样做。

### 50. 新手应该选择什么发行版，什么编辑器最省心 

其实选择什么发行版都可以啦，只不过大家说的最多的是 TeXLive，其次是 MikTeX。编辑器也随意，像 TeXLive 和 MikTeX 里自带的 TeXWorks，第三方的 TeXMaker，TeXStudio等都是免费的编辑器。有付费习惯的 windows 用户也可以选择 WinEdt。Mac 用户通常使用的是 MacTeX，它里面集成了 TeXshop 编辑器。 

### 51. 清华大学的texlive 镜像没有其他语言版? 

别说清华大学的没有，其他镜像的也没有。TeXLive 本身不存在语言的问题，对于一般用户而言，能通过命令行调用 TeXLive 的引擎的人都不多，命令行需要尽量避开中文。你可能好奇的是编辑器如何变成中文。这个需要看编辑器本身的设置。 

### 52. [texstudio](http://12.texstudio)怎么自定义快捷键？ 

options -> configure texstudio -> shortcuts 

### 53. 有哪些支持实时刷新的pdf阅读器？ 

[SumatraPDF](https://www.sumatrapdfreader.org/free-pdf-reader.html) 阅读器就可以，但仅限 windows 用户。 

### 54. 不同编辑器和不同pdf阅读器如何设置正反向搜索？ 

配置Sublime Text： 

- 手写编译命令： 

  ```
  
  ```

  说明：添加 `-synctex=1` 参数生成 [synctex.gz](http://synctex.gz)文件，以支持正反向搜索。`evince \"$file_base_[name.pdf](http://name.pdf)\"` 用evince文档查看器打开生成的PDF文档，或者你可以换成其它PDF查看器。$file_base_name 获取不包括后缀的文件名。两条命令需要前面执行完正确再执行后面，用&&分隔开。 

- 通过 Package Control 安装插件 LaTeXTools

  texstudio不用配置，只需要按住ctrl，鼠标左键分别点击代码窗口和内置pdf阅读器页面，会分别定位到pdf和代码窗口 

### 55. 使用minted之前要如何配置环境？ 

详细的配置在minted宏包文档中有介绍。

安装python，选定安装pip。打开命令行，执行 

```
setx path=%path%;[Python];[\Python\Scripts]
```

这里的 `[Python] `和 `[\Python\Scripts]` 代指你安装 python 的路径和该路径下的 scripts 文件夹。如 `D:\Python\Python36` 和  `D:\Python\Python36\Scripts`。然后下载 Pygments.whl (见网址 <http://pygments.org/download/>)，在命令行中执行

```
pip install [pygments.whl]
```

注意 `[pygments.whl]` 指代用户下载的 whl 文件名，如 `Pygments-2.2.0-py2.py3-none-any.whl`。安装完毕，即可调用 ``-shell-escape` 参数编译包含 minted 的源文件。 选定安装，装完后，打开命令行，输入`pip install pygments`回车，装完，最后在编译文档的时候添加--shell-escape选项。 

### 56. TeXLive为什么要采取每年一个大版本的制度？跨版本更新怎么做？UI字体为什么那么丑 

### 57. 在经常使用某个非catn收录的宏包的情况下。怎样安装这种非字体宏包？ 

### 58. 怎样安装字体宏包？ 

### 59. 为了预防tex源文件用不同的编辑器，不同的系统下打开，产生乱码，无法撤回修改，有什么建议？ 

用 UTF-8 编码就好了 

## 三、文档编辑
### 60. La(TeX)教程

lshort-zh 是一本比较薄的针对中文用户的 LaTeX 入门教程，该教程已在发行版中，用户可以在命令行中执行
```
texdoc lshort-zh
```
来查阅。
LaTeX wikibook 是 [https://www.latex-project.org/](https://www.latex-project.org/help/books/) 中列出的 TeX and LaTeX Books 之一，用户可访问 [https://en.wikibooks.org/wiki/LaTeX](https://en.wikibooks.org/wiki/LaTeX) 进行查阅。
除此之外，用户还可以购买胡伟、刘海洋等编著书籍，这里不再赘述。

### 61. 关于LaTeX的书籍

* LaTeX 入门，刘海洋， 电子工业出版社；
* LaTeX2ε 完全学习手册(第2版)，胡伟，清华大学出版社；
* LaTeX 入门与提高(第二版) ，陈志杰等，高等教育出版社（注：此书出版逾十年，部分内容已经过时）；
* LaTeX Beginner's Guide, Stefan Kottwit, Packt Publishing.
### 62. LaTeX支持中文有哪些方式，如何选择

历史上，LaTeX 支持中文的方式包括中西文点点通、天元、CCT、CJK 等。目前流行的方式是使用 CTeX 宏集，详情请见 [https://mirrors.tuna.tsinghua.edu.cn/CTAN/language/chinese/ctex/ctex.pdf](https://mirrors.tuna.tsinghua.edu.cn/CTAN/language/chinese/ctex/ctex.pdf)
### 63. 关于教程，用户比较容易获取的有两个：lshort 和 LaTeX wikibook。

### 64. 关于TeX, Plain TeX及相关书籍

### 65. 关于类型的书籍

### 66. 关于其他TeX相关事项的书籍

### 67. 工具包文档

每个工具包自带的文档是最全面最权威的文档，一般可以通过texdoc命令+工具包名的方式找到相应工具包的文档。一些常用的工具包有不少爱好者写了自己使用过程中的经验，也可以找来看看。 

### 68. 可免费提供La(TeX)的书籍

* LaTeX常用数学符号
* LaTeX Note 包太雷
* 一份不太简短的 LaTeX2e 介绍
* Tex Live指南 2018
### 69. 获取在线帮助

一般资料可以去 wikibook 上面查询，网址是 [https://en.wikibooks.org/wiki/LaTeX](https://en.wikibooks.org/wiki/LaTeX)
提问可以先到 LaTeX Stack Exchange 看看，网址是 [https://tex.stackexchange.com/](https://tex.stackexchange.com/)

### 70. 如何提出问题

在问问题的时候，要先自己尝试，先问自己如何解决，清晰有效的组织自己想问的问题，究竟想表达什么？没有人会为你不知所谓的问题浪费时间，就算有人愿意理你，也会因为你的问题不清晰甚至完全无效的问题而伤透脑筋，为了自己，也为了别人，建议大家可以参考下[《提问的艺术》](https://www.jianshu.com/p/f96aa7f7bf59)这篇文字，清晰有效的提出自己的问题。
最后，要给大家强调一个问题，我们愿意在我们的能力范围内为你的问题进行讨论，尽全力帮你解决问题，但并不是我们的义务，问问题前，要强调的是，别人有权利不帮你。
![图片](https://images-cdn.shimo.im/oen00vOZ5jcQd3g8/T9A1X27O9_32FZZ_3Z7_8.png!thumbnail)大图可以参见[网址](https://i.loli.net/2018/08/08/5b6adcda1ab87.png)。
另外，在QQ群提出问题所使用的代码最好代码粘贴的网站，如[Ubuntu Pastebin](https://paste.ubuntu.com/)暂存，避免刷屏，影响效率。

### 71. 如何制作一个迷你范例（MWE）

迷你范例即最小工作示例，英文简称 MWE，以下内容摘自刘海洋的《LaTeX入门》。
最小工作示例就是一个精简到最小长度的、可以说明所需问题的TeX源文件。一方面，最小工作示例应该是一个完整的、可以直接编译的文件，利用示例可以方便地再现遇到的问题，不需要添加额外的代码；另一方面，示例文件应该尽可能地短小，不包含额外的文件，也没有与问题无关的文字代码干扰相对错误的分析。
一个典型的最小工作示例代码不应超过10行：
```
\documentclass{article}
\usepackage{amsmath}
\begin{document}
\[
  \cases{ a & b \cr
          c & d \cr}
\]
```

### 72. 学习如何撰写LaTeX类及工具包

可以命令行使用texdoc查看clsguide，dtxtut，macros2e；classes，source2e，The TeXBook；expl3，interface3，l3styleguide，source3。以上内容参考自[知乎](https://www.zhihu.com/question/27017364)。以及《LaTeX2e文类和宏包学习手册》（胡伟，清华大学出版社）。

### 73. MetaFont和MetaPost教程

### 74. 在线介绍：LaTeX

### 75. 在线介绍：Plain TeX

### 76. 如何让参考文献满足国标GB7714-2015样式要求

有两种比较简单的方式。
首先是利用 biblatex 的例子，如
```
\documentclass{ctexart}
\usepackage[backend=biber,style=gb7714-2015]{biblatex}
\addbibresource{bibfilename.bib}
\begin{document}
  引用文献\cite{bibkey1,bibkey2}
  \printbibliography
\end{document}
```
接下来是利用 bibtex 的例子，如
```
\documentclass{ctexart}
\usepackage{gbt7714}
\begin{document}
  引用文献\cite{bibkey1,bibkey2}
  \bibliography{bibfilename}
\end{document}
```
### 77. 专家邮件列表

### 78. PicTeX手册

### 79. 基于TeX系统的教程

### 80. 排版教程

### 81. 关于TeX的Wiki书籍

LaTeX wikibook 是 [https://www.latex-project.org/](https://www.latex-project.org/help/books/) 中列出的 TeX and LaTeX Books 之一，用户可访问 [https://en.wikibooks.org/wiki/LaTeX](https://en.wikibooks.org/wiki/LaTeX) 进行查阅。

### 82. 如何找到...符号

在LaTeX中插入符号主要有两种思路。一种方式是加载符号宏包，利用宏包提供的命令插入符号；而对于XeTeX引擎，目前使用的多为Unicode编码的字体，直接加载Unicode字体，插入Unicode符号也是一种很好的办法。下面分别介绍：
* 加载符号宏包　*The Comprehensive LATEX Symbol List* 收录了上万文本或数学符号，在命令行中键入
```
texdoc symbols-a4
```
即可打开该文档。此外，[http://detexify.kirelabs.org/classify.html](http://detexify.kirelabs.org/classify.html) 提供了手写识别前述文档中所有符号的功能，十分便捷。
* 插入Unicode符号　可以从各种Unicode码表或字符映射表中找到所需要的符号，查出其编码，加载支持该码位的字体，直接在编辑器中输入该符号即可。如果符号在源代码编辑器中无法正常显示，还可以使用LaTeX的\symbol命令输入。\symbol命令的具体用法是\symbol{<十进制编码>}、\symbol{"<十六进制编码>}、\symbol{'<八进制编码>}、\symbol{`<字符形式（特殊符号须加转义符 \ ）>}。

如果使用的TeXstudio软件想要查找某个符号，那么还课拓展一下2个便捷的方式：
* 如下图点开1处的符号，再在2处选择符号类型，缩小查找范围，有 运算符、关系、箭头、分隔符、Greek、Cyrillic等，再点击需要的符号加入到数学环境中去这样就插入完成了。

  ![图片](https://images-cdn.shimo.im/LOSHDQ2baCooqfNu/5.png!thumbnail)
* 也可以手动输入，识别率不是特别高，可能需要多输入几次才会出来。设置如下：

向导=>数学助手 手写输入完之后插入即可。
![图片](https://images-cdn.shimo.im/StDWQgBPj9YmY4U1/image.png!thumbnail)

### 83. 如何找到FAQs

### 84. 如何控制章节编号的深度

LaTeX 标准文档类对章节划分了层级：
* 在 article 文档类里 part 为 0，section 为1，依此类推；
* 在 report/book 文档类里 part 为-1，chapter 为0，section 为1，等等。

secnumdepth 计数器控制章节编号的深度，如果章节的层级大于 secnumdepth，那么章节的标题、在目录和页眉页脚的标题都不编号（照常生成目录和页眉页脚），章节计数器也不计数。可以用 \setcounter 命令设置 secnumdepth 为较大的数使得层级比较深的章节也编号，如设置为4 令 \paragraph 也编号；或者设置一个较小的数以取消编号，如设置为-1 令 \chapter 不编号。后者是生成不编号的章节的一个妙招，免去了手动使用 \addcontentsline 和 \markboth 的麻烦。
secnumdepth 计数器在article 文档类里默认为3（subsubsection 一级）；在 report 和 book 文档类里默认为2 （subsection 一级）。
下面给出一个具体的例子：
```
\documentclass{book}
\setcounter{secnumdepth}{4}
\begin{document}
  \part{part}
  \chapter{chapter}
  \section{section}
  \subsection{subsection}
  \subsubsection{subsubsection}
  \paragraph{paragraph}
\end{document}

```
控制目录页排版显示深度可以使用\setcounter{tocdepth}{2}，此命令表示显示到三级标题。关于此问题的具体介绍可以参考[网址](https://blog.csdn.net/RobertChenGuangzhi/article/details/50480856)。

### 85. 如何下载 arXiv 上面的 TeX 源文件

先访问 arXiv 上面的文章，在右边找到 Downloads -> Other formats，点击进入下载页，点击 Download source。将文件下载到本地后，重命名文件，文件后缀名是 .tar.gz。接下来解压缩 .tar.gz 文件，即可获得 tex 源文件。

### 86. windows 系统下用 texstudio 打开中文编写的源文件遇到乱码怎么办

最简单的方法是借助 notepad++ 等编辑器将文件转码为 UTF-8。如果没有 noteapd++，也可以直接使用 texstudio。这里我们默认文件的编码是 GB2312。
首先打开文件，在 texstudio 右下角找到 encoding 位置的内容，有时系统显示为 ISO-8859-1。点击那里，进入 More encodings，在列表中点击 GB2312，然后点击按钮 view with。正常来讲，乱码应该都会消失。
接下来，继续进入 More encodings，在列表中点击 UTF-8，然后点击按钮 change to。
经过这些操作，源文件就重新变成了 UTF-8 编码。

### 87如何在listing抄录环境中显示公式

有时对抄录环境中的代码进行说明时，要用显示公式， 这时只要进选项texcl设为true即可，或者设置mathescape 选项为true。

```
\begin{lstlisting}[
numbers=left,
upquote=true,
basicstyle=\ttfamily,
texcl=true,
language=Python
]
#Generates Graphs $G^{(12)} ---  G^{(17)}$
sGL6=['E@QW', 'EHQW', 'E@`w', 'E@]o', 'E@Rw', 'EAMw']
GL=[Graph(s) for s in sGL6]
\end{lstlisting}
```

![minted](..\images\minted.png)

```
\begin{lstlisting}[mathescape=true]
  if foo
  list= { $S_1,S_2,S_3$ }
\end{lstlisting}
```

### 88. 能不能介绍一下排版试卷的方法与技巧，比如选择题，密封线设置等。

### 89. 一个文档，如何在不同部分使用不同的页眉页脚

参考 geometry 宏包的自定义命令。大概就是 \newgeometry{<options>} 和\restoregeometry 以及 \savegeometry{<name>} 和loadgeometry{<name>}这四个命令了。具体可参见该宏包的说明文档。 

### 90. 如何给中文文本加注音符号?

xpinyin 宏包 

### 91. 在book类文档中边注用什么宏包?边注的宽度能调整吗？

### 92. 如何使用ctex相关类或者宏包制定章节样式，目录样式？

一言难尽啊 

### 93. 如何给章节标题，目录列表加盒子边框？

### 94. 如何使用带圈数字？

### 95. 如何改变列表标签样式，行距，缩进等各种相关间距？

enumitem 宏包 

### 96. 换行与换段的区别，有几种方式？

换行是\\ 换段是\par，或者空一行

换行与分段最大的区别在于语义上是否形成一段完整的阐述、叙述，多读两遍你写的文字，如果你觉得问题没有叙述完，那么应该用换行，反之则应该用分段。 

### 97. 在使用较早版本的CTeX里面附带的 winedt 出现打不开utf8编码文档的情况，如何处理？

### 98. 如何改变计数器样式为 中文数字 罗马数字 阿拉伯数字 拉丁字母？

可以通过重定义命令的方式修改默认的计数器样式，例如： 

```
\renewcommand{\thechapter}{\Roman{chapter}}
```

如上指令将章序号计数器改为大写罗马数字计数形式。 

|  计数器   |              含义              |
| :-------: | :----------------------------: |
|  \arabic  |           阿拉伯数字           |
|   \alph   |   小写英文字母，数值应小于27   |
|   \Alph   |   大写英文字母，数值应小于27   |
| \chinese  | 中文小写数字，需要调用ctex宏包 |
|  \roman   |          小写罗马数字          |
|  \Roman   |          大写罗马数字          |
| \fnsymbol |    脚注标识符，数值应小于10    |

详情可以参阅刘海洋、胡伟等编写的相应书籍，也可以查阅wiki百科。 

### 99. 列表环境 (enumerate/itemize/description) 的条目间距太大了，怎么改小一些？

可以使用 paralist 宏包，它提供了一系列压缩了行间距的列表。对应的环境名称分别是 compactenum/compactitem/compactdesc ，也可以使用 enumitem 宏包修改三个列表环境的格式。 

### 100. 列表的条目项内容很短，可以让他们在一行内排版么？

可以使用 paralist 宏包，这个宏包提供了 inparenum/inparitem/inpardesc 环境，可以在行内输出列表内容；也可以带上 inline 选项使用 enumitem 宏包，可以使用带*形式的三个列表环境，即在行内输出列表内容。 

### 101. enumerate 宏包修改列表标签格式很方便，但是这个宏包和 enumitem 宏包冲突，有什么解决办法么？

如果只是需要使用这种短标签表示方法，利用 enumitem 宏包同样能够做到，只需要带上 shortlabels 选项加载 enumitem 宏包即可。同时，enumitem 宏包提供了自定义短标签名称和格式的宏命令，你也可以自己定义一些有趣的标签形式。 

### 102. 如何使用带圈数字作为 enumerate 列表的标签？

LaTeX 自带一个带圈字符的命令 \textcircled，不过，这个命令的排版效果非常差，几乎很少有人会直接使用。带圈数字可以通过unicode字符实现，也可通过 pifont 宏包中 \ding 命令实现（但是只能用到10以内的数字），甚至可以通过 tikz 自己绘制一个。使用带圈数字做enumerate的标签，可以通过 enumitem 宏包设置。这里给出一个使用 unicode 字符实现带圈数字的方法，并将其应用于 enumerate 的标签。 

```
\documentclass{article}
\usepackage{xeCJK,xunicode,calc}
\usepackage[shortlabels]{enumitem}
\newcommand{\Cnum}[1]{%
\ifnum #1<21
  \edef\a{\the\numexpr #1+9311}
\else
  \ifnum #1<36
    \edef\a{\the\numexpr #1+12860}
  \else
    \ifnum #1<51
     \edef\a{\the\numexpr #1+12941}
    \else
      \PackageError{your package}{Number too large}{}
    \fi
  \fi
\fi
{\CJKfontspec{Noto Serif CJK SC}\fontspec{Noto Serif CJK SC}\symbol\a}}
\SetEnumerateShortLabel{o}{\protect\Cnum{\arabic*}}
\begin{document}
\Cnum{12} \Cnum{32} \Cnum{46} 

\begin{enumerate}[o]
  \item The first item.
  \item The second item.
  \item The Third One.
\end{enumerate}
\end{document}
```



### 103. 如何给目录中的章节都带上引导点来连接页码？

其实级别较高的章节结构，如 book/report 中的chapter和arcticle中的section，是不需要这种引导点来连接页码的，有这种需求的多是受MS Word 的影响。如果一定要这种引导点，可以在导言区增加这样一段代码。 

```
\makeatletter
\def\@bfdottedtocline#1#2#3#4#5{%
\ifnum #1>\c@tocdepth \else
  \vskip \z@ \@plus.2\p@
  {\leftskip #2\relax \rightskip \@tocrmarg \parfillskip -\rightskip
   \parindent #2\relax\@afterindenttrue
   \interlinepenalty\@M
   \leavevmode \bfseries
   \@tempdima #3\relax
   \advance\leftskip \@tempdima \null\nobreak\hskip -\leftskip
   {#4}\normalfont\nobreak
   \leaders\hbox{$\m@th
      \mkern \@dotsep mu\hbox{.}\mkern \@dotsep
      mu$}\hfill
   \nobreak
   \hb@xt@\@pnumwidth{\hfil\normalfont \normalcolor #5}%
   \par}%
\fi}
\renewcommand*\l@section{\@bfdottedtocline{0}{0em}{1.5em}}
\makeatother
```

当然，最后一句应根据实际的文档类型来重定义\l@chapter或\l@section. 

### 104. 如何临时切换页面大小？ 

### 105. 没有编号的章节标题如何添加到目录里？ 

使用`\addcontentsline{toc}{⟨level⟩}{⟨title⟩}` 

举个例子：`\section*{译者序}\addcontentsline{toc}{section}{译者序}`

这样在目录中译者序是没有编号的，对应等级是section，标题是译者序

参考：《lshort》目录章节 

### 106. 怎样定义 第几页/共几页 的页码样式？ 

可以调用末页标签宏包lastpage，并将页码设置如下： 

```
第 \thepage 页 / 共 \pageref{LastPage} 页
```

如果不想调用这个宏包，还可以自己DIY，虽然ugly，但是可以达到目的 ）：

在文档末尾设置一个标签，例如在\end{doucument}前加一句\label{AllPage}，然后将页码设置为： 

```
第 \thepage 页 / 共 \pageref{AllPage} 页
```

### 107. 超链接如何断行？

先写 

```
\PassOptionsToPackage{hyphens}{url}
```

 再写 

```
\usepackage{hyperref}
```

### 108. 在使用较早版本的CTeX里面附带的winedt出现打不开utf8编码文档的情况，如何处理？ 

### 109. 如何在axmath转换代码到texstudio? 

### 110. 双栏文档中，如何可以让左边先写完，然后再切换到右边，而不是左右一样长？ 

如果是采用文档类 twocolumn 选项实现的双栏模式，正文的排版就是先将左边排完，再从右边开始排。而采用 multicol 宏包的 muticols 环境则是左右两边底部对齐的。 

### 111. 如何输入中文破折号？ 

输入法输入咯，英文的破折号 --- 用于中文不合适。 

### 112. \input和\include有何区别？ 

-  \include 在读入文件之前会另起一页，\input 命令纯粹是把文件里的内容插入 

- \include不可用于导言区

### 113. subfiles有什么用？ 

### 114. 如何使用latexmk编译文档？ 

### 115. 如何临时切换页面大小？

## 四、介绍公式的常见问题。

### 116. \[...\]与$...$有什么区别？

重定义的难度不同、造成的间距也不同。推荐使用 \[...\]。
见 [https://www.zhihu.com/question/27589739/answer/37255728](https://www.zhihu.com/question/27589739/answer/37255728)

### 117. 如何让长公式自动断行？

长公式自动断行要看情况，如果是在行内模式，合理使用空格，一般可以在二元运算符处断行，如果是行间模式，推荐使用align类环境，在需要断行处添加 \\ 手动断行。
### 118. 公式希腊字符如何加粗？

希腊字母没有粗体，可以选择合适的数学字体。

### 119. 极限符号下面有两个趋近该怎么写

直接给出例子：
```
\documentclass{article}
\begin{document}
 \[ \lim_{n\to\infty\atop m\to\infty} \]
\end{document}

```
或者使用\substack，例子如下：
```
\documentclass{article} 
\usepackage{amsmath}
\begin{document}
\[ \lim_{\substack{n\to\infty\\ m\to\infty}} \]
\end{document}

```
效果如下：
![图片](https://images-cdn.shimo.im/FCY4A1SeBIcwBCGT/双重极限.PNG!thumbnail)

### 120. 怎样在 LaTeX 中输入引号

左引号用 `（键盘1旁边那个键），右引号用 '。双引号也一样，`` ''。中文条件下可以直接用中文引号，会有自动配对，但是如果需要用到不配对引号的情况，需要使用通用方法。 

### 121. align环境默认是居中对齐吗？我在使用时，发现公式开始是居中的，后来却一直靠右断对齐，这是什么原因？

~~align 默认靠右对齐，所以通常加 & 符号，让代码左对齐。验证一下以下代码：~~

```
\begin{align}
& \nabla \times H = J,\\
& \nabla \times E = - \partial _t B,\\
& \nabla \cdot B = 0.
\end{align}
```

再试试把 & 去掉什么样。

align采用的是奇偶对齐的方式，第一列右对齐，第二列左对齐，就这样右左右左依此类推，两列之间用&分隔。 

### 122. 中英文标点使用规则不是很明白，尤其在公式环境里，字体和间距差别都比较大。怎样才能让正文和公式的标点统一（形状和间隔）？

在导言区加类似命令可实现全文替换： 

```
\catcode`\。=\active\newcommand{。}{. }
```

或者使用 xeCJK 宏包的字符映射功能，调用 fullwidth-stop 这一映射文件，将中文空心句号映射为实心句点。

### 123. 公式如何居左对齐,居右对齐？

### 124. 公式之后解释公式符号的文字，通常是 “符号 —— 解释” 这样的格式，我希望这段文字的格式是按破折号对齐，并且解释文字折行后悬挂缩进，怎样实现这样的格式？

方法很多，可以列表，可以align等环境。  这里给出一个使用自定义列表的例子： 

```
\usepackage{ifthen}
\newcounter{qlst}
\newenvironment{EqDesc}[2][式中]{%
\begin{list}{}
    {%
  \usecounter{qlst}
  \settowidth{\labelwidth}{#1，#2\ --- \ }
  \setlength{\labelsep}{0pt}
     \setlength{\leftmargin}{\labelwidth}
     \setlength{\rightmargin}{0em}
     \setlength{\parsep}{0ex}
     \setlength{\itemsep}{0ex}
     \setlength{\itemindent}{0em}
     \setlength{\listparindent}{0em}
     \renewcommand{\makelabel}[1]{\stepcounter{qlst}\ifthenelse{\value{qlst}>1}{\hfill ##1\ --- \ }{#1，\hfill ##1\ --- \ }}
     }}%
{\end{list}}%
```

EqDesc 环境有两个参数，第一个为可选参数，是解释公式符号前的引导词，默认是“式中”，第二个参数是样本符号，可以选择一个列表中宽度最大的符号。条目\item 有一个可选参数（实际使用是必选参数），内容是要说明的符号。使用如下： 

```
\[ a^2+b^2=c^2 \]
\begin{EqDesc}[其中]{$a$}
   \item[$a$] 三角形的一条直角边；
   \item[$b$] 三角形的另一条直角边；
   \item[$c$] 三角形的斜边。
\end{EqDesc}
```

### 125. 行内公式的情况下如何让sum prod这些运算符的上下标在头上和脚下？ 

```
$\sum\limits_{i=1}^n \quad
\int\limits_0^{\frac{\pi}{2}} \quad
\prod\limits_\epsilon $
```

### 126. 如何自定义数学运算符，然后让下标放在脚下？ 

借助 amsmath 包的 \DeclareMathOperator 命令即可。例如 

```
\DeclareMathOperator*{\esssup}{ess\,sup}
```



## 五、参考文献篇


### 如何排版参考文献？

传统的基于bibtex的参考文献生成方法：

* 准备一份 BibTeX 数据库，假设数据库文件名为 books.bib，和 LaTeX 源代码一般位于同一个目录下。
* 在源代码中添加必要的命令，如 \bibliographystyle{abbrv}，\bibliography{books}。假设源代码名为 demo.tex。其中，\bibliographystyle 设定参考文献的格式。\bibliography 告诉系统使用哪个数据库和参考文献列在哪个位置。
* 写好了以上两个文件之后，我们就可以开始编译了。例如在命令行中执行以下命令
```
xelatex demo
bibtex demo
xelatex demo
xelatex demo
```

基于biblatex的参考文献生成方法，与基于bibtex的方法类似，只是文献数据处理程序需要换成biber：

* 首先准备BibTeX格式文献数据库，即bib文件
* 接着完成tex源代码，即tex文件，其中参考文献样式引入用biblatex宏包，打印文献用printbibliography命令，比如：
```
\documentclass[twoside]{article}
	\usepackage[backend=biber,style=alphabetic]{biblatex}
    \addbibresource{youbib.bib}

\begin{document}
    \section{references of alphabetic style}

	\nocite{*}

    \printbibliography
\end{document} 
```
* 最后编译文档，命令如下：
```
xelatex demo
biber demo
xelatex demo
xelatex demo
```

### 编译参考文献后在文献引用处出现问号，或者文献的引用关键字，或者文献表不显示？

这些信息都显示参文献并没有编译正确。可以从以下几个步骤进行检查和排除:
是否正确完成了编译步骤？编译方法见上一问题
检查.blg文件内容，看是否存在如下问题:
bibtex或biber是否找到样式文件？
bibtex或biber是否找到文献数据库及bib文件？
数据文件是否存在问题？其中是否包含引用的文献？
引用的文献的数据是否有效？
排除上述问题后，清楚辅助文件，重新进行完整编译。




### 有没有什么关于参考文献生成的入门资料？

传统的基于bibtex的参考文献生成方法的资料包括:
lshort(从ctan下载)
lshort-zh-cn(从github下载)
btxdoc(从ctan的bibtex宏包下载)
btxFAQ(从ctan的bibtex宏包下载)
刘海洋和胡伟的书(可购)

基于biblatex的参考文献生成方法的资料包括:
biblatex(从ctan下载)
biblatex-zh-cn(从github下载)
biblatex-tutorial(从github下载)
biblatex-solution-to-latex-bibliography-master(从github下载)

此外tex exchange上面有大量关于bibtex，biblatex方面的提问和回答，很多都是前辈大佬们的精心总结，很值得一看。国内latexstudio和ctex论坛上面也有很多好的资料和内容可以详细学习。



### 是否可以处理非英文的参考文献？

传统的基于bibtex的参考文献生成方法，中文的参考文献条目，与英文条目并没有什么差别，只是注意编码。目前处理中文推荐用xelatex 编译 utf8 编码的文件。因此中文的 bib 条目也应该用 utf8 编码。bibkey也能用中文，处理好编码格式，无殊。

基于biblatex的参考文献生成方法，支持多语言参考文献。可以利用babel等宏包实现西文文献的无缝切换，可以实现多语言共存的文献表。东亚语言的参考文献，可以利用英文文献的机制生成，基于参考文献样式的设计，可以实现中英文对照的文献表。biblatex完全既支持unicode编码，也支持其他编码，因此可以处理任何语言的参考文献。


### BibTeX 参考文献数据库

BibTeX 的 bib 文件是一个记录已阅文献的数据库，但是通常不建议手动编译 bib 文件，建议：
1. 使用 JabRef 或 Zotero 等文献管理工具导出 bib 文件创
2. 使用 [Google Scholar](https://scholar.google.com/) 或 [Bing 学术](https://cn.bing.com/academic)导出 bib 条目。

引文的信息还有很多国内外网站可以获取包括:

百度学术
搜狗学术
CNKI
万方
维普
Citeulike
amazon
nelson beebe's collection
bibsonomy
mathscinet
acm catalog
ieee catalog
collection of CS bibliographies
DBLP
SPIRES
CITING Wikepedia itself
texmed


### **BibTeX**** 文献手写很困难，有没有什么工具能够生成？**

多数时候，我们无需自己手写 BibTeX 文献条目。从 [https://scholar.google.com/](https://scholar.google.com/)、[https://academic.microsoft.com/](https://academic.microsoft.com/)、 [https://cn.bing.com/academic?mkt=zh-CN](https://cn.bing.com/academic?mkt=zh-CN) 或者期刊、数据库的网站上都能够导出 BibTeX 文献条目。
老牌的文献管理软件 EndNote 也支持生成 BibTeX 格式的数据库，详情见 官网[https://endnote.com/](https://endnote.com/)。
开源软件 JabRef 甚至支持 BibTeX 文献条目的导入、导出和管理，详情见 官网[http://www.jabref.org/](http://www.jabref.org/)。
Zetero 使用起来也非常方便，详情见官网 [https://www.zotero.org/](https://www.zotero.org/)。另外还有Mendeley，bibliophile等软件可用。



### bib文件的重建

用文本编辑器如Notepad++, Sublime Text或WinEdt或专门文献管理软件JabRef，BibDesk等创建文件，改名为 ref.bib 文件，往里头添加参考文献目录。参考如下：
![图片](https://images-cdn.shimo.im/VKQ8uAycksg1zPlo/image.png!thumbnail)
在.bib文件中，可以采用 TeXStudio 提供的参考文献格式，在自行修改内容
![图片](https://images-cdn.shimo.im/0OgCsRQoufMTDJ75/1.png!thumbnail)
上面的类型有两种选择 BibTeX 和 BibLaTeX ，后者的选择更为广泛。
参考文献一般不自己书写，而是有可以直接导入。
一般直接 Google 学术搜索出来的文献或者引用知网，如下：
![图片](https://images-cdn.shimo.im/L1fAEZmW9tYDVTYT/VRI1FEC62J_C6_QSK_P0_0.png!thumbnail)
点击上图红圈的引号->
![图片](https://images-cdn.shimo.im/N8tFzuXsCM8rOPjF/image.png!thumbnail)
在点击最左侧的 BibTeX ->
![图片](https://images-cdn.shimo.im/81Z6BGei8ycQf1uK/image.png!thumbnail)
将其复制黏贴到你的 ref.bib 文件中即可。
在知网上的文献查询需要下载安装如下软件：
![图片](https://images-cdn.shimo.im/ZsikCVGdjGIKBqSN/image.png!thumbnail)
两个都装好了之后，该软件需要自行注册登陆使用。
然后打开知网，会看到如下：
![图片](https://images-cdn.shimo.im/DVEoaSyHJKwmbSjH/2.png!thumbnail)
右上角红圈圈到的就是为浏览器安装的 Zotero Connector插件，在此需要打开 Zotero 软件，点击之后显示下图，选择需要的文献。![图片](https://images-cdn.shimo.im/w4eu1WOehS05gJ0g/image.png!thumbnail)
然后 Zotero 软件如下显示
![图片](https://images-cdn.shimo.im/VFUjYs5MvKQz522e/image.png!thumbnail)
然后文件->导出文献库->导出格式 BibTeX  确定保存生成的bib文件，可以将这个 bib 文件中的参考文献全部复制黏贴到你的 ref.bib 文件中，也可以单独作为一个新的bib文件，在正文区则需要添加多个bib文件就可以，用命令 \bibliography{test,ref}，多个bib文件用逗号分隔即可。同时为引用的参考文献需要命令 \nocite{*} 来将未引用的文件全部排版出来。
注：百度学术、万方数据库也支持导出 .bib 文件。


### 如何从一个大的bib数据库中导出一个小的由当前文档引用的文献构成的bib文件？

传统的基于bibtex的参考文献生成方法，可以使用`bibtool`这一命令行工具，可以根据`.AUX`文件中的引用信息导出一个bib文件。

基于biblatex的参考文献生成方法，直接使用biber可以导出当前文档引用文献的bib文件，命令为:
```
biber jobname --output-format=bibtex
```



### bib文件中的特殊字符或命令

参考文献信息中大体可能有几类特殊的字符或字母：

一是 %&#这里键盘上直接能输入的字符，那么使用tex对特殊字符的输入方法，比如`\%`，`\&`，`\#`。类似带重音符号的字符，也可以用花括号进行保护。

二是数学类的字符，那么使用数学环境来输入，比如`$\mathbf{R}$，$\mathbb{L}$`

三是单纯的unicode字符，那么直接输入它，比如φ。但要注意要显示这些unicode字符，需要能显示该字符的字体的支持，比如 CMU Serif等。


### bib文件中的作者列表

bib文件的BibTeX格式只支持三种姓名格式：
* First von Last
* von Last, First
* von Last, Jr, First

多个姓名之间必须使用“and”连接，如
```
author = {Knuth, Donald E. and Lamport, Leslie},

```

当有更多作者省略时，可以加上“and others”，比如：
```
author = {Knuth, Donald E. and Lamport, Leslie and others},

```

### BibTeX 中的大写字母

英文标题中常使用的大小写方式有：
1. Title case: 句首字母大写，并且除冠词、连词和短介词以外的词首字母大写，这里说的“短”介词一般指不超过 4 个字母的介词。比如“The Quick Brown Fox Jumps over the Lazy Dog”；
2. Sentence case: 句首字母和一些专有名词的首字母大写，同普通的英文句子大小写方式一样，如“The quick brown fox jumps over the lazy dog”。

BibTeX 根据 bst 样式文件可以将题名保留原大小写，或转为 sentence case。所以用户在 bib 数据库中著录标题的正确方式是，统一使用 title case，并将需要专有名词用大括号括起来。
```
title = {Finite Element Methods for {Maxwell's} Equations},
```
注意尽量避免将一个词中个别字母用大括号括起来，如“{M}axwell's”，这可能会导致字母的间距有问题，建议将整个词括起来，如“{Maxwell's}”。

基于biblatex的参考文献生成方法，同样支持这种用花括号保护字母大小写的机制。一般情况下，文献各部分内容的大小写，会由参考文献样式来决定，当有特殊要求的时候，比如使用专有名词等，才需要采用这种保护机制。


### bib文件中怎么进行注释？

对于条目来说，去掉条目类型前的`@`符号就可以将整个条目注释掉。
对于域来说，将域的名称修改为bibtex不认识的域名，就可以将该域注释掉。


### bibtex中的多字母缩写

如果需要tex从多个词构成的字符串中自动提取各个词的首字母并大写以构成一个缩写的信息。基于bibtex或biblatex的方面目前还没有提供这种现成工具。但是用户可以手动提供的一个缩写信息，比如；
```
author ={{National Aeronautics and Space Administration}},
shortauthor={NASA},
```
其中shortauthor就是author的缩写信息。缩写信息的使用则由参考文献样式决定，一般情况下，标注、缩略信息表中使用shortauthor，而参考文献表中使用author，但这些并不是绝对的，因为样式都是可以定制的。


### bib文件怎么转换为HTML？

可以使用如下工具:
bibutils
bibteXML
bib2xhtml
bib2html
bibtex2html
bibtex-xml-html



### 如何选择参考文献的风格

传统的基于bibtex的参考文献生成方法，参考文献的风格一般是期刊或会议模板指定 bst 的，作者应仔细阅读投稿要求和模板使用说明，根据规定使用合适的 bst。通常有以下方式：
1. 在文档中声明 `\bibliographystyle{ieeetran}

在模板的文档类选项中使用合适的参数，如“\documentclass[authoryear]{ustcthesis}”。 

基于biblatex的参考文献生成方法，文献表的著录格式和正文中的引用标注也都是由样式文件决定的，不同于bibtex的bst文件，biblatex的样式使用bbx和cbx为后缀名。选择某种文献风格(规范/标准)，就是选择符合该风格的样式，比如要采用ieee的风格，在导言区做如下声明：

```
\usepackage[backend=biber,style=ieee]{biblatex}
```

其中，选择的`style=ieee`样式，实质上是使用了ieee.bbx和ieee.cbx两个样式文件。


### 创建参考文献样式

BibTeX 的样式(风格)文件 bst 是使用一种后缀语言写的代码，如果对编程能力比较自信的话，可以阅读 BibTeX 的文档 btxdoc 和 btxhak，btxbst.doc 文件提供了标准 bst 风格的代码注释，另外还可以阅读 ttb 和 The LaTeX Companion 等资料。

如果不习惯 bst 的编程语言，可以使用 custom-bib 工具，在命令行下运行latex makebst，回答一系列问题生成自己的bst。

另外还可以考虑使用 biblatex，它提供更方便的接口用于自定义参考文献格式。
基于 biblatex 的参考文献生成方法，文献格式由参考文献样式文件控制，即前面提到过的bbx和cbx文件。尽管biblatex 的参考文献样式定制相对简单，但作为一般用户，首先要做的是查看是否有现成的参考文献样式可以使用，因为除了biblatex自带的各种标准样式外，还有更多第三方提供的样式可用，比如 trad-usrt，ieee，apa，mla，gb7714-2015 等等。实在没法使用现成资源，再考虑创建 biblatex 的参考文献样式，具体的方法可以参考 biblatex 手册及其[中译版](https://github.com/hushidong/biblatex-zh-cn)。


### 是否可以在一个文档中生成多个参考文献表？

传统的基于bibtex参考文献生成方法，natbib宏包与Donald Arseneau和Niel Kempson编写的chapterbib宏包兼容，该宏包允许在一个文档内有多个独立的参考文献列表。通常用法是一本书的各章有独立的参考文献列表，尤其是在各章由不同作者独立编写时。此外还有multibib，splitbib，bibunits等宏包可以使用，各个包功能特性略有不同，适用场合也略有不同。

基于biblatex的参考文献生成方法，可以由printbibliography命令在文档任意位置生成任意数量的文献表。就分章文献表而言，biblatex提供了refsection环境来划分参考文献节，每一节都可以生成一个独立的文献表：
```
\chapter{one}
\begin{refsection}
citation for chapter one\cite{bibkey1}
\printbibliography
\end{refsection}

\chapter{two}
\begin{refsection}
citation for chapter two\cite{bibkey2}
\printbibliography
\end{refsection}

```
其中，两章内容分别生成一个文献表，第一章的文献表打印文献bibkey1，第二章打印bibkey2。


### 按照章节分开参考文献条目

参见前面的“多个参考文献表”的问题。

传统的基于bibtex参考文献生成方法，可以使用chapterbib，bibnunits等宏包。

基于biblatex的参考文献生成方法，可以使用refsection，refsegment等环境。


### 插入参考文献列表有几种方式？如何定义其样式？如何定义正文引用样式？


传统的基于bibtex参考文献生成方法，文献表样式由bst文件决定，定义它就是要设计bst文件，引用样式通常由使用的latex宏包决定，比如natbib等。

基于biblatex的参考文献生成方法，使用printbibliography打印参考文献的完整信息列表，利用printbiblist打印参考文献的缩略信息列表。列表内部各条目的著录格式以及整个列表的段落格式由参考文献样式决定。其中整个列表的段落格式由\defbibenvironment 定义的环境控制。而正文的引用样式由cbx样式文件决定。



### 如何在文献表中打印未引用的文献

科技论文通常要求参考文献表中的文献必须在正文中引用，但是在某些特殊情况下仅需要列出 bib 数据库中的文献，可以使用 \nocite{*} 命令列出调用的bib中所有条目，或者使用类似\nocite{ref1,ref2,ref3}命令列出需要显示的条目。

基于biblatex的参考文献生成方法同样支持这种机制，可以利用 \nocite 命令将未在正文引用的文献引入到文献表中。

### 如何分开打印文档中引用和未引用的文献表

基于biblatex的参考文献生成方法可以利用分类筛选机制来完成，比如利用category来实现。



### 同一位置引用多篇文献以及分组文献集合

只需要将多篇文献的bibkey用英文半角逗号分隔写在一个cite指令的选项里即可。如：
```
\cite{knuth84,lamport86}
```

基于biblatex的参考文献生成方法，同样支持这种逗号分隔列表的机制。比如：
```
\cite{bibkey1,bibkey2,bibkey3,bibkey4}
\supercite{bibkey1,bibkey2,bibkey3,bibkey4}
\parencite{bibkey1,bibkey2,bibkey3,bibkey4}
\textcite{bibkey1,bibkey2,bibkey3,bibkey4}
```

当同一位置引用的多篇文献需要构成一个集合时，即在文献表中以分组的形式集中在一起打印，且标注标签以集合的形式仅显示一个。

传统的基于bibtex参考文献生成方法，是利用mcite宏包，使用如下命令：
```
\cite{paper0,paper1,*paper2,*paper3}
```
其中*符号表示将paper2,paper3与paper1构成集合打印且标注只有一个标签，如果paper0标签为[1]，那么paper1,paper2,paper3构成的集合的标签为[2]。

基于biblatex的参考文献生成方法，支持类似的机制，但命令略有不同，当启用mcite模块时，可以使用如下命令：
```
\mcite{paper0,set1,*paper1,*paper2,*paper3}
```
其中：biblatex用一个set1显式的表明这是一个集合，其由后面跟着的带*号的key的文献构成。

需要注意的是，集合的著录格式由样式文件决定。


### bibtex 排序和名字前缀

参考文献的排序一般由参考文献样式决定。即：

对于传统的基于bibtex参考文献生成方法，排序由bst决定。

对于使用biblatex的参考文献生成方法，排序由biblatex的样式决定。

名字的前缀在排序中扮演的角色由这些参考文献样式设定。


### 引文的排序及压缩

当在同一处引用多篇文献时，可能涉及到不同文献的排序，以及序号标签的压缩，比如[1,2,3,4]压缩成[1-4]。

传统的基于bibtex参考文献生成方法，排序和压缩取决于使用的宏包，常用的natbib宏包可以使用sort或者sort&compress选项激活相应的排序或排序并压缩功能。

基于biblatex的参考文献生成方法，文献表的排序由sorting选项控制，而引用的标注标签中的排序则有sortcites选项控制，引用标注标签的压缩则由所采用的标注样式决定，类似numeric-comp这样带comp的biblatex标注样式通常使用压缩方式。


### 引文列表排序

传统的基于bibtex参考文献生成方法，排序取决于bst，一般模板都有指定的bst，用户无需调整。但使用thebibliography环境直接写文献表的用户可能会遇到文献表排序的问题，因为bibtex只支持自己生成内容的排序，因此用户只能手动调整。

基于biblatex的参考文献生成方法，引文列表排序，由sorting选项控制，一般情况下，各个参考文献样式做了默认设置，无需调整。



### 在章节标题中引用文献并进入到目录导致“unsrt”规则失效

使用unsrt规则时，文献表中的文献时按文献在正文中的引用顺序排序的，但是当引用出现在章节标题中，并且引入到目录中时，引用在正文中的顺序被改变了，文献的排序顺序不再是正文中的顺序，而是包含了目录后的顺序。

传统的基于bibtex参考文献生成方法，可以采用手动方法解决，当按常规的编译方法编译文档稳定后，采取如下步骤：
* 删除aux，toc，lof，lot文件
* 运行latex
* 最后一次运行bibtex
* 多运行几次latex直至文档稳定

如果不想手动处理，也可以使用notoccite宏包。

基于biblatex的参考文献生成方法，顺序编码累的样式使用“unsrt”规则，包括numeric，numeric-comp，以及对应传统unsrt的bst文件的样式trad-unsrt等等。biblatex不存在目录导致unsrt规则失效的问题，只要使用了sorting=none选项，biblatex就能正确处理好顺序。
比如：

```
\documentclass[twoside]{article}
%\usepackage[backend=biber,style=trad-unsrt]{biblatex}%
\usepackage[backend=biber,style=numeric,sorting=none]{biblatex}%
%\usepackage[backend=biber,style=gb7714-2015]{biblatex}%
\usepackage{filecontents}
\begin{filecontents}{\jobname.bib}
@inbook{IEEEexample:repeatedauthortwo,
  author    = "W. Dai and H. V. Pham and O. Milenkovic",
  title     = "comparative study of quantized compressive sensing schemes",
  booktitle =
    "IEEE Information Theory Workshop on Networking and Information Theory",
  year      = "2009"
}

@thesis{IEEEexample:masterstype,
  author        = "A. Karnik",
  title         = "Performance of {TCP} Congestion Control with Rate
                   Feedback: {TCP/ABR} and Rate Adaptive {TCP/IP}",
  institution   = "Indian Institute of Science",
  type          = "M. Eng. thesis",
  location      = "Bangalore, India",
  year          = "1999-01"
}

@ARTICLE{bernanke1989agency,
  AUTHOR = {Bernanke, Ben and Gertler, Mark},
  PUBLISHER = {JSTOR},
  DATE = {1989},
  JOURNALTITLE = {The American Economic Review},
  shortjournal={AER},
  KEYWORDS = {bernanke1989agency},
  PAGES = {14--31},
  TITLE = {Agency costs, net worth, and business fluctuations},
}
\end{filecontents}
    \addbibresource{\jobname.bib}

    \begin{document}
    \tableofcontents
        
    \section{one}
	ref: \cite{bernanke1989agency}

    \section{two\cite{IEEEexample:masterstype}}

    \section{three}
    ref:\cite{IEEEexample:repeatedauthortwo}
	
    \printbibliography
    \end{document} 
```


### 如何将参考文献条目引入到正文中？

理工科类论文很少用。人文类的期刊和出版物可能会有这样的需求，有时需要将引用文献的整个条目放入正文或者正文的脚注中。

传统的基于bibtex参考文献生成方法中，可以参考使用bibentry、inlinebib、jurabib等宏包，配合使用的bst样式文件，将文献条目放入正文。
而要把文献放入脚注可以使用footbib、inlinebib、jurabib等宏包。

基于biblatex的参考文献生成方法，可以把文献表(或者说详细的文献信息)放到文档的任何位置，包括正文中、文后、页脚处、边注处等等位置。这些要求一般由相应的文献样式来实现。比如：

```
\documentclass[twoside]{article}
\usepackage[backend=biber,citestyle=verbose-note,bibstyle=verbose]{biblatex}%alphabetic
\usepackage{filecontents}
\begin{filecontents}{\jobname.bib}
@ARTICLE{bernanke1989agency,
  AUTHOR = {Bernanke, Ben and Gertler, Mark},
  PUBLISHER = {JSTOR},
  DATE = {1989},
  JOURNALTITLE = {The American Economic Review},
  shortjournal={AER},
  KEYWORDS = {bernanke1989agency},
  PAGES = {14--31},
  TITLE = {Agency costs, net worth, and business fluctuations},
}
\end{filecontents}
\addbibresource{\jobname.bib}

\begin{document}
\section{references of verbose-note style}

first time: \footnote{\cite{bernanke1989agency}}
second time:\footnote{\cite{bernanke1989agency}}

\end{document} 
```

其中，标注样式verbose-note实现了在脚注中给出完整参考文献信息的方法，而如果将其换成verbose，那么将在正文中引入完整的文献信息。


### 如何将参考文献引入到目录中？

传统的基于bibtex的参考文献生成方法，可以使用tocbibind宏包进行控制。

基于biblatex的参考文献生成方法，可以使用printbibliography命令的选项来设定:
```
\printbibliography[heading=bibliography] %不加入目录
\printbibliography[heading=bibintoc] %加入目录
```



### 参考文献中的数字编号标签格式

传统的基于bibtex的参考文献生成方法，参考文献表中的数字格式是由 \@biblabel 控制的，可以通过重定义该命令来修改格式。比如将数字修改为左对齐：
```
\makeatletter
\renewcommand\@biblabel[1]{[#1]\hfill}
\makeatother
```

基于biblatex的参考文献生成方法，文献表中的数字标签格式，通常由参考文献样式决定。如果需要手动调整，可以采用修改域格式的方法，比如：
```
\DeclareFieldFormat{labelnumberwidth}{\ttfamily\mkbibbrackets{#1}\hfill}
```
其中#1是标签数字，`\ttfamily`设置了标签的字族，`\mkbibbrackets`设置用方括号包围数字，`\hfill`设置左对齐。



### 参考文献编号如何左对齐，右对齐？

基于biblatex的参考文献生成方法，默认情况下使用list环境来构造文献表，因此文献的数字编号标签是右对齐的。但可以通过对标签数字域格式的修改进行调整，比如：
```
\DeclareFieldFormat{labelnumberwidth}{\mkbibbrackets{#1}\hfill}
```
其中将带方括号的数字标签设置左对齐。
需要注意：通常标签的格式是由参考文献样式决定的，用户一般不需要做修改。





### 如何控制参考文献表中文献作者的数量？

传统的基于bibtex的参考文献生成方法，需要修改样式，即修改bst文件。

基于biblatex的参考文献生成方法，可以通过设置宏包选项来实现，maxbibnames=3设置最多出现的作者数为3，minbibnames=3设置当作者数超过maxbibnames值时，数量需减少至minbibnames。


### 如何减少参考文献条目行间距

传统基于bibtex的参考文献生成方法，文献条目间距为\itemsep，默认值4.5pt plus 2pt minus 1pt，可通过指令\addtolength{\itemsep}{距离}调整。当使用natbib包时，也可以利用设置间距\bibsep来调整。

基于biblatex的参考文献生成方法，由\bibitemsep 控制各条目的垂直间距，此外还有\bibnamesep，\bibinitsep 用于控制插入在两条姓名不同的条目之间的垂直间距和插入在两条首字母不同的条目之间的垂直间距。三个尺寸遵守\addvspace 的规则所得到的垂直间距取为三个间距中的最大值。


### 参考文献列表行距如何设置？

基于biblatex的参考文献生成方法，参考文献列表的行距与正文是一致的。由于文献表本质上与正文是一致的，因此所有正文中设置行距的方法均对其有效，而且可以将这些设置用编组局部化，避免影响文档的其它内容。关于各条目的垂直间距问题见前面的问题“如何减少参考文献条目行间距”。



### 从文献表到引用标注的反向超链接

传统的基于bibtex的参考文献生成方法，要使用反向超链接，可以使用backref或citeref宏包，其中backref是hyperref宏集的一部分，因此兼容性可能更好。

而基于biblatex的参考文献生成方法，只要加载biblatex时，使用backref=true选项，那么就能使用反向超链接。


### BibTeX参考文献中的URL和doi

传统的基于bibtex的参考文献生成方法，调用url或者xurl宏包即可正常使用url，也可以看看href宏包。对于doi也可以使用doi宏包。
 
基于biblatex的参考文献生成方法，由于biblatex自动载入url宏包，并利用biburlnumpenalty、biburlucpenalty、biburllcpenalty 三个计数器的值来控制url在数字/大写字母/小写字母处进行断行。计数器取值大于等于0但小于10000，等于0表示不断行。而是否在文献表中输出url由宏包选项url控制，url的格式则由所选样式中设置的域格式控制，url的字体由url宏包的字体控制命令设置。biblatex 中 doi格式与url格式相同。


### 使用超链接，如何去除颜色边框？

直接在引用 hyperref 宏包的时候使用以下命令之一 

```
\usepackage[hidelinks]{hyperref}
\usepackage[colorlinks]{hyperref}
```

第一种方法是隐藏链接，即隐藏颜色和边框。第二种方法是用不同颜色来替换默认的边框强调超链接的方式，但是这种方法会使得链接具有不同的颜色。如果需要设置各种链接的颜色可以参考 hyprref 的说明文档，值得庆幸的是，该宏包已经有了一个[中文翻译版](https://github.com/latexstudio/LaTeXPackages-CN/blob/master/hyperref/hyperref-zh-cn.pdf)。 




### 参考文献列表的字体字号如何设置？

传统的基于bibtex的参考文献生成方法，有两种方法，一是直接加命令，比如:
```
{
\small
\bibliography{bibfile}

}
```

而是使用natbib宏包，比如:
```
\def\bibfont{\small}
```



基于biblatex的参考文献生成方法，字体字号由命令bibfont控制，重定义该命令即做出设置，比如：
```
\renewcommand{\bibfont}{\fangsong\zihao{6}}
```
其中设置参考文献表内容的默认字体为仿宋，字号为6.


### 基于bibtex的方法和基于biblatex的方法各有哪些特点和优点？

基于bibtex的方法和基于biblatex的方法都是成熟的latex的参考文献生成方法，两者各有特点，要了解最好的方法是去看作者给出的资料，比如btxdoc和biblatex。当然前辈们给出意见也可以参考，下面综合一下tex exchange上各位大佬说法。首先理清一下术语。

bibtex有两种意思，一种是BibTeX格式，即参考文献数据库bib文件的格式。另一种是处理参考文献数据的程序bibtex。其中BibTeX格式由于bibtex程序的发明而得名。由于biblatex也支持bibtex格式，因此默认情况下我们讨论的bibtex通常是bibtex程序。因此需要比较两种方法其实是bibtex程序和biblatex宏包使用的biber程序，以及常与bibtex程序配合使用的natbib宏包与biblatex宏包之间的比较:


natbib是长期维护的latex宏包，使用广泛，稳定可靠。具有如下优缺点:
* 可以配合很多期刊和出版商开发的bst样式使用
* natbib作者提供的makebst工具可以用于bst样式开发
* 生产的参考文献列表代码可以直接拷贝进文档使用
* 由于依赖于bibtex，使用bst文件，其编程语言学习困难
* 引用标准主要包括作者年制和数字顺序编码制缺乏人文社科类文献常用的作者标题制或者脚注样式
* 文档中打印多各文献表需要使用其它宏包
* 由于依赖于bibtex，因此也继承了bibtex的所有缺点
当要提交的文档需要使用给定bst时或者当有要求使用natbib时可以使用该宏包。

biblatex则是包含biber程序的一个大型宏包，其优缺点有:
* 包含人文社科类常用的样式
* 支持更多更广的条目类型和域
* 更便捷的参考文献格式控制
* 提供了覆盖natbib的功能
* 所有的样式都是有tex宏控制容易学习和修改
* 多文献表，分类筛选非常容易
* 但一些期刊和出版商可能不接收使用biblatex的文档

bibtex的优缺点:
* 稳定且使用广泛
* 但修改样式困难，因为需要学习一门不同于tex的语言
* 能支持utf-8编码的bib文件，但不支持非ASCII字符的排序

biber的优缺点:
* 能处理bib文件中更多样的条目类型和域
* 可以处理utf-8编码的bib文件，也支持unicode字符的排序，更支持本地语言的排序调整，比如中文的按笔画数排序等
* 支持处bibtex格式外的更多格式的文献数据库文件
* 支持远程的数据库
* 支持其他格式的文献数据的输出
* 完全的unicode支持
* 可定制的排序机制
* 自动的姓名和姓名列表歧义处理
* 可定制的数据集成规则
* 自动的编码转换
* 非常灵活的数据映射(动态处理)
* 但只能与biblatex配合使用





### 要从基于bibtex的方法转换到基于biblatex的方法，需要做哪些改变？

1. 源文档中的命令需要改变，见前面的第一个问题。
2. bib文件一般不用改变，biblatex完全支持bibtex格式的bib文件。但如果需要应用一些biblatex特有的功能，可以做一些改动，比如:多语言处理是的langid域，比如列表形式的域比如出版地列表中各个出版地之间用and连接，比如使用date代替year，month，day，比如新的域如subtitle，titleaddon，maintitle，editortype等，比如使用bookauthor代替会议文件的editor等。
3. 编译命令需要改变从bibtex转换到biber，见前面的第一个问题。但如果使用latexmk编译，那么用户操作无任何变化。

 
### 常用的biblatex参考文献样式有哪些？

biblatex除了可以应用自带的标准样式外，还可以使用其他作者提供的第三方样式，这里介绍一些常用的样式：
* 国外常用
  * APA
  * MLA
* 国内
  * GB7714-2015

|样式名|用法|对应的bibtex样式|作者介绍|样式说明|
|:----:|:----|:----|:----|:----|
|trad-plain|`\usepackage[style=trad-plain]{biblatex}`|plain|MarcoDaniel and MoritzWemheuer，后者是biblatex维护者之一|将引文按字母顺序排序,比较次序为作者姓氏、出版年份和题名,如果不能顺序,将以在正文中的引用顺序为准。|
|trad-unsrt|`\usepackage[style=trad-unsrt]{biblatex}`|unsrt|MarcoDaniel and MoritzWemheuer|按照在正文中引用文献的先后顺序排列文献,其排版格式与trad-plain基本相同|
|trad-alpha|`\usepackage[style=trad-alpha]{biblatex}`|alpha|MarcoDaniel and MoritzWemheuer|用文献的作者姓氏前三个字母加出版年份的后两位数作为文献序号,如果出现相同的序号,则会根据排序结果在序号后追加字母以示区别，排序方法和排版格式与trad-plain相同|
|trad-abbrv|`\usepackage[style=trad-abbrv]{biblatex}`|abbrv|MarcoDaniel and MoritzWemheuer|将文献中作者名和月份名的拼写改为缩写, 显得文献信息紧凑简洁, 其排序方法和排版格式与trad-plain相同|
|ieee|`\usepackage[style=ieee]{biblatex}`|IEEEtran|Joseph Wright，biblatex 维护者之一|国际电气电子工程师协会IEEE期刊文献格式|
|apa|`\usepackage[style=apa]{biblatex}`|apalike|Philip Kime，biblatex 作者之一|American Psychological Association 的文献格式|
|Chicago|`\usepackage{biblatex-chicago}`|Chicago|David Fussner|for the Chicago Manual of Style|
|iso-numeric|`\usepackage[style=iso-numeric]{biblatex}`| |Michal Hoftich|ISO690 international standard numeric system|
|iso-iso-authoryear|`\usepackage[style=iso-iso-authoryear]{biblatex}`| |Michal Hoftich|ISO690 international standard nameanddate system,so-called Harvard style|
|gb7714-2015|`\usepackage[style=gb7714-2015]{biblatex}`|gbt7714-unsrt.bst by zepinglee|hushidong|中文文献著录标准 GB/T 7714-2015 顺序编码制|
|gb7714-2015ay|`\usepackage[style=gb7714-2015ay]{biblatex}`|gbt7714-plain.bst by zepinglee|hushidong|中文文献著录标准 GB/T 7714-2015 著者年份制|
|caspervector|`\usepackage[style=caspervector]{biblatex}`| |Casper vector|一种中文文献格式|
|nature|`\usepackage[style=nature]{biblatex}`| |Joseph Wright|for Nature|
|science|`\usepackage[style=science]{biblatex}`| |Joseph Wright|for Science|
|chem-acs|`\usepackage[style=chem-acs]{biblatex}`| |Joseph Wright|covers most American Chemistry Society journals|
|chem-angew|`\usepackage[style=chem-angew]{biblatex}`| |Joseph Wright|covers Angewandte Chemie Chemistry–A European Journal.|
|chem-biochem|`\usepackage[style=chem-biochem]{biblatex}`| |Joseph Wright|covers Biochemistry and asmallnumber of other American Chemistry Society journals|
|chem-rsc|`\usepackage[style=chem-rsc ]{biblatex}`| |Joseph Wright|covers all Royal Society of Chemistry journals|
|phys|`\usepackage[style=phys]{biblatex}`| |Joseph Wright|for AIP and APS|
|nejm|`\usepackage[style=nejm]{biblatex}`| |MarcoDaniel|for New England Journal of Medicine|
|mla|`\usepackage[style=mla]{biblatex}`| |James Clawson|for Modern Language Association|
|authortitle-dw|`\usepackage[style=authortitle-dw]{biblatex}`| |Dominik Waßenhoven|for Humanities|
|footnote-dw|`\usepackage[style=footnote-dw]{biblatex}`| |Dominik Waßenhoven|for Humanities|


### 更换biblatex参考文献样式后为什么编译出错？

基于biblatex的参考文献生成方法，由于样式文件的定制性，每个样式使用了定制了一些不同的内容，比如选项、域等等，可能导致相互间的不兼容，因此当出现错误时，清除一下旧的辅助文件，再次编译即可。


 
### 基于Plain TeX的BibTeX的使用

这个问题没有遇到过，不懂。




### BibTeX中过长的字符串

这个问题的真正需求不明确。没有遇到过。



## 六、字体篇
### 158. LaTeX字体是如何处理的

LaTeX 2ε目前的字体机制称为“新字体选择机制”（New Font Selection Scheme，NFSS）。它将文本字体分为五个互不干扰的属性（数学字体初学者不必过早了解）：
* 编码（encoding）。这个属性初学者暂时不必了解。在（pdf）latex和uplatex中，默认的西文编码称为OT1；在xelatex中，默认的编码称为EU2，就是Unicode。
* 字族（family）。一套成风格的字型的统称，如cmr、ptm（times）等。LaTeX 2ε预先定义了三个切换字族的命令：\rmfamily（衬线体）、\sffamily（无衬线体）、\ttfamily（等宽体）。
* 系列（series）。在一般的字体中一般表示字重（weight）。如粗体命令为\bfseries，正常粗细为\mdseries。
* 字形（shape）。在同一字族、同一系列下的风格差异，如斜体\slshape、意大利斜体\itshape、正体\upshape、小型大写\scshape。
* 字号（size）。以上四种变化是字型（typeface）的变化，而这是同一字型下不同大小的变化。LaTeX 2ε提供了成套的字号命令，如\normalsize、\small、\scriptsize等。

中文字体的方面，不同的中文解决方案的处理也有不同，这里就不介绍了。
### 159. 获取位图字体

### 160. PDF格式图片插入过程中的字形缺失

### 161. 为数学排版选择Type 1字体

### 162. Type 1字体配置

### 163. 切换到T1时字体变得模糊

### 164. 由于Ghostscript太旧造成字体模糊

### 165. 如何使用斜体

斜体一般是西文字体用的，在中文中不用斜体。
斜体这个名字比较误导，因为它对应英文的两个名字：倾斜体（slanted，指字形风格大致相同但是倾斜）和意大利体（italic，指字形设计为接近手写的形态，同时也就出现了倾斜）。
两种情况下分别有\slshape和\itshape两个命令，使用例如{\slshape slanted}及{\itshape italic}；也有把斜体内容作为参数的命令（推荐使用这种），如\textsl{slanted}及\textit{italic}。

### 166. 如何使用粗体

- \mathbf 

  \mathbf 会将数学模式取消再来取用字型，因此它加粗的不是数学符号，而是公式里的一般文字。\mathbf 只能在公式内部使用： 

  ```
  \documentclass{article}
  \begin{document}
  $\mathbf{equation: f(x,y) = \alpha x^2 + \beta y^2}$
  \end{document}
  ```

  ![mathbf](../images/mathbf.png)

- \boldmath 

  \boldmath可以将整套数学字体切换为粗体版本，这个命令只能在公式外使用： 

  ```
  \documentclass{article}
  \begin{document}
  \boldmath{$f(x,y) = \alpha x^2 + \beta y^2$}
  \end{document}
  ```

  效果如下： 

  ![boldmath](../images/boldmath.png)

- \boldsymbol

  amsmath 提供了一个 \boldsymbol 命令（由调用的 amsbsy 宏包提供），用于打破 \boldmath的限制，在公式内部将一部分符号切换为粗体： 

  ```
  \documentclass{article}
  \usepackage{amsbsy}%或者直接调用常用宏包amsmath
  \begin{document}
  $f(x,y) = \boldsymbol{\alpha x^2 + \beta y^2}$
  \end{document}
  ```

  效果如下： 

  ![boldsymbol](../images/boldsymbol.png)

- \bm 

  ```
  \documentclass{article}
  \usepackage{bm}
  \begin{document}
  $\sum x_i y_i$, 
  $\bm{\sum x_i y_i}$, 
  ${\bm \sum}{\bm x_i}{\bm y_i}$.
  \end{document}
  ```

  效果如下： 

  ![bm](../images/bm.png)

- \textbf

  ```
  \documentclass{article}
  \begin{document}
  \textbf{equation: $f(x,y)=\alpha x^2+\beta y^2$}
  \end{document}
  ```

  效果如下： 

  ![textbf](../images/textbf.png)

- \bfseries 

  \bfseries 影响之后所有的字符，如果想让它在局部生效，需使用花括号分组： 

  ```
  \documentclass{article}
  \begin{document}
  {\bfseries equation: $f(x,y) = \alpha x^2 + \beta y^2$}\\ 
  equation: $f(x,y) = \alpha x^2 + \beta y^2$.\\
  \bfseries equation: $f(x,y) = \alpha x^2 + \beta y^2$\\
  equation: $f(x,y) = \alpha x^2 + \beta y^2$.\\
  \end{document}
  ```

  效果如下： 

  ![bfseries](../images/bfseries.png)

参考：

Ishort-zh-cn

LaTeX入门，刘海洋。

<http://blog.sina.com.cn/s/blog_5e16f1770100nqwx.html> 

### 167. 如何设置文档字体为本机已安装字体？

### 168. 如何通过字体文件名来调用未安装本机字体？

### 169. 字体相对大小指令

\small 等命令对应的字体大小与文章 \documentlcass 中指定的字体有关，对应 10, 11, 12pt 三种全局字体大小的情况如下表所示，
```
      指令                        10pt    11pt    12pt
      \tiny                           5       6       6
      \scriptsize                 7       8       8
      \footnotesize            8       9       10
      \small                        9       10      10.95
      \normalsize              10      10.95   12
      \large                       12      12      14.4
      \Large                      14.4    14.4    17.28
      \LARGE                    17.28   17.28   20.74
      \huge                       20.74   20.74   24.88
      \Huge                      24.88   24.88   24.88
```
## 七、图片篇

### 170. LaTeX可以插图哪些类型的图片？

我们通常使用LaTeX、PDFTeX、XeTeX编译源文件。各种编译方式下图形格式支持如下
* LaTeX直接支持EPS、PS图形文件，间接支持JPEG、PNG等格式；
* PDFTeX直接支持PNG、PDF、JPEG格式图形文件，间接支持EPS；
* XeLaTeX直接支持BMP、JPEG、PNG、EPS、PDF图形格式

【注意】在使用PDFLaTeX时，如果要插入EPS，可以先把EPS转化为其他格式（比如PDF、JPEG、PNG、EPS），或者在导言区加载epstopdf，此宏包需要在graphicx宏包之后调用。更改图片格式可以使用ImageMagick或者类似[改图宝](http://www.gaitubao.com)等在线改图软件。

### 171. 在子文档中想用主文档所在文件夹下的子文件夹内的图片？

关键在于找到图片，直接暴力使用指定路径的方法，MWE如下：

```
main----subfile
     |--figure

main.tex in main folder, figure.png in figure folder, sub.tex in subfile folder.

main.tex:
% !TeX program = pdflatex
\documentclass{article}
\usepackage{graphicx}
\begin{document}
  \include{./subfile/sub1}
\end{document}

sub.tex:
% !TeX root = ../file.tex
\section{test}
hello! \LaTeX{}!
\includegraphics[width=\linewidth]{../figure/figure.png}
```

但是此种情况有问题，就是不能够使用 \graphicspath 指定插图路径。这个就留给后来人去解决吧。 

### 172. 图片的路径如何自动设置，不用正文一个个设置路径？

 可以使用指令graphicspath来设置图片路径，如：\graphicspath{{./figures/}} 即设定图片路径为当前目录下子文件夹figures。

### 173. 图片浮动如何控制？各自参数如何使用？

插图(figure)、表格(table)等浮动体浮动位置有四个选项可以控制，分别是 h -- here（当前位置）, t -- top （页面顶部）, b -- bottom（页面底部）和 p -- page（单独一个浮动页）。这四个位置选项的输入顺序是无所谓的，也就是说 [htbp] 和 [btph] 的效果是一样的。LaTeX 总是按照h-t-b-p的顺序依次尝试浮动，直到找到合适的位置。LaTeX 标准文档类中对位置参数的默认值是[tbp]，可以通过重定义内部命令\fps@figure 和\fps@table 来修改。 

```
\makeatletter
\def\fps@figure{htbp}
\def\fps@table{htbp}
\makeatother
```

LaTeX 放置浮动体时，浮动体不能造成页面溢出（overfull page），且只能放置于当前页或后面的页面中，浮动体根据其类型必须按源码内出现的顺序出现，也就是说，只有当之前的插图都被处理之后才能对下一幅插图进行处理，那么，只要前面有未处理的插图，当前位置就不会放置插图，一幅不可放置的插图将阻碍其后的图形放置，直到文件结束或出现\clearpage 等处理所有未处理浮动体的名令出现之处。 需要说明的是，对于两种浮动体类型，表格的排版和插图的排版是相互独立处理的，未处理的表格不会影响插图的布置。一般来说，给出的参数越多，排版的结果就越好，单个参数选项极容易引发问题，一旦浮动体不适合指定位置，将被搁置并阻碍接下来其他浮动体的处理，一旦被阻塞的浮动体超过LaTeX允许的最大值，还将产生错误。 LaTeX还设定了一些计数器来限制页面上浮动体的数量，这些包括： 

|    计数器    |                            含义                             |
| :----------: | :---------------------------------------------------------: |
| dbltopnumber | twocolumn 模式下可以位于页面顶部的浮动体最大数目（缺省为2） |
| topnumber | 可以位于页面顶部的浮动体最大数目（缺省为2）|
| bottomnumber | 可以位于页面底部的浮动体最大数目（缺省为1）|
| totalnumber | 可以位于文本页中的浮动体最大数目（缺省为3）|

LaTeX 还设定了一些比例参数控制浮动体的放置，包括：

| 参数          | 含义                            |
| ------------- | ------------------------------- |
| \textfraction | 文本页上文本最小比例（默认0.2） |
| \topfraction | 页面顶部浮动体高度比例（默认0.7）|
| \bottomfraction | 页面底部浮动体高度比例（默认0.3）|
| \floatpagefraction | 浮动页浮动体高度比例（默认0.5）|
| \dbltopfraction | twocolumn 模式下页面顶部浮动体高度比例（默认0.7）|
| \dblfloatpagefraction | twocolumn 模式下浮动页浮动体高度比例（默认0.5）|

这些计数器和比例值可以通过\setcounter 和\renewcommand 分别进行调整。但调整时应特别小心，不适当的比例值会导致非常糟糕的排版或大量未处理的浮动体。如果只是需要LaTeX在处理某一浮动体时忽略以上这些限制条件，可以在浮动体位置选项参数中加!即可。注意，! 对 浮动页限制条件的忽略无效。 

```
\begin{table}[!hbt]
  the contents of the table ...
\end{table}
```



### 174. 图文混排用什么方法实现？

大概有好几个宏包：picinpar、wrapfig，以及过时了的 picins 宏包。但是都有或多或少的问题，都不能够做得比较智能。等着后来人的修订以及更好的实现方式吧。 

- wrapfig 用法 

  ```
  \begin{wrapfigure}{行数}{位置}{超出长度}{宽度}
    <图形>
  \end{wrapfigure}
  ```

  - 行数 

    是指图形高度所占的文本行的数目，如果不给出此选项， wrapfig 会自动计算。 

  - 位置 

    是指图形相对于文本的位置，须给定下面四项的一个。 

    r,R    表示图形位于文本的左边。 

    l,L    表示图形位于文本的右边。 

    i,R    表示图形位于页面靠里的一边（用在双面格式里）。

    o,O    表示图形位于页面靠外的一边。 

  - 超出长度 

    是指图形超出文本边界的长度，缺省为 0pt。 

  - 宽度 

    指图形的宽度。 wrapfig 会自动计算 图形的高度。不过，我们也可设定图形的高度，具体可见 wrapfig.sty 内 的说明。 

- picinpar 用法 

  picinpar 宏包定义了一个基本的环境 window，还有两个变体  figwindow 和 tabwindow。允许在文本段落中打开一个``窗口 ''， 在其中放入图形、文字和表格等。这里我们主要讨论将图形放入文本段落 的用法，其它的用法可参考 picinpar 的说明。  

  ```
  \begin{window} [行数，对齐方式，内容，内容说明]\end{window}
  \begin{figwindow} [行数，对齐方式，图形，标题]\end{figwindow}
  ```

  - 是指“窗口”开始前的行数。 
  - 对齐方式是指在段落中“窗口'“的对齐方式。缺省为 l， 即左对齐。 另外两种是 c ：居中和 r ：右对齐 。
  - 第三个参数是出现在“窗口”中的“内容”，这在 figwindow 中就是 要插入的图形。第四个参数则是对``窗口''内容的说明性文字，这在  figwindow 中就是图形的标题。 

### 175. 并列插图如何进行排版

并列插图有3种情况：
* 并排摆放，各有标题。 

可以在figure环境中使用两个minipage环境，每个里面插入一幅插图。
```
\begin{figure}[htbp]
\centering
\begin{minipage}{60pt}
\centering \includegraphics[scale=0.4]{leftfigure.png} \caption{左边的图片} 
\end{minipage}
\hspace{10pt}%用来调整图片中间的间距
\begin{minipage}{60pt}
\centering
\includegraphics[scale=0.4]{rightfigure.png} \caption{右边的图片}
\end{minipage}
\end{figure}
```

* 并排摆放，共享标题 

通过使用两个\includegraphics命令
```
\begin{figure}[htbp]
\centering 
\includegraphics{leftfig.png} 
\includegraphics{rightfig.png} 
\caption{总标题} 
\end{figure}
```
* 并排摆放，共享标题，并且有各自的子标题

如果想要两幅并排的图片共享一个标题，并且各有自己的子标题， 可以使用 Steven D. Cochran 开发的 subfig 宏包。它提供的 \subfloat 命 令，并且总图和子图可以分别有标题和引用。 

```
\begin{figure}[htbp]
\centering
\subfloat[左边图片的标题]{
\label{fig:subfig_a} \includegraphics[scale=0.4]{leftfig.png} 
}
\hspace{10pt}% 用来调整两图中间的间距
\subfloat[右边图片的标题]{
 \label{fig:subfig_b}
 \includegraphics[scale=0.4]{rightfig.png}
} \caption{总标题} \label{fig:subfig} \end{figure}
```

此外，如果是并列的是两个有各自标题的插图，可以使用floatrow系列浮动体宏包，该宏包提供的floatrow环境可以并列图表等浮动体。

### 176. 并列子图如何进行排版

并列子图可以看看subfigure，subfloat等宏包。

### 177. 如果想让图片的题注在图片右侧，应该怎么做

可以利用盒子来实现这个功能。下面给出一个例子
```
\documentclass{article}
\usepackage{graphicx}
\begin{document}
    \begin{figure}
    \centering
    \includegraphics[width=0.45\linewidth]{figure.png}
    \parbox[b]{0.45\linewidth}{\caption{the content of caption}}
  \end{figure}
\end{document}
```
若要让题注在图片左侧，只需将 \parbox 那段代码移到 \includegraphics 之前。

### 178. 在插图较多，文字较少的情况下，正文会产生较多空白，或者单个图片占一页的情况，如何处理？ 

尽量避免这样的行文方式，比如可以将图片以附录形式集中排版。单个图片占一页在绝大多数情况下都不需要处理，浮动体页是很常见的形式。只有当图片恰好出现在一章的结尾，正文正好排满一页后换页，而图表本身尺寸又不大的时候，图表以浮动页排版方式排在页面正中有些突兀，这时可以通过浮动选项设置[!ht]要求其在页面顶部排版，并忽略latex从美学角度出发对浮动体做出的一些限制。 

### 179. 在双栏文档中，如何插入单栏图片，表格？ 

要看双栏文档是如何实现的。若双栏文档的实现方式是文档类的 twocolumn 选项实现的，那么用带*形式的浮动体环境替代原浮动体环境即可，这时的浮动选项只有tp有效；若双栏文档是以 multicol 宏包的 multicols 环境实现的，那么，在 multicols 环境内不支持浮动体，当需要插入单栏图片表格时，可结束multicols环境，待插入图片、表格后，重新开启multicols 环境。 

### 180. 不想让图片浮动，又想使用caption，如何二者兼得？ 

caption宏包提供了一个 `\captionof` 命令，可以在浮动体环境外使用，命令的语法格式是：`\captionof{<float type>}[<list entry>]{<heading>}`，举例如下： 

```
\begin{center}
\includegraphics{example-image.pdf}
\captionof{figure}{the example}
\end{center}
```

不过非常不建议使用这种方式，浮动体是一种很好的处理图表的方式。 

### 181. 有没有办法把图片固定在某位置

## 八、表格篇

### 182. 如何指定表格的总宽度

可以看看tabularx、tabu等宏包。 

### 183. 指定列宽度的表格如何使单元格内容居中

 指定宽度的表格列一般采用 p{<width>} 形式的列格式，这种列格式下，表格内容是两端对齐的，如果想使其成为居中对齐需要借助 array 宏包提供的功能，示例如下：
```
\usepackage{array} % this line in preamble
\begin{tabular}{c|>{\centering\arraybackslash}p{4cm}}
\hline
1  &  3.530  \\
2  &  456.0  \\
3  &  78.945 \\
4  &  3.65   \\
\hline
\end{tabular} 
```
而 `>{<format>}p{<width>}` 这样的格式在文档的应用过程中是非常不方便的，`array` 宏包同时提供了 `\newcolumntype` 宏命令可以将其定义为一个较为简短的格式，如：
```
\newcolumntype{z}[1]{>{\centering\arraybackslash}p{#1}}
```
从而可以在正文中使用
```
\begin{tabular}{c|z{4cm}}
\hline
1  &  3.530  \\
2  &  456.0  \\
3  &  78.945 \\
4  &  3.65   \\
\hline
\end{tabular}
```
类似的，采用 \raggedright 或 \raggedleft 替换\centering 可以使得单元格内容变成左对齐或右对齐。
### 184. tabularx 中的 X 列格式如何居中对齐

同样采用 array 宏包的 `>{<format>}` 方法，并利用 `\newcolumntype` 定义新的列格式，如：
```
\usepackage{array,tabularx}  % this line in preamble
\newcolumntype{Z}{>{\centering\arraybackslash}X} % this line in preamble
\begin{tabularx}{\linewidth}{ZZ}
\hline
1  &  3.530  \\
2  &  456.0  \\
3  &  78.945 \\
4  &  3.65   \\
\hline
\end{tabularx}

```
### 185. tabularx 中的 X 列格式，当单元格内容发生换行时，如何使同一行其他列的单元格垂直居中对齐？

对于指定宽度的表格列格式 p{<width>}，单元格内一旦进行换行，该单元格同一行内其他列的单元格内容均为垂直方向上顶端对齐，我们可以使用 array 宏包，以 m{<width>} 列格式或者 b{<width>} 列格式 替代 p{<width>} 格式即可实现垂直居中对齐或垂直底部对齐。对于 tabularx 中的 X 列格式，也是采用同样的思路实现，只是这里需要对 \tabularxcolumn 宏进行重定义如下：
```
\usepackage{array,tabularx}   % this line in preamble
\renewcommand{\tabularxcolumn}[1]{m{#1}}  % this line in preamble
```
以上则将同行的其他列单元格设置为垂直居中对齐。显然的，垂直底部对齐的设置方法是将重定义宏命令中的 `m{#1}` 替换为 `b{#1}` 即可。
### 186. booktabs的三线表，竖线为什么是不连续的？

宏包的作者为表格线的前后都增加了额外的sep，而且，宏包的作者认为三线表是不应该有竖线的。当然，如果你一定想要使用竖线，不妨以下面两个命令将表格线前后的sep设置为0pt。
```
\usepackage{booktabs} % this line in preamble
\setlength{\belowrulesep}{0pt}
\setlength{\aboverulesep}{0pt}
```
### 187. booktabs的三线表，竖线为什么是不连续的？

宏包的作者为表格线的前后都增加了额外的sep，而且，宏包的作者认为三线表是不应该有竖线的。当然，如果你一定想要使用竖线，不妨以下面两个命令将表格线前后的sep设置为0pt。 

```
\usepackage{booktabs} % this line in preamble
\setlength{\belowrulesep}{0pt}
\setlength{\aboverulesep}{0pt}
```



### 188. 表格的一列全是公式，有什么办法能输入简单些？

可以使用 array 宏包，>{ } 与 <{ } 可以为一列数据前后加上特定的宏命令。在一列数据前后均加上$则把这列数据放入数学模式中，举例如下：
```
\usepackage{array} % this line in preamble
\begin{tabular}{>{$}c<{$} c}
\hline
\multicolumn{1}{c}{function} &  value \\
g(x)     &  3.65   \\
f(x)     &  2.58   \\
\sin(x)  &  14.7   \\
\hline
\end{tabular}
```
第一列数据省去了输入数学模式起止符号 $ 的痛苦。对于不需要放入数学模式的单元格，比如表头，需要用 \multicolumn{1}{c}{xxx}的方式来保护一下，重新指定对齐方式。
### 189. 我的表格单元格内容是一个列表环境 (enumerate/itemize)，它和表格横线之间间距好大啊，怎么能把这些间距去掉？

把列表环境放入到 minipage 环境中即可，即使表格列格式采用的是`p{<width>}`格式。如果想让表格中数字小数点对齐要怎么做 

### 190. 如果想让表格中数字小数点对齐要怎么做

 可以借助 @ 的功能，如
```
\begin{tabular}{r@{.}l}
  \hline
  1 & 0 \\
  23 & 1 \\
  \hline
\end{tabular}
```
或者借助 warpcol 宏包提供的功能，如
```
\documentclass{article}
\usepackage{warpcol}
\begin{document}
\begin{tabular}{P{3.1}P{-2.1}}
  \hline
  \multicolumn{1}{c}{Label 1} & \multicolumn{1}{c}{Label 2} \\
  \hline
  123.4 & -12.3 \\
  12.3 & 12.3 \\
  1.2 & 1.2 \\
  \hline
\end{tabular}
\end{document}
```
还可以借助 array 和 dcolumn 的配合，如
```
\documentclass{article}
\usepackage{array,dcolumn}
\newcolumntype{d}[1]{D{.}{.}{#1}}
\begin{document}
\begin{tabular}{cd{3}}
  \hline
  1 & 3.14 \\
  2 & 27.12 \\
  3 & 78.095 \\
  \hline
\end{tabular}
\end{document}
```
### 191. 表格竖排

```
\documentclass{ctexart}
\usepackage[usestackEOL]{stackengine}

\begin{document}

\setlength\normalbaselineskip{11pt}
\strutlongstacks{T}
\begin{tabular}{|c|c|c|}
\hline
Foo bar & {\Centerstack{ 这 \\ 一 \\ 列 \\ 竖 \\ 排 }} & Foo bar \\
\hline
\end{tabular}

\end{document}
```
### 192. 跨页长表格

\usepackage{longtable}，做好对长表格跨页时的设置 

### 193. 双栏中表格过大怎么调整?

- 方法一：用 graphicx 宏包提供的 \raisebox 命令： 

  ```
  \raisebox{width}{height}{function}
  ```

  raisebox 会缩小 function 中的内容到 width 宽度、height 高度。你也可以指定其中一项，另一个用!占位，这样系统会自适应另一个参数，即相当于scale命令。 

- 方法二：用 table* 取代 table 环境，针对的是单栏表格。 

- 方法三：将表格中的字体缩小。 

- 方法四：使用横排：使用 rotating 宏包 

### 194. 如何制作列数可变的表格，例如试卷的计分表？

主要是使用 makecell 和 interfaces-makecell 宏包。下面给出一个 MWE。 

```
\documentclass{standalone}
\usepackage{ctex,calc,makecell,interfaces-makecell,CJKnumb,tabularx,multirow}

\newcounter{TotalPart}
\newcounter{SubColumn}
\newcounter{EmptyColumn}

\setcounter{TotalPart}{1}

% 计分表制作
\newcommand{\ScoreTable}{
 \setcounter{SubColumn}{\value{TotalPart}+2}
 \setcounter{EmptyColumn}{\value{TotalPart}+4}
 \begin{tabularx}{\textwidth}{|*{\theSubColumn}{X<{\centering}|}*{3}{c|}}
  \hline
   \multicolumn{\theSubColumn}{|c|}{\multirow{2}{*}{试卷卷面成绩}}
   & \multicolumn{1}{c|}{\multirow{3}{3em}{课程考核成绩占~\%}}
   & \multicolumn{1}{c|}{\multirow{3}{3em}{平时成绩占\,\%}}
   & \multicolumn{1}{c|}{\multirow{3}{3em}{课程考核成绩}}
  \\
   \multicolumn{\theSubColumn}{|c|}{}
   & & &
  \\
  \cline{1-\theSubColumn}
   \hfill 题 \hfill 号 \hfill~
   & \repeatcell{\theTotalPart}{text=\CJKnumber{\column}}
   & \hfill 小 \hfill 计 \hfill~
   & & &
  \\
  \hline
   \hfill 得 \hfill 分 \hfill~
   & \eline{\theEmptyColumn}
  \\
  \hline
 \end{tabularx}
}

\begin{document}

\ScoreTable

\end{document}
```

- CJKnumb 宏包是为了把阿拉伯数字转换为小写汉字序号。
- calc 宏包是为了做四则运算。
- tabularx 宏包是为了做列宽自动扩展的表格。
- multirow 宏包是为了合并单元格。
- makecell 是制作表格。
- interfaces-makecell 宏包提供了一系列命令，使得制作可变表格称为可能，同时简化了表格制作。 

### 195. 如何固定表格的总宽度？ 

### 196. 表格在单元格内如何换行？

可以通过限制列宽实现，例如下面的例子：

```
\begin{tabular}{|c|c|m{50mm}|}%这里用m则必须调用array宏包
\hline
a & b & \LaTeX{}表格固定列宽自动换行自动换行自动换行自动换行自动换行\\
\hline
a & b & \LaTeX{}表格固定列宽自动换行自动换行自动换行自动换行自动换行\\
\hline
a & b & \LaTeX{}表格固定列宽自动换行自动换行自动换行自动换行自动换行\\
\hline
\end{tabular}
```

### 197. 如何插入子图/表，各自分别带子标题，不带子标题？

### 198. 如何减小表格，插图，公式，列表等前后空白？

表格、插图、公式、列表的前后空白很多是由于不良的文本结构引起的，比如太短篇幅的正文，接连几级标题之间没有正文内容，甚至标题之间只有插图和表格等浮动体而没有任何说明的正文，这些都是不好的行文习惯，应杜绝这样的行文方式。此外，一些不良的代码写法也会引入较大的空白，如： 

```
\begin{center}
  \begin{figure}
  ...
  \end{figure}
\end{center}
```

或者 

```
\begin{figure}
  \begin{center}
  \includegraphics{x.pdf}
  \caption{the title}
  \end{center}
\end{figure}
```

而应该采用的方式是： 

```
\begin{figure}
\centering
\includegraphics{x.pdf}
\caption{the title}
\end{figure}
```

这是因为 center 环境本身就是一个 list 列表环境，其与上下文之间就有垂直间距，加上figure 浮动体与正文之间的间距，插图与正文之间的间距自然就变大了。 

### 199. 表格如何分页？

这个问题可见跨页长表格。 

### 200. 表格怎样可以旋转90度？

希望旋转90度的表格多半是由于过宽而需要进行横排，这里一个方法是使用 rotating 宏包，使用方法非常简单，用 sidewaytable 替代 table 即可，但这种表格不能实现跨页长表格（当然又宽又长的表格确实很少见）；另一个方法是使用lscape 宏包提供的 landscape 环境，进入横排状态，在其中使用相应的环境即可，这种方法可以实现跨页表格。 

### 201. 如何使用图表目录？

- \listoftables
- \listoffigures 

### 202. 图表如何使用双语标题

使用 bicaption 宏包或 ccaption 宏包。 

## 九、beamer篇

### 203. 隐藏导航栏

Beamer 自带的导航符号看起来很不错，但是实际上使用的并不多，为了让文稿的显示面积增加，减少干扰元素，我们可以隐藏下方的导航栏符号，两个方法如下：

```
\setbeamertemplate{navigation symbols}{}
\beamertemplatenavigationsymbolsempty % both ok
```

如果需要去掉下方 title，Author 等信息的话，可以用

```
\setbeamertemplate{footline} 
```
### 204. 向 Beamer 中添加参考文献

我们可以使用下面的命令添加参考文献，最好放在 `appendix' 后面。

```
\begin{frame}[allowframebreaks]{References}
\def\newblock{}
\bibliographystyle{plain}
\bibliography{mybib}
\end{frame}
```
### 205. 每节显示目录

在我们做一个比较长的报告时，我们可能会想在每一节添加一个目录，让听众清楚内容讲到哪了，我们可以在导言区添加如下的命令。

```
\setbeamerfont{myTOC}{series=\bfseries,size=\Large}
\AtBeginSection[]{\frame{\frametitle{Outline}%
                  \usebeamerfont{myTOC}\tableofcontents[current]}}
```
为了得到节的标题信息，我们会在帧与帧之间添加 `\section[short_title]{long_title}', 其中 	short_title	是短标题，用于 “页眉” 信息（header）显示。如果你不想要显示每帧的页眉信息（header），可以使用下面的命令。

```
\setbeamertemplate{headline}{}
```
### 206. 多栏显示

	有时候我们有图需要并排摆放，一个好方法是使用分栏，尤其是当两个图不同的高度的时候，然后在每一栏插入我们需要的图片。代码如下：

```
\begin{columns}[c] % Columns centered vertically.
\column{5.5cm}     % Adjust column width to taste.
\includegraphics ...
\column{5cm}
\includegraphics ...
\end{columns}
```
### 207. 添加 LOGO

在右下方添加 logo，直接用系统默认的命令就可以。

```
\logo{\includegraphics[width=0.08\textwidth]{logo500}}
```

如果需要在右上方添加 logo，可以用 TikZ 命令（需要用到 tikz 宏包）在 Frametitle 上添加。

```
\addtobeamertemplate{frametitle}{}{%
\begin{tikzpicture}[remember picture,overlay]
\node[anchor=north east,yshift=2pt] at (current page.north east) {\includegraphics[width=0.09\textwidth]{logo500}};
\end{tikzpicture}}
```
## 十、绘图篇

### 208. 如何利用Tikz画超过360º的角，并做好标注

下面解答来自<https://tex.stackexchange.com/questions/60295/drawing-angles-greater-than-360%C2%BA-intikz> 

```
\documentclass[11pt]{scrartcl}
\usepackage{tikz}
\usetikzlibrary{arrows}
\begin{document} 
\newcommand\bigangle[2][]{% 
\draw[->,domain=0:#2,variable=\t,samples=200,>=latex,#1]
plot ({(\t+#2)*cos(\t)/(#2)},
{(\t+#2)*sin(\t)/(#2)}) node[right=.5cm] {$#2^\circ$}
;}
\begin{tikzpicture}
\draw [thick] ( 0,0) -- (3,0);
\draw [thick] ( 0,0) -- (0,3); 
\draw [red,thick] ( 0,0) -- (400:3); 
\bigangle[blue,dashed]{400}      
\end{tikzpicture}
\end{document}
```

![tikz-90-1](../images/tikz-90-1.png)
![tikz-90-2](../images/tikz-90-2.png)



## 十一、开发篇-含LaTeX3

介绍宏开发技巧，宏包和模板类开发的常见问题。

### 209. 在阅读已有的宏包或者文类时，遇到未知的命令应如何处理

可以参照胡伟的《LaTeX2e文类和宏包学习手册》中的第四章-命令集注。
# 十二、常见错误提示﻿
* ! LaTeX Error: File `xxx.sty' not found.    \usepackage时，引用错误宏包名称或者本机未下载相应的宏包。解决方法为检查拼写，或TeXLive使用tlmgr安装宏包。
* ! LaTeX Error: File `xxx.cls' not found.    \documentclass时，引用错误文类名称或者本机未下载相应的文类。解决方法为检查拼写，或TeXLive使用tlmgr安装文类。
* ! Undefined control sequence.    编译遇到不存在的命令（未定义的控制序列）。解决方法为检查拼写，引用相应的宏包，或者定义该命令。
* ! Missing { inserted. 或者 ! Missing } inserted.    缺少分组的某个花括号。解决方法为仔细查找上下文对应的花括号。
* ! Missing $ inserted.    缺少数学环境，通常为把数学环境专用的命令用在普通文本模式。
* ! LaTeX Error:  Can be used only in preamble. 有许多命令只能用于导言区，如果在document 环境中用了这些命令，将显示上面的错误信息。
* ! LaTeX Error:  Counter too large.  计数器数值太大，一般是在需要以字母形式显示的计数器其数值超过了26。
* ! LaTeX Error:  \include cannot be nested. 在一个已经要用 \include 引入的文件中又使用了 \include 命令。
* ! LaTeX Error: Missing \begin{document} 这种情况可能是忘了输入\begin{document}，或者是在导言区中有可打印的文本，还有可能是编译中断时在 aux 等辅助文件中写入错误，对于后者，可以清理辅助文件后重新进行编译。
* ! LaTeX Error: No counter `xxx' defined. 调用某计数器，但该计数器并不存在。
* ! LaTeX Error: No \title given. 在给出 \title 声明之前就使用了 \maketitle 命令。
* ! LaTeX Error: Something's wrong--perhaps a missing \item. 导致这个问题一般是在列表环境中的文本不是由 \item 开始的。
* ! LaTeX Error: There's no line here to end. 在\par 或空行后调用命令\newline 或 \\ 。这里它们没有任何意义，如果需要额外竖直间距，应使用 \vspace 命令。
* ! LaTeX Error: Lonely \item -- perhaps a missing list enviroment. 在列表环境外使用了\item 命令。
# 十三、用法惯例
### 210. TeX编辑器中的魔法注释

在TeX中有单行注释命令为%，其后的文本主要是对源代码进行一些说明，它们会被TeX，LaTeX等排版引擎所忽略。但有些注释对专门的TeX相关编辑器来说，可能用特别的意义。在不同的TeX编辑器中，这魔法注释(magic comments）可能是不同的。
下面是一些例子：
* 指定TeX编译器
```
TeXStudio，TeXworks
% !TeX program = xelatex
 
TeXShop
%！TEX TS-program = xelatex  
```
同理，将 xelatex 变为 pdflatex，就可以强制调用 pdfLaTeX 编译器。
在代码中需要使用ifxetex宏包进行条件判断。
* 指定文档为 utf-8 编码
```
TeXworks，TeXStudio
% !TeX encoding = utf8
```
Winedt(由于Winedt对编码自动识别能力较弱，使用此注释比较必要，不然要手动设置)
```
% !Mode:: "TeX:UTF-8"
或者
% -*- coding: utf-8 -*-
 
TeXShop
%!TEX encoding = UTF-8 Unicode

```
* 指定主文档
```
TeXStudio
% !TeX root = filename
```
* 指定bib处理程序

用biber处理bib文件，可在文件头添加如下代码
```
TeXStudio
% !TeX TXS-program:bibliography = txs:///biber
```
将biber改为bibtex，就可指定bibtex处理bib文件。
* 为TeX编译器指定参数

有时在使用某些宏包时我们需要额外调用一些编译参数，例如 minted 宏包需要使用 --shell-escape，这时可用如下魔法注释实现该功能
```
TeXStudio
% !TeX TXS-program:compile = txs://xxelatex/[--shell-escape]
 
sublime text - latextools
%!TEX options = --shell-escape
 
texshop
% !TEX parameter = --shell-escape
```

下面是各种编辑器对神奇注释的支持情况

|编辑器|Encoding|Program|Root|Spellcheck|
|:----:|:----:|:----:|:----:|:----:|
|TeXShop|x|x|x|x|
|TeXStudio|x|x|x|x|
|TextMate|?|x|x|?|
|TeXworks|x|x|x|x|
|SublimeText|o|o|?|?|
|VSCode|o|o|?|?|
|Atom|o|x|x|o|
|Vim (vimtex)|o|x|x|o|
|Texpad|o|o|?|?|

**注意：**

- x：支持特性 
- o：不支持特性 
- ?：不确定

## 其它

### 211. LaTeX与数学软件(Mathematica, Maple,Sagemath等)

### 212. LaTeX与公式编辑器

### 213. MathJaX

**官网**：http://www.latexstudio.net
**微信公众号**：latex2015
**QQ 交流群**：91940767
