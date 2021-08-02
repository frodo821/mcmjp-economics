---
title: モンテカルロ法で日本経済シミュレーション
tags: モンテカルロ法,シミュレーション
---

# モンテカルロ法で日本経済をシミュレーションしたい！

## モデル
投資 $I$
稼働率 $r$
生産量 $w(I) = \alpha I$
需要 $d = \frac{\gamma}{p}$
消費税 $\tau$
消費率 $u$

上記の条件の下で, 
$$
wr = {\rm min}(\theta p, w) \\
\frac{\gamma}{p} = \theta p \\
\theta\gamma = p^2 \\
p = \sqrt{\frac{\gamma}{\theta}} \\
$$

また,

$$
\begin{aligned}
    G + I + C &= R + g \\
    &= T + S + C \\
    &= \tau g + S + C \\
    &= \tau g + S + (1-\tau)ug
\end{aligned}
$$

可処分所得 $(1 - \tau)g$

$$
\begin{aligned}
    \frac{I}{\beta} &< \sqrt{\frac{\gamma}{\theta}} \\
    \theta &< \frac{\gamma\beta^2}{I^2}
\end{aligned}
$$

$\theta < \frac{\gamma\beta^2}{I^2}$ なので, $\theta = s\frac{\gamma\beta^2}{I^2}$ と置く.

均衡価格 $p = \sqrt{\frac{\gamma}{\theta}} = \sqrt{\frac{\gamma}{s\frac{\gamma\beta^2}{I^2}}} = \frac{I}{\sqrt{s}\beta}$

$\theta_D = \frac{\gamma\beta^2}{I^2}$のときの$p = \frac{I}{\beta}$を ___投資均衡価格___ と呼ぶことにする.

需要 $d = \frac{\gamma}{p} = \frac{\sqrt{s}\beta\gamma}{I} = \frac{\sqrt{s}\beta C}{I} = wr$
消費 $C = dp = \gamma = wrp = (\alpha I)r\frac{I}{\beta} = \frac{\alpha r}{\beta} I^2$

$\frac{\sqrt{s}\beta C}{I} = \alpha Ir$なので, つまり,

$$
\begin{aligned}
     \sqrt{s} &= \frac{\alpha I^2}{\beta C}r \\
     &= \frac{\frac{\alpha}{\beta}r(\frac{\beta}{\beta-1})^2((1 - u + u\tau)g - G)^2}{(1 - \tau)ug} \\
     &= \frac{\alpha\beta rg(1-u+u\tau - \frac{G}{g})}{(\beta-1)^2(1-\tau)u}
\end{aligned}
$$

$$
\begin{aligned}
C &= wrp\\
&= (\theta p)p\\
&= \theta p^2\\
&= s\frac{\gamma\beta^2}{I^2}p^2\\
&= (1 - \tau)ug\\
\end{aligned}
$$