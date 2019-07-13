# MOT概念理解

#### 术语

- Trajectory（轨迹）

一条轨迹对应这一个目标在一个时间段内的位置序列

- Tracklet（轨迹段）：

形成Trajectory过程中的轨迹片段。完整的Trajectory是由属于同一物理目标的Tracklets构成的。

- ID switch（ID切换）：又称ID sw.

对于同一个目标，由于跟踪算法误判，导致其ID发生切换的次数称为ID sw.。跟踪算法中理想的ID switch应该为0。

- 数据关联 

数据关联是多目标跟踪任务中经常使用的典型的处理方法，用于解决目标间的匹配问题，这里的目标可以是detection responses，也可以是tracklets。

注： 所谓的“物理目标”，就是具有相同物理意义的目标，比如两幅图像都出现了“张三”、“李四”，那么两个“张三”就是同一物理目标，虽然有可能两幅图像中“张三”的形状、表观都发生了很大的变化。

- 检测响应 detection response

也称为“检测假设”、“检测观测量”。（detection response,detection hypotheses,detection observations）。是检测过程的输出量。


#### 评价指标
对于多目标跟踪，最主要的评价指标就是MOTA。
这个指标综合了三点因素：FP、FN、IDsw.。

FP即False Postive，为误检测的目标数量；

FN即False Negetive，为未检出的真实目标数量；

IDsw.即同一目标发生ID切换的次数。

MOTA越高，代表一个Tracker综合性能越好，上限为100，下限负无穷。

除此之外，多目标跟踪还有很多的评价指标，比如MOTP、IDF1、MT、ML、Frag等。作为入门，读者最需要关注的就是MOTA，其他指标可以等对MOT有了进一步了解后再关注。

MOTchallenge官网 列出了一些 [Evaluation Measures](https://motchallenge.net/results/MOT17/) 如下图。

![Evaluation Measures](../../MOT-Roadmap/sources/images/MOT_Benchmark_Evaluation Measures.png)


## 参考文献
[1]带你入门多目标跟踪（一）领域概述
作者：ZihaoZhao
网址：https://zhuanlan.zhihu.com/p/62827974

[2]Luo, W., Xing, J., Milan, A., Zhang, X., Liu, W., Zhao, X., & Kim, T.-K. (2014). Multiple Object Tracking: A Literature Review, 1–18. Retrieved from Multiple Object Tracking: A Literature Review