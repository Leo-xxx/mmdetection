## 目标检测用这个就够了！多家机构联合提出MMDetection工具箱助力目标检测新发展

让创新获得认可 [CVer](javascript:void(0);) *今天*

点击上方“**CVer**”，选择加"星标"或“置顶”

重磅干货，第一时间送达![img](https://mmbiz.qpic.cn/mmbiz_jpg/ow6przZuPIENb0m5iawutIf90N2Ub3dcPuP2KXHJvaR1Fv2FnicTuOy3KcHuIEJbd9lUyOibeXqW8tEhoJGL98qOw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

> 本文授权转载自：将门创投（thejiangmen）

![img](https://mmbiz.qpic.cn/mmbiz_png/ibaXaPIy7jV2FZSMKYUasEeBgQibJ5zVNFjt2dO555VjdZ2VcRIuka6zokcNBxxgdyyDhdPCNaibS6KBXmNAiaQDqQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

*From: Github  编译: T.R*



目标检测作为视觉领域的重要任务，近年来在研究人员的共同努力下取得了丰硕的成果，包括一系列算法、数据、开源工具等等。为了向学术届和工业界提供更多完善灵活的工具和模块化部件，多个大学和机构的研究人员联合提出了目标检测工具箱**Open MMLab Detection**，将有效促进目标检测领域的应用和新方法研究发展。



![img](https://mmbiz.qpic.cn/mmbiz_jpg/ibaXaPIy7jV2FZSMKYUasEeBgQibJ5zVNFObxdibicpiaJaiayKNG3BDcCZISKGzcC7HFicicEpfcsCTwQUMGSpibnVlUZg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



MMDetection工具箱主要有如下特点：



首先是*模块化*的设计：研究人员将目标检测的网络架构分解成不同的原件，并构建了多样化的模块似的用户可以根据需要构建个性化的检测架构；



支持*多样化*的模型架构：包括单阶段，双阶段和多阶段的检测架构都可以通过这一工具箱轻松构建；



*高性能*计算：所有的基础元件和模块都进行了GPU实现，可以实现最先进的训练速度；



*优异的目标检测*性能：这一工具箱由2018年COCO目标检测团队**MMDet**主导开发，并不断在前沿表现的基础上提升着模型性能。



#### 工具箱的主要架构  

研究人员将目标检测架构拆解成了多个通用部分，并将每一部分标准化和模块化。



![img](https://mmbiz.qpic.cn/mmbiz_jpg/ibaXaPIy7jV2FZSMKYUasEeBgQibJ5zVNFHRIibQIcNBzwjnczHiaHpIPHraBibatw6YeWF38ASjIYSSJtsr2ugvrtA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

单阶段和量阶段检测器的元件分解图

######  

**主干网络**(backlbone)：其作用是从图像中抽取特征，将图像从像素空间转换到高维的特征空间中去，例如VGG和ResNet-50等都是常用的主干网络;


**衔接部分**(Neck)：用于连接主干网络与头部结构，它的作用是重新配置或者优化由主干网络生成的初始特征图，特征金字塔网络就是一种典型的衔接部件；


**密集连接头**(DenseHead)：用于在特征图上进行密集的位置相关操作，包括AnchorHead、AnchorFreeHead等，其中RPN、Retina、FCOS等Head是具有代表性的操作；


**ROI抽取器**：用于从单个或多个特征图中抽取出每个RoI对应的特征，例如SingleRoIExtractor.


**感兴趣区域头**(RoIHead)：将RoI特征作为输出并计算出对应的任务结果，包括bbox的位置、分类或者分割的预测结果。


通过这些通用模块，工程人员或研究人员可以构建出自己的检测器，并在此基础上进行更深入地开发和探索。



![img](https://mmbiz.qpic.cn/mmbiz_jpg/ibaXaPIy7jV2FZSMKYUasEeBgQibJ5zVNFSKDqCAkIUOWu18ChicSEXbPWh9dY4aBX1VOjfwTyaCk2bBhd4n8DlIw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

标准的训练流程


同时在这一工具箱中将训练过程总结成了一个标准的、适用于多种视觉任务的通用流程。其中训练和验证流程可以循环进行，在每个周期将在模型上运行多次前传和反传操作。



为了让流程为便捷和个性化，研究人员定义了最小流程单位；同时也支持多种用户自定义操作和时间节点，并可以利用钩子触发对应的时间节点及对应操作。



#### 涵盖丰富的模块和架构  

下表展示了目前MMDetection中包含具有代表性的模型架构，包括了单阶段、两段和多级的多种目标检测及分割方法。



![img](https://mmbiz.qpic.cn/mmbiz_jpg/ibaXaPIy7jV2FZSMKYUasEeBgQibJ5zVNFx78Yqd4U0T9kKwQQgO7G0RicoOibnkJsZr9S58zxFnhsic6ckqmVMSjlg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


这一工具箱支持的检测模型完整列表如下，数量上远远超过了其他现有目标检测代码库：



![img](https://mmbiz.qpic.cn/mmbiz_jpg/ibaXaPIy7jV2FZSMKYUasEeBgQibJ5zVNFTxBm472EicZx0jYwrSDicFNRZwY8rHGYxOcrrMmJRC6sKKS6dhmIHqQQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


此外还包括了各种先进的模块方法实现：



![img](https://mmbiz.qpic.cn/mmbiz_jpg/ibaXaPIy7jV2FZSMKYUasEeBgQibJ5zVNFV7tI6LxgiaP4L0oHI1nb24ZQccx85VaVhRDynOhgKKLFPQJicaJ5VXHw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


为了比较这一工具包中各个模块的性能，研究人员在模型性能、速度和内存的方面进行了比较。同时也在不同GPU及GPU节点上对代表性模型的表现进行测评。结果如下图所示：



![img](https://mmbiz.qpic.cn/mmbiz_jpg/ibaXaPIy7jV2FZSMKYUasEeBgQibJ5zVNFmhXmdnq3QQoDyCn7giaj7HwFR4h9bUDvzYnlSkrzAFtTVHDl6ib6sJ8g/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

###### 与先前的三个目标检测工具箱进行了性能、速度和内存开销方面的对比  

下图展示了典型模型在不同GPU和多个分布式架构上的拓展能力：



![img](https://mmbiz.qpic.cn/mmbiz_jpg/ibaXaPIy7jV2FZSMKYUasEeBgQibJ5zVNFYoeEwm4cF72grrwqu8EsFqP23PfxD6QN9VD9sPHrBxrOtmvXaibj8QQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)![img](https://mmbiz.qpic.cn/mmbiz_jpg/ibaXaPIy7jV2FZSMKYUasEeBgQibJ5zVNF89icZamGkevAviaTWkLD5vMq7PsOudPyiaUuSuictjkQsA5z602Ffc0SHg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


此外研究人员还对归一化、损失函数、训练规模以及各种超参数进行了详细的分析和对比，如果想要了解更多细节请参看：

*https://arxiv.org/pdf/1906.07155.pdf*



如果在学习研发中需要使用工具箱，代码和部署工具可以在这里找到，其中包含了200多个网络模型和模块工具：

*https://github.com/open-mmlab/mmdetection*



*ref:**http://mmlab.ie.cuhk.edu.hk/index.html*
*https://github.com/open-mmlab/mmdetection/tree/master/mmdet*
*https://arxiv.org/pdf/1906.07155.pdf*
*https://github.com/NVIDIA/apex*

*picture from:https://dribbble.com/shots/5075555-Toolbox*

*https://dribbble.com/shots/3000321-Toolbox*





-The End-



**CVer-目标检测交流群**



扫码添加CVer助手，可申请加入**CVer-目标检测交流群。****一定要备注：****研究方向+地点+学校/公司+昵称**（如目标检测+上海+上交+卡卡）

![img](https://mmbiz.qpic.cn/mmbiz_jpg/yNnalkXE7oX7pdpBKibicSnmb8wRGicbT0Rhr61k0f922lbXcowibk5DTRibROvFB1yMCAZQvj1iaEe6Qsia9bU0UMJCA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

▲长按加群



![img](https://mmbiz.qpic.cn/mmbiz_png/e1jmIzRpwWg3jTWCAZ4BrnvIuN20lLkhIjtg4GRSDhTk9NpeF0GGTJwUpKPatscIQU7Ndj9hgl8BPpGj2BJoFw/640?tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

▲长按关注我们

**麻烦给我一个在看****！**

[文章转载自公众号![将门创投](http://wx.qlogo.cn/mmhead/Q3auHgzwzM7JT1FAEQN32XrRB5ickep43amP1ibbDffMv0cQHcFezlzw/0) **将门创投** ](https://mp.weixin.qq.com/s?__biz=MzUxNjcxMjQxNg==&mid=2247490003&idx=2&sn=5c03c0a7a77deebd7e3eb634cbf98578&chksm=f9a26b5cced5e24a063af2050044b714fd28c45b1b40faceb6ebe8004dab5e4b9ce5d03b2137&mpshare=1&scene=1&srcid=&key=0aa21025b9197e7fb3b98b2114dd11e64bd69904e5751f9e34afea7ddc808f2923d94289df2b3517e79b28073b9316f312b3573924d5981adae9be82cc36c72d98c0ff2b8426a93a200321b5052b6a03&ascene=1&uin=MjMzNDA2ODYyNQ%3D%3D&devicetype=Windows+10&version=62060833&lang=zh_CN&pass_ticket=jJHZ56qUmcawBtALjsCbszM%2FtYNdeb3juLOgmsKAFv6POnCM9SuNoUc%2BqSiqYoLU##)





![img](https://mp.weixin.qq.com/mp/qrcode?scene=10000004&size=102&__biz=MzUxNjcxMjQxNg==&mid=2247490003&idx=2&sn=5c03c0a7a77deebd7e3eb634cbf98578&send_time=)

微信扫一扫
关注该公众号