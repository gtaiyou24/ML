# クラスタリング(clustering)
データをいくつかのクラスタにグループ分けをする**クラスタリング**についてまとめる。

データ$D = \left\{d^{1}, d^{2}, \cdots, d^{n}\right\}$が与えられ、$D$内の各要素はそれぞれベクトル$d^{1} = \left(x_{1}, x_{2}, \dots, x_{n}\right)$で表現されているとする。


# クラスタ間の類似度

## 距離関数
クラスタ間の類似度を測るために二つのベクトル$x_{i}$と$x_{j}$の間の距離を定義する必要がある。

 - $d$: 各ベクトルの次元数
 - $x_{i} = {\left({x}_{i1}, \dots ,{x}_{id}\right)}^{T}$

### ユークリッド距離
$$
d\left(x_{i}, x_{j}\right) = {\left[\sum _{k=1}^{d}{{\left({x}_{ik} - {x}_{jk}\right)}^{2}} \right]}^{1/2}
$$

## 類似度関数
### 方向余弦(コサイン類似度)
ベクトル間の角度($\cos {\theta}$)を用いた尺度であり、よく利用される。
$$
d\left(x_{i}, _{j}\right) = \frac { \sum _{k=1}^{d}{{x}_{ik}{x}_{jk}} }{  \sqrt {\left(\sum _{k=1}^{d}{{{x}_{ik}}^{2}}\right)\left(\sum _{k=1}^{d}{{{x}_{jk}}^{2}}\right)} }
$$