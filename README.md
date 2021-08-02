---
title: モンテカルロ法で日本経済シミュレーション
tags: モンテカルロ法,シミュレーション,数値シミュレーション,jpes
---

# モンテカルロ法で日本経済をシミュレーションしたい！【JPES 第1回】

[![hackmd-github-sync-badge](https://hackmd.io/idG386JaToyCCoTAQwUVNQ/badge)](https://hackmd.io/idG386JaToyCCoTAQwUVNQ)


## モデル
### 公共投資 $G$
政府が企業に対して投じるお金. 公共サービスの対価.

### 投資 $I$
銀行などの経済主体が企業に対して投じるお金. 返済が必要.

### 所得税 $\tau$
自然人の所得に対して課される税金.

### 消費率 $u$
自然人の可処分所得に対して消費されるお金の割合.

### 返済 $R$
何らかの債務に対して返済されるお金.

### 所得 $g$
自然人の総所得金額.

### 租税 $T = g\tau$
政府が課した租税収入の総額.

### 消費 $C = gu(1-\tau)$
自然人の消費した財の総額.

### 貯蓄 $S$
自然人の行った貯蓄の総額.

### 稼働率 $r$
生産力に対して実際に生産された財の量の割合.

### 生産量 $w(I) = \alpha I$
投資に対して生産可能な財の最大量. $\alpha$は任意の定数.

### 需要 $d(p) = \frac{\gamma}{p}$
価格$p$のときに発生する財の需要の総量.

### 求解してみる

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

$\theta > \frac{\gamma\beta^2}{I^2}$ なので, $\theta = s\frac{\gamma\beta^2}{I^2}$ と置く.

均衡価格 $p = \sqrt{\frac{\gamma}{\theta}} = \sqrt{\frac{\gamma}{s\frac{\gamma\beta^2}{I^2}}} = \frac{I}{\sqrt{s}\beta}$

$\theta_D = \frac{\gamma\beta^2}{I^2}$のときの$p = \frac{I}{\beta}$を ___投資均衡価格___ と呼ぶことにする.

需要 $d = \frac{\gamma}{p} = \frac{\sqrt{s}\beta\gamma}{I} = \frac{\sqrt{s}\beta C}{I} = wr$
消費 $C = dp = \gamma = wrp = (\alpha I)r\frac{I}{\beta} = \frac{\alpha r}{\beta} I^2$

$\frac{\sqrt{s}\beta C}{I} = \alpha Ir$なので, つまり,

$$
\begin{aligned}
     \sqrt{s} &= \frac{\alpha I^2}{\beta C}r \\
     &= \frac{\frac{\alpha}{\beta}r(\frac{\beta}{\beta-1})^2((1 - u + u\tau)g - G)^2}{(1 - \tau)ug} \\
     &= \frac{\alpha\beta rg(1-u+u\tau - \frac{G}{g})^2}{(\beta-1)^2(1-\tau)u}
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