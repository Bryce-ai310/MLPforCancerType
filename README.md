# MLPforCancerType
Multi Layer Perceptron for cancer type

#### 数据预处理 ####
1. y label数据集中每个类别（也就是 cancer type）少于20样本量的类别删除；
2. 然后在chunk循环中将X中存在于y label数据集中的样本保留下来；
3. 然后删除NA的行；
4. 去除重复样本；
5. 再计算方差；
6. 保留方差大于10的行；
7. 最后转置；
8. 得到X_final后（PCA可选）；
9. 再保留y label中在X中出现的样本名。

##### 思路：
特征筛选：方差 + L1正则化 + dropout（这里选用这个方法）
特征提取：PCA + dropout (其中PCA非常吃内存)
这里没用PCA因为内存太小，并且为了可解释性高
