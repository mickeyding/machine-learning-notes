# 机器学习（二）概率密度估计

**2018/2/13**

**by ChenjingDing**

---

高斯分布预备知识总结（可以先跳过，必要时查找）

#### 1.一维高斯分布公式

$$N(x|μ，σ^2) = \frac{1}{\sqrt{2π}*σ} exp{- \frac{(x-μ)^2}{2σ^2}}$$ ；

#### 2.多维高斯分布公式

$$N(x|μ，Σ)=\frac{1}{(2π)^{D/2}|Σ|^{1/2}}exp \{-\frac{1}{2}(x-μ)^T Σ^{-1}(x-μ) \}$$ ；

#### 3.多维高斯分布数据的相关性

由于Σ是实对称矩阵，可以将Σ分解成特征向量和的形式：

$$Σ = \sum_{i=1}^D λ_i μ_i μ_i^T$$；矩阵的逆：$$Σ^{-1} = \sum_{i=1}^D \frac{1}{λ_i} μ_i μ_i^T$$

以2维高斯分布为例：

$$μ =[ \ \begin{array}{c}
μ_1\\
μ_2\\
\end{array} \ ]$$；$$μ =[ \ \begin{array}{cc}
σ_1^2 & \rho \\
\rho & σ_2^2\\
\end{array} \ ]$$ ；

其中，$$\rho$$表示了数据间的相关性，数值越大，相关性越高，下图中，随着$$\rho$$的增大，高斯模型在xy平面上的投影越尖。$$\rho > 0 $$ ，为正相关；$$\rho < 0 $$ ，为负相关。![](/assets/2.0多维高斯模型协方差矩阵表示相关性.png)$$图2 二维高斯模型在xy平面上投影(左：\rho=0；中：\rho=0.4；右：\rho=0.8)$$

> https://www.youtube.com/watch?v=YRS-IB3vCow 了解更多多维高斯分布的性质

---



一.非参数估计

1.1高斯分布

1.2最大似然估计

二.参数估计

2.1直方图估计

2.2核方法

2.3K近邻估计

三.高斯混合模型

四.判别模型和生成模型

4.1什么是判别模型以及在机器学习中的应用

4.2什么是生成模型以及在机器学习中的应用

4.3两者的优缺点比较

高斯混合模型的判别依据是什么？

discriminative models infer outputs based on inputs, while generative models generate both inputs and outputs, typically given some hidden parameters.

