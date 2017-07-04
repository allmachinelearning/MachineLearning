# 距离度量

- - -

[toc]

## 常见距离与相似度度量

- - -

### 欧氏距离

定义在两个向量（两个点）上：点$\mathbf{x}$和点$\mathbf{y}$的欧氏距离为：

$$
d_{Euclidean}=\sqrt{(\mathbf{x}-\mathbf{y})^\top (\mathbf{x}-\mathbf{y})}
$$

### 闵可夫斯基距离

Minkowski distance， 两个向量（点）的$p$阶距离：

$$
d_{Minkowski}=(|\mathbf{x}-\mathbf{y}|^p)^{1/p}
$$

当$p=1$时就是曼哈顿距离，当$p=2$时就是欧氏距离。

### 马氏距离

定义在两个向量（两个点）上，这两个点在同一个分布里。点$\mathbf{x}$和点$\mathbf{y}$的马氏距离为：

$$
d_{Mahalanobis}=\sqrt{(\mathbf{x}-\mathbf{y})^\top \Sigma^{-1} (\mathbf{x}-\mathbf{y})}
$$

其中，$\Sigma$是这个分布的协方差。

当$\Sigma=\mathbf{I}$时，马氏距离退化为欧氏距离。

### 互信息

定义在两个概率分布$X,Y$上，$x \in X,y \in Y$.它们的互信息为：

$$
I(X;Y)=\sum_{x \in X} \sum_{y \in Y} p(x,y) \log \frac{p(x,y)}{p(x)p(y)}
$$

### 余弦相似度

衡量两个向量的相关性（夹角的余弦）。向量$\mathbf{x},\mathbf{y}$的余弦相似度为：

$$
\cos (\mathbf{x},\mathbf{y}) = \frac{\mathbf{x} \cdot \mathbf{y}}{|\mathbf{x}|\cdot |\mathbf{y}|}
$$

理解：向量的内积除以向量的数量积。

### 皮尔逊相关系数

衡量两个随机变量的相关性。随机变量$X,Y$的Pearson相关系数为：

$$
\rho_{X,Y}=\frac{Cov(X,Y)}{\sigma_X \sigma_Y}
$$

理解：协方差矩阵除以标准差之积。

范围：[-1,1]，绝对值越大表示（正/负）相关性越大。

### Jaccard相关系数

对两个集合$X,Y$，判断他们的相关性，借用集合的手段：

$$
J=\frac{X \cap Y}{X \cup Y}
$$

理解：两个集合的交集除以并集。

扩展：Jaccard距离=$1-J$。

- - -

## 概率分布的距离度量

- - -

### KL散度

Kullback–Leibler divergence，相对熵，衡量两个概率分布$P(x),Q(x)$的距离：

$$
D_{KL}(P||Q)=\sum_{i=1} P(x) \log \frac{P(x)}{Q(x)}
$$

非对称距离：$D_{KL}(P||Q) \ne D_{KL}(Q||P)$.

### JS距离

Jensen–Shannon divergence，基于KL散度发展而来，是对称度量：

$$
JSD(P||Q)= \frac{1}{2} D_{KL}(P||M) + \frac{1}{2} D_{KL}(Q||M)
$$

其中$M=\frac{1}{2}(P+Q)$。是对称度量。

### MMD距离

Maximum mean discrepancy，度量在再生希尔伯特空间中两个分布的距离，是一种核学习方法。两个随机变量的距离为：

$$
MMD(X,Y)=\left \Vert \sum_{i=1}^{n_1}\phi(\mathbf{x}_i)- \sum_{j=1}^{n_2}\phi(\mathbf{y}_j) \right \Vert^2_\mathcal{H}
$$

其中$\phi(\cdot)$是映射，用于把原变量映射到高维空间中。

理解：就是求两堆数据在高维空间中的均值的距离。

### Principal angle

也是将两个分布映射到高维空间（格拉斯曼流形）中，在流形中两堆数据就可以看成两个点。Principal angle是求这两堆数据的对应维度的夹角之和。对于两个矩阵$\mathbf{X},\mathbf{Y}$，计算方法：首先正交化两个矩阵，然后：

$$
PA(\mathbf{X},\mathbf{Y})=\sum_{i=1}^{\min(m,n)} \sin \theta_i
$$

其中$m,n$分别是两个矩阵的维度，$\theta_i$是两个矩阵第$i$个维度的夹角，$\Theta=\{\theta_1,\theta_2,\cdots,\theta_t\}$是两个矩阵SVD后的角度：

$$
\mathbf{X}^\top\mathbf{Y}=\mathbf{U} (\cos \Theta) \mathbf{V}^\top
$$

### HSIC

希尔伯特-施密特独立性系数，Hilbert-Schmidt Independence Criterion，用来检验两组数据的独立性：

$$
HSIC(X,Y) = trace(HXHY)
$$

其中$X,Y$是两堆数据的kernel形式。

### Earth Mover’s Distance

推土机距离，度量两个分布之间的距离，又叫Wasserstein distance。以最优运输的观点来看，就是分布$X$能够变换成分布$Y$所需要的最小代价：

一个二分图上的流问题，最小代价就是最小流，用匈牙利算法可以解决。

$$
emd(X,Y)=\min{\frac{\sum_{i,j}f_{ij}d(\textbf{x}_i,\textbf{y}_j)}{\sum_{j}w_{yj}}}
$$

约束条件为

$$
s.t. \sum_{i}f_{ij}=w_{yj}, \sum_{j}f_{ij}=w_{xi}.
$$

#### References

[1] http://blog.csdn.net/pipisorry/article/details/45651315

[2] http://chaofan.io/archives/earth-movers-distance-%E6%8E%A8%E5%9C%9F%E6%9C%BA%E8%B7%9D%E7%A6%BB


