WzComparerX
====================

**WzComparerX**是继承WzComparer和WzComparerR2的下一代冒险岛Online资源提取器。


WzComparer的历史
--------------------

WzComparer项目最早启动于2010年6月，产生于Exprg冒险岛社区小组的闲聊中。当时世界上已经出现了很多冒险岛提取器，比如**HaRepacker**(Haha's repacker, HR), **wzextract**(Fiel), **火人提取器**，**Exrpg Extractor系列**等。Exrpg论坛在当时一直致力于冒险岛世界各个服务器更新内容的最新资讯，于是有人发出疑问，“为什么没有一个提取器能够对比客户端的详细变化呢？”。一周后，WzComparer第一个版本诞生。

WzComparer最初的版本非常简陋，它的基础代码完全是基于wzextract3.4的复制粘贴，因为wzextract是存在img级别变化对比功能的（基于img校验和的存档文件）。当时的作者对C#语言也并不熟悉（甚至连treeview控件也是第一次见），仅凭摸索与尝试，在很短的时间内完成了这个功能，并在KMST的下次更新实现了**基于客户端变化的精确对比**，于是WzComparer的名字由此诞生。

随后的三年，WzComparer也增加了大量和提取无关的功能，比如wz搜索与string.wz搜索模块，角色状态模拟与加点模拟，装备与buff模拟（也就是如今CharaSim的前身），与766数据库的联动自动更新模块（内部功能），简易地图模拟（初版中只能显示obj和tile的静态帧，没有动画），本地数据库（access文件数据库）。随着使用用户越来越多，以及功能的越来越臃肿难以维护，WzComparer进行了第一次重构，于2013年初开启了WzComparerR2项目（R即有revision，也有rebuild的含义），并于2015年初开源至github。

WzComparerR2在重构时，对原有wzextract中关于wz文件解析的部分完全重写，成为如今的wzlib，同时做了大量性能优化；裁剪了全部难以维护及不适宜公开的功能，如原来的角色面板模拟仅剩下了UI界面的空壳，仅保留装备道具的tooltip模拟，数据库功能全部移除，wz对比也由原来的UI显示简化为生成html报告；添加了更多“有趣”功能，如真正的补丁安装，音乐播放器，完整的地图模拟，纸娃娃模拟等。WzComparer比起“对比器”(comparer)，更多地成为了“仿真器”(simulator)而被大众所知了。

同时，WzComparerR2也成为作者本身对于新技术挑战与尝试的试验田，如ribbon window、bass library、xna/monogame、TSF-IME、libapng、spine的应用，都是作者初次应用在一个正式项目中，也因此积累了很多版权上不合规与功能难以维护的隐患。比如bass.net与spine的版权问题至今未能妥善处理，monogame与emptykeysUI停留在老旧的版本，使用了大量反射代码修复内存泄露的bug与不当的使用。同时作者因工作繁忙以及对游戏的疏远，于2018年后便暂停了主要功能的开发，仅剩下不定时的CharaSim维护工作了。


WzComparerX是什么
--------------------

WzComparerX意为WzComparer十周年特别版（源自iPhoneX或SurfaceX），它是WzComparerR2的下一代版本。

WzComparerX致力于如下目标：

- 基于.net core或.net 5开发，全部第三方库使用nuget引入，并开源全部未公开的库。
- 对于配置文件与全局对象的架构重构。
- 重构且重新设计UI，使其更适用于版本管理，并符合现代桌面应用的布局。
- UI与数据分离，使得纸娃娃可以被移植或复用。
- 多语言支持。
- 重新设计的插件系统。
- MapRender的性能优化。
- 完成WzComparerR2中遗留的不完善功能，如动画保存选项，纸娃娃的导出等。

但这更像是一个愚人节笑话，因为作者并没有时间^_^

冒险岛已经是诞生近20年的老游戏，作者如今已过中年，很难为这样一个古老的游戏与软件全力以赴了。(~I have to work for food~)

如今WcR2开源已多年，有很多开发者完成了非常繁重的本土化工作与功能维护，非常感谢大家十年如一日的支持与付出。

如果你有意承担WzComparerX的设计与开发工作，欢迎联系作者:)


轶闻
--------------------
- *WzComparer*的工程名实际为*WzCompare*，少了一个字母。
- 当初提出WzComparer设想的人网名叫做*大杰*，如今已无法联系了。
- Wc与WcR2的icon素材，均来自于item.wz。
- 在社区中大家更习惯简称为*R2*，而作者本人更喜欢简称为*上厕所*。
