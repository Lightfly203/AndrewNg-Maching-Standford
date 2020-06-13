> 作为英语课程，读中文参考资料的确有助于理解，但是出于对以后更长久的学习优势考虑，笔记中我会尽量采用英文来表述，这样有助于熟悉专有名词以及常见语法结构，对于无中文翻译的资料阅读大有裨益。

#  Week2  多变量线性回归Linear Regression with Multiple Variables
## 一、Multiple Variables Linear Regression Algorithm

1. Multiple Feature多维特征

   - 模型中的特征为（x~1~,x~2~,x~3~.....x~n~ ）
   - n代表特征数量
   - x^i^是第i个训练实例，特征矩阵中的第i行，是一个向量Vector

2. Multiple Variables Linear Regression Algorithm

   - $h_\theta(x)=\theta^TX=\theta_0+\theta_1x_1...+\theta_nx_n$
     - n+1维
   - $J(\theta_0,...\theta_n)=\frac{1}{2m}\sum_{i=1}^{m}(h_\theta(x^i)-y^i)^2$


   - $\theta_j:=\theta_j-\alpha\frac{1}{m}\sum_{i=1}^{m}((h_\theta(x^i)-y^i)x^j)$


## 二、梯度下降法实践

1. $x_n=\frac{x_n-\mu_n}{s_n}$
   1. $\mu_n$为平均值
   2. $s_n$为标准差

##  三、Polynomial Regresssion多项式回归

1. 多项式回归模型运行梯度下降算法前，必须进行特征缩放

## 四、正规方法法

1. 求导
2.  $\theta=(X^TX)^{-1}X^Ty$

##  五、Octave教程

1. 建议用什么上网搜索什么，直接搜索matlab相应语法；Octave体量小容易启动，但是终究是要使用Matlab或者转入python的，不如就用Matlab语法；

2. size：向量维度或者矩阵维度

3. who：当前工作空间的所有变量，详细信息whos

4. 点运算针对元素，否则针对整个矩阵

5. A'转置

6. imagesc（A）可视化矩阵，colorbar颜色调，colormap gray灰度图

7. 循环 

   - `for i=1:10 `
   - `end`

8. exit/quit

9. 函数定义(```)

   ```function y = name(x) 
   function y = name(x) 
   y=x^2 
   ```

   可以定义多个返回变量（很特别，大多数编程语言一个函数只能返回一个值）

## 六、向量化思维

1. 使用向量而非循环来计算