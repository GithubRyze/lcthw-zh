# 练习0：准备

> 原文：[Exercise 0: The Setup](http://c.learncodethehardway.org/book/ex0.html)

> 译者：[飞龙](https://github.com/wizardforcel)

在这一章中，你将为C语言编程配置好你的系统。一个好消息是对于所有使用Linux或者Mac的人，你的系统是为C语言编程而设计的。C语言的创造者也对Unix操作系统的创造做出了贡献，并且Linux和OSX都是基于Unix的。事实上，安装工作会非常简单。

对于Windows上的用户，我有一个坏消息：在Windows上学习C非常痛苦。你可以在Windows上编写C代码，这并不是问题。问题是所有的库、函数和工具都和其它的C语言环境有些诧异。C来自于Unix，并且和Unix平台配合得比较好。恐怕这是一个你并不能接受的事实。

然而你并不需要为此恐慌。我并不是说要完全避免Windows。然而我说的是，如果你打算已最短的时间来学习C，你需要接触Unix并适应它。这同时也对你有帮助，因为懂得一些Unix的知识，也会让你懂得一些C编程的习惯，以及扩充你的技能。

这也意味着每个人都需要使用命令行。嗯，就是这样。你将会进入命令行并且键入一些命令。不要为此感到害怕，因为我会告诉你要键入什么，以及结果应该是什么样子，所以你实际上会学到很多东西，同时扩充自己的技能。

## Linux

在多数Linux系统上你都需要安装一些包。对于基于Debian的系统，例如Ubuntu你需要使用下列命令来安装一些东西：

```
$ sudo apt-get install build-essential
```

上面是命令行提示符的一个示例。你需要接触到能输入它的地方，找到你的“终端”程序并且运行它。接着，你会看到一个类似于`$`的Shell提示符，并且你可以在里面键入命令。不要键入`$`，而是它后面的东西。

下面是在基于RPM的Linux系统，例如Fedora中执行相同安装工作的方法：

```
$ su -c "yum groupinstall development-tools"
```

一旦你运行了它，它会正常工作，你应该能够做本书的第一个练习。如果不能请告诉我。

## Mac OSX

在 Mac OSX上，安装工作会更简单。首先，你需要从苹果官网下载最新的`XCode`，或者找到你的安装DVD并从中安装。需要下载的文件很大，要花费很长时间，所以我推荐你从DVD安装。同时，上网搜索“安装xcode”来指导你来安装它。

一旦你安装完XCode，可能需要重启你的电脑。你可以找到你的中断程序并且将它放到快捷启动栏中。在本书中你会经常用到中断，所以最好将它放到顺手的区域。

## Windows

对于Windows用户，你需要在虚拟机中安装并运行一个基本的Ubuntu Linux系统，来做本书的练习，并且避免任何Windows中安装的问题。

> 译者注：如果你的Windows版本是Win10 14316及之后的版本，可以开启Ubuntu子系统来获取Linux环境。

## 文本编辑器

对于程序员来说，文本编辑器的选择有些困难。对于初学者我推荐他们使用[`Gedit`](http://projects.gnome.org/gedit/)，因为它很简单，并且可以用于编写代码。然而，它在特定的国际化环境中并不能正常工作。如果你已经是老司机的话，你可以选用你最喜欢的编辑器。

出于这种考虑，我打算让你尝试一些你所在平台上的标准的用于编程的文本编辑器，并且长期使用其中你最喜欢的一个。如果你已经用了Gedit并且很喜欢他，那么久一致用下去。如果你打算尝试一些不同的编辑器，则赶快尝试并选择一个。

最重要的事情是，不要纠结于寻找最完美的编辑器。文本编辑器几乎都很奇怪，你只需要选择一个并熟悉它，如果你发现喜欢别的编辑器可以切换到它。不要在挑选它和把它变得更好上面花很多时间。

这是亦可以尝试的一些编辑器：

+ Linux和OSX上的[`Gedit`](http://projects.gnome.org/gedit/)。
+ OSX上的[`TextWrangler`](http://www.barebones.com/products/textwrangler/)。
+ 可以在终端中运行并几乎在任何地方工作的[`Nano`](http://www.nano-editor.org/)。
+ [`Emacs`](http://www.gnu.org/software/emacs/)和[`Emacs OSX`](http://emacsformacosx.com/)。需要学习一些东西。
+ [`Vim`](http://www.vim.org/)和[`Mac Vim`](http://code.google.com/p/macvim/)。

每个人都可能选择一款不同的编辑器，这些只是一部分人所选择的开源编辑器。在找到你最喜欢的那个之前，尝试其中的一些，甚至是一些商业编辑器。

## 警告：不要使用IDE

IDE，或者“集成开发工具”，会使你变笨。如果你想要成为一个好的程序员，它会是最糟糕的工具，因为它隐藏了背后的细节，你的工作是弄清楚背后发生了什么。如果你试着完成一些事情，并且所在平台根据特定的IDE而设计，它们非常有用，但是对于学习C编程（以及许多其它语言），它们没有意义。

> 注

> 如果你玩过吉他，你应该知道TAB是什么。但是对于其它人，让我对其做个解释。在音乐中有一种乐谱叫做“五线谱”。它是通用、非常古老的乐谱，以一种通用的方法来记下其它人应该在乐器上弹奏的音符。如果你弹过钢琴，这种乐谱非常易于使用，因为它几乎就是为钢琴和交响乐发明的。

> 然而吉他是一种奇怪的乐器，它并不能很好地适用这种乐谱。所以吉他手通常使用一种叫做TAB（tablature）的乐谱。它所做的不是告诉你该弹奏哪个音符，而是在当时应该拨哪根弦。你完全可以在不知道所弹奏的单个音符的情况下学习整首乐曲，许多人也都是这么做的，但是如果你想知道你弹的是什么，TAB是毫无意义的。

> 传统的乐谱可能比TAB更难一些，但是会告诉你如何演奏音乐，而不是如果玩吉他。通过传统的乐谱我可以在钢琴上，或者在贝斯上弹奏相同的曲子。我也可以将它放到电脑中，为它设计全部的曲谱。但是通过TAB我只能在吉他上弹奏。

> IDE就像是TAB，你可以用它非常快速地编程，但是你只能够用一种语言在一个平台上编程。这就是公司喜欢将它卖给你的原因。它们知道你比较懒，并且由于它只适用于它们自己的平台，他们就将你锁定在了那个平台上。

> 打破这一循环的版本就是不用IDE学习编程。一个普通的文本编辑器，或者一个程序员使用的文本编辑器，例如Vim或者Emacs，能让你更熟悉代码。这有一点点困难，但是终结果是你将会熟悉任何代码，在任何计算机上，以任何语言，并且懂得背后的原理。

> > 译者注：和Python不同，使用编辑器和命令行编写并编译C语言存在依赖配置问题。对于Python这种脚本语言，项目中文件之间的所有依赖都存在于代码中，命令行中只需要运行`Python`，解释器便于自动加载依赖。但是在C的Makefile中你需要手动配置`.c`文件的依赖，如果文件多于5个会非常麻烦。对此你需要找到一种通用的解决方案，或者还是直接使用IDE。