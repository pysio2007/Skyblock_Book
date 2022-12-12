# 小人模拟

{% hint style="info" %}
本文由上古编写与2022/10/15
{% endhint %}

前一段时间我们能看到一个小传言：小人的收益改了，削到了10%。

以上说法不完全准确，而且是因为bug导致的，截至上周已经修复。

之所以没有这么快跟大家说是因为最近忙一些也没有跟进论坛的进度，目前已经修复。

先给大家说说到底发生了啥。

以下翻译自上个月中旬的Hypixel论坛原帖。

\-------------

We've noticed that a few players are unable to join the game.

It looks like the cause is minion simulation on login.

While we optimize the simulation, we've reduced the actions limit accumulated on minions while offline from 100k to 14k

我们注意到一些玩家无法进入游戏。

似乎是由于登录时小人模拟计算导致的。

随着我们优化了模拟系统，我们减少了小人在离线时累积的行动数，从10万到了1万4千(14%)。

If you couldn't log on your island, then you probably can today (might require 2 attempts).

But with that setup, your offline resources will cap out in about 1 day instead of 10 days.

如果你之前无法登陆，今天应该就可以了。（可能需要多尝试几次）

We are working on a better solution to minion simulation, after which the limit will be upped again.

Thank you for your understanding.

我们正在寻找一个更好的方式去完成小人的模拟运算，在此之后这个限制会被再次放开。

感谢您的理解。

Update 10/05/22: Minion simulation has been optimized and there is no longer a cap!

截至2022年10月5日：小人模拟已经优化并且目前不存在限制了。

\-------------

也就是说10%收益说法不准确，应该是14%的收益累计上限，而不是小人工作速度慢了。

根据我今天上线的情况，大概也给大家简单分析一下小人的计算系统。

以前的计算系统就是百分百的模拟，一个动作接一个动作，直到你箱子以任何形式占满了，占位置的包括enchanted过的和没有的。

就以雪小人为例。

以下核能，省流看这里：现在箱子更废了，住校党挂小人可以比以前存的更久，雪小人挂3k然后中箱子可以存两周的收益（以前是一周多一点）。

\-------------

正常雪小人我们应该用的都是超级压缩器3000+钻石传播组件，产物有钻石，附魔钻石，附魔钻石块，附魔雪块，雪球。雪球需要640个才能压缩为附魔雪块，也就是十组，附魔钻石两组半一压缩，钻石两组半一压缩。

雪小人十一级基础仓储15格，额外上一个中型箱子9格。一共24格，主产物为附魔雪块，杂项物品最终占地：雪球10格，附魔钻石块1格，附魔钻石3格，钻石3格，共17格。可以容纳主产物仅7格，目前水晶+附魔岩浆桶工作间隔为5.2s，需要工作320次得到一压缩雪块。

可以容纳最长的收集间隔时间：745,472s 折合约207h，8.6天。

但是今天我上号看到了一个奇观：我大约10天以上（差不多两星期）没有来看这边的小人了，但是没有满仓！

根据以往经验应该全部爆仓了，最终生成2个附魔钻石块。

![](../.gitbook/assets/0)

以上是雪小人加上diamond spreading生成钻石的概率，看不懂的说结论就是，每工作一次可以认为是产生0.4颗钻石（最终向下取整）。

一个附魔钻块需要160x160颗钻石，也就是工作128k次，665,600s，约185h

也就是说我的收益累积了起码15天了。

而且不出意料，上线挂机五分钟，全部显示仓满

也就是说现在的小人模拟从完全的小人动作模拟变成了：在线时实时动作模拟，离线时简单粗暴的算一下离线时间得出动作数量，然后直接计算最终产物，不存在以上“半成品占格子这种说法”。

省略过程再次粗算：你能挂大概3周多不爆仓，但是上线注意一定要收，已经爆仓后的雪小人不工作。

最终结果会导致箱子更废物了，以前两星期一收小人需要挂large storage，但是现在medium就够了。

核能预警：铁块价格肯定更容易崩了，因为我认识一些挂铁小人几十年不上线的家伙。
