# RSpapers
### 我整理的一些推荐系统相关的论文

主要是跟我研究相关的论文

---

* **Tag-aware RS：** 基于标签的推荐系统，使用标签来提高推荐准确率等
* **Attention Based RS：** 采用Attention机制的论文
* **realtime RecSystem：**  实时推荐系统
* **temporal dynamics :**  考虑动态时序的推荐系统


## Tag-aware RS
#### 1-liang2018-TRSDL Tag-Aware Recommender System
#### 2- Towards A Standardized Tag Recommender Benchmarking Framework 
[http://www.dominikkowald.info](http://www.dominikkowald.info/)
[github](https://github.com/learning-layers/TagRec)
发现了tag领域同道中人的github ，万岁！！o(*≧▽≦)ツ┏━┓
## Attention Based RS
#### 1-  NAIS: Neural Attentive Item Similarity Model for Recommendation.
[code](https://github.com/AaronHeee/Neural-Attentive-Item-Similarity-Model)
item similarity 
#### 2-MTNet:Neural Approach for Cross-Domain Recommendation with Unstructured Text
cross domain
#### 3-Neural Collaborative Filtering
[论文导读](https://www.paperweekly.site/papers/notes/390)
[pytorch实现](https://towardsdatascience.com/paper-review-neural-collaborative-filtering-explanation-implementation-ea3e031b7f96)
[keras实现(原版)](https://github.com/hexiangnan/neural_collaborative_filtering)
这篇论文导读给我一种“这才是论文导读的感觉啊”，一篇论文的正确读法：
* 动机
* 模型
* 实验
* 评价（读者的）

而不是翻译一篇论文，看别人的翻译不如自己看原文
>取代MF的一个基础模型
>
这篇不是注意力模型的，分错了。
#### 4-Next Item Recommendation with Self-Attention
[论文导读](https://zhuanlan.zhihu.com/p/48069398)
> **本文提出了一种基于 self-attention 的基于序列的推荐算法**，利用**self-attention**来为用户短期行为模式的依赖关系和重要性建模。同时该模型也保留了用户的长久兴趣。整个网络在 **metric learning** 的框架下，是**第一次将 self-attention 和 metric learning的结合的尝试。**
#### 5-**Attention-based Transactional Context Embedding for Next-Item Recommendation**
[paper](http://203.170.84.89/~idawis33/DataScienceLab/publication/AAAI18-Wang.pdf)
[论文导读](https://blog.csdn.net/Zhongsigen/article/details/81704545)
>作者提出一个推荐算法，这个算法不仅考虑当前交易中所有的observed items，而且还要用不同的relevance(相关性)对它们进行加权，以建立一个attentive context(注意力上下文)，以高概率输出正确的下一个项目。模型——基于注意的事务嵌入模型（ATEM），用于上下文嵌入，以在不假定顺序的情况下对每个观察到的项目进行加权。


这篇导读对模型的介绍几乎没有，需要补全
$$Attention(Q,K,V)=Attention(Q, Q, Q)$$

### 6-self-attention 
[介绍博客-self attention in NLP](http://www.cnblogs.com/robert-dlut/p/8638283.html)

#### 7-Attentive collaborative filtering
Multimedia recommendation with item-and component-level attention
[论文导读](https://zhuanlan.zhihu.com/p/32787606)
利用多媒体内容特征学习component-level attention网络， 然后再利用该网络的结果学习item-level attention网络，其实就是嵌套了两层网络。

#### 8- A^3NCF: An Adaptive Aspect Attention Model for Rating Prediction
paper weekly 推荐的一篇论文
https://www.paperweekly.site/papers/2560 
[代码](https://github.com/hustlingchen/A3NCF)
>本文是新加坡国立大学发表于IJCAI 2018的工作，论文**基于评论文本**对用户偏好和商品特征进行抽取，提出了一种自适应注意力模型用于用户评论的智能排序，不断学习用户对商品在不同关注点方面的权重，进而提升推荐效果。本文解决了已有方法忽视不同用户对商品不同侧面关注点不同的缺陷，并且在Amazon Product Review和Yelp 2017这两个大规模推荐系统数据库上取得了领域内最好效果。

[](https://www.jianshu.com/p/46d36caa9688)
#### 9-Attention-based Group Recommendation
paper weekly 推荐的一篇论文
https://www.paperweekly.site/papers/2561
>本文来自南洋理工大学。作为个体的用户和群组成员的行为是不同的，作者基于用户评级历史的深度学习技术，提出了一个注意力群体推荐模型来解决群体推荐问题，模型自动学习群组中的每个用户的影响权重并根据其成员的权重偏好为群组推荐项目。虽然基于图和概率的模型已经得到了广泛的研究，但本文是第一个将Attention机制应用到群体推荐中的。

#### 10-Attentional Factorization Machines: Learning the Weight of Feature Interactions via Attention Networks
[paper & code](https://github.com/hexiangnan/attentional_factorization_machine/tree/master/code)
在原有的fm模型上添加注意力模型，其实就是在fm的二次交叉项上乘一个注意力因子权重，注意力因子采用mlp模型，输入就是fm的二次交叉项，输出放入softmax函数得到我们想要的注意力因子。

数据集：movielens latest larger  - rmse ：0.43~0.44

## 实时推荐系统
#### 1-StreamRec: a real-time recommender system ACM2011
#### 2-Streaming recommender systems
[paper](https://dl.acm.org/citation.cfm?id=3052627)
#### 3- RecSys'15 Tutorial on "Real-Time Recommendation of Streamed Data"
tutorial 不是论文
[地址](https://www.slideshare.net/fraho/recsys15-tutorial-on-realtime-recommendation-of-streamed-data)

## 交叉推荐
#### 1-Man, Tong et al. Cross-domain recommendation: an embedding and mapping approach. IJCAI, 2017.
[导读](https://zhuanlan.zhihu.com/p/30621349)

## 时序漂移
#### 1-Collaborative filtering with temporal dynamics
#### 2- taste over time: the temporal dynamics of user preferences
[paper](http://www.cs.cornell.edu/~jlmo/ismir13.pdf)

提出了一个动态嵌入概率模型，将用户和歌曲都嵌入一个d维欧几里得空间，通过空间距离来为时间动态建模。但是实验部分只是可视化了用户和歌曲在嵌入空间的动态变化，而且为了能够可视化实现，只进行了2维嵌入，但是在时间的动态建模上可以有所借鉴。但是不知道最后的准确率效果如何。具体建模就是 采用最大似然概率来最大化转移概率
#### 3-Recurrent Poisson Factorization for Temporal Recommendation
[paper](https://arxiv.org/pdf/1703.01442.pdf)
poisson矩阵分解概率模型
#### 4- Next-song recommendation with temporal dynamics
[paper](https://www.sciencedirect.com/science/article/abs/pii/S0950705115003032)
和上一篇一样都是概率模型， 使用马尔科夫链表示嵌入
#### 5-modeling temporal dynamics of user preferences in movie recommendation 2018IEEE
推荐任务： 推荐电影类型==
通过耦合张量分解框架来建模用户偏好中的时序动态，同时采用了用户的人口统计学信息来辅助推荐。

数据处理：将movielens -1m横跨36个月的数据分成了6个时间段，结合用户的人口统计学信息设计了24个属性特诊。
#### 6-# Time and Local Popularity in top-N Recommendation
[paper](https://arxiv.org/abs/1807.04204)
#### 7- TCARS
利用时间信息计算相似用户，假设在同一时间段内，评分相似的用户有着更xiang
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyMTI5NzQ0NzcsNTM4MDA1MjgsLTkxMz
A2ODk0NiwtNzA3NTkyMzUxLDEwMjI3NDQxMzUsMTEzMjYxMzM1
MCwtMTQzNjA3Mjc2Miw3NjExMjMzMjEsMTc0MDIxNzQxOSwtMT
E3NjA5OTYzNSwtMTk5MjI4MzQ4MiwyMjA2Njk0NTUsMTA0MDY0
ODY0NCwtMTUzMjE3MTU5OCwxNzcyMjA4MDEwLDgzNDkwMDkwOS
w5ODkxNTYzNDcsLTY1NDkxMzcyNiwtMTg2MzA5NTMwNywtMTMx
Njk2ODk1MF19
-->