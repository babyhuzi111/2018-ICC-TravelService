# 2018-ICC-精品旅行服务成单预测

这是第二届智慧中国杯（ICC）中的一题：**[精品旅行服务成单预测](http://www.dcjingsai.com/common/cmpt/%E7%B2%BE%E5%93%81%E6%97%85%E8%A1%8C%E6%9C%8D%E5%8A%A1%E6%88%90%E5%8D%95%E9%A2%84%E6%B5%8B_%E7%AB%9E%E8%B5%9B%E4%BF%A1%E6%81%AF.html)**。我入赛的时间很晚，大约是赛程的后期了。我的队伍是“魂斗罗”，最终取得 **14th/1135** (**Top 1.23%**) 的成绩。这个比赛可以学到不少**从序列数据中挖掘特征的套路**。

## 从序列数据中挖掘特征的套路*

1. 由于用户最近的行为极可能代表了近期的想法，因此我保留了最近k天的行为与时间，作为k个特征；
2. 对最近k天的行为和时间进行统计，构建统计特征；
3. 对所有的行为和时间进行统计，构建全局统计特征；
4. 对时间序列进行一阶和二阶差分，保留最近的k个差分值，作为k个特征；
5. 对k个一阶和二阶差分值进行统计，构建统计特征；
6. 对所有的一阶和二阶差分值进行统计，构建全局统计特征；
7. 按行为分组后，对时间序列进行一阶和二阶差分，保留最近的k个差分值，作为k个特征
8. ……

诸如此类，实验表明，差分特征十分有效，是这个比赛提分的关键。

## 嘿！

如果您有任何的想法，例如：发现某处有 bug、觉得我对某个方法的讲解不正确或者不透彻、有更加有创意的见解，欢迎随时发 issue 或者 pull request 或者直接与我讨论！另外您若能 star 或者 fork 这个项目以激励刚刚踏入数据挖掘的我，我会感激不尽~