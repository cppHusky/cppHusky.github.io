# RGB

初始位置在 `puzzle.cpphusky.xyz/red`。

> 在本关我们只能看到一个色块，而通关所需要信息以背景色隐写在了色块中央。

*本关已给提示：去年解法，故技重施。*

## 解析

如果你在电脑上用鼠标划一下，就很容易发现 red 页面中的隐写内容 `1F`。手机也有可能看出隐写内容，你在屏幕中央长按一会儿就有可能选中对应文字。有的大神直接 Ctrl+A 一键发现隐写内容，确实可行。另外还可以按 F12 进行网页元素审查，一样能发现这个隐写内容。

接下来可以想一想，1F 和红色能让你联想到什么？有可能是色号。但倘若是色号的话，单纯一个红色 1F 是不能说明什么信息的，还应该有绿色和蓝色。

那么问题来了，绿色和蓝色应该到哪里去找呢？答案就在 url 中。原本的网址 url 是 `https://puzzle.cpphusky.xyz/red`，如果改成 `https://puzzle.cpphusky.xyz/green` 和 `https://puzzle.cpphusky.xyz/blue` 会怎么样呢？

哎，改完了之后发现还各有一个页面，其上的信息分别是 1E 和 33.这样一个色号就拼成了。

~~如果你游玩过一款创新立体 3D 节奏游戏《韵律源点 Arcaea》的话，你就会知道 #1f1e33 是由曲师 Camellia 制作的一首曲目（同时还是游戏主角对立的代表色）~~

但是，我们还始终没看到答题区域。那么最后尝试把这个色号放到 url 中，也就是 `https://puzzle.cpphusky.xyz/1f1e33`（这里我们设计了容错机制，大小写均可以），就会出现又一个页面。这里有四个答题框，终于有了答题区域。该页面还有一条隐写信息 C,M,Y,K，这是 CMYK 颜色表示法。下面的答题区总共有四个，看起来它们之间有着一一对应的关系。

随便百度一个“RGB 转 CMYK”，把 #1F1E33 这个色号转换成 CMYK，就会得到39, 41, 0, 80这个结果，填进去就通关了。

*关于提示：去年的[门对千棵竹](../2023/men-dui-qian-ke-zhu.md)就是改 url 的题目，今年又来一道改 url 的题，所以说是故技重施。*
