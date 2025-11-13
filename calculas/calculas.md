---
title: 微积分速成教程
author: 你的名字
date: 2025
---

# 《微积分速成教程》

> **从零基础到会求导、会积分，200+ 例题，附答案与 GeoGebra 动态图**

---

## 本书适合谁？

- 高中生预习大学数学
- 大学生补基础
- 考研数学一/三冲刺
- 程序员自学数值计算

## 你将学会

1. 极限的 $\varepsilon-\delta$ 定义
2. 导数的几何意义与链式法则
3. 定积分的黎曼和与牛顿-莱布尼茨公式
4. 泰勒展开与误差估计

---

## 使用说明

- 每节 = **概念 → 定理 → 证明 → 例题 → 练习**
- 公式用 $$ 包裹，支持放大
- 扫描二维码看 **B站视频讲解**
- 答案在书末 PDF

---

![cover](images/cover.jpg)

*图 0.1：微积分核心思想——无限逼近*  
  
  
# 第1章 极限与连续

## 1.1 极限的 $\varepsilon-\delta$ 定义

**定义 1.1**（极限）  
设函数 $f(x)$ 在 $x_0$ 的某去心邻域内有定义。若 $\forall \varepsilon > 0$，$\exists \delta > 0$，使得当

$$ 0 < |x - x_0| < \delta $$

时，有

$$ |f(x) - L| < \varepsilon $$

则称

$$ \lim_{x \to x_0} f(x) = L \tag{1.1} $$

---

### 例题 1.1

证明：$\lim_{x \to 2} (3x - 1) = 5$

**解：**  
令 $\varepsilon > 0$，取 $\delta = \varepsilon / 3$。  
当 $0 < |x - 2| < \delta$ 时，

$$
\begin{align}
|(3x - 1) - 5| &= |3x - 6| \\
                 &= 3|x - 2| < 3 \cdot \frac{\varepsilon}{3} = \varepsilon
\end{align}
$$

$\therefore$ 极限为 5. $\square$

---

![limit_graph](images/limit_graph.png)

*图 1.1：函数 $f(x) = 3x - 1$ 在 $x=2$ 附近逼近 5*

---

### 练习 1.1

1. 证明：$\lim_{x \to 1} x^2 = 1$
2. 计算：$\lim_{x \to 0} \frac{\sin x}{x} = ?$

> 答案见书末  


# 第2章 导数

## 2.1 导数的定义

**定义 2.1**  
函数 $f(x)$ 在 $x_0$ 处可导，若极限

$$ f'(x_0) = \lim_{h \to 0} \frac{f(x_0 + h) - f(x_0)}{h} \tag{2.1} $$

存在，则称 $f'(x_0)$ 为 $f$ 在 $x_0$ 处的**导数**。

---

### 几何意义

导数 = 切线斜率

![derivative](images/derivative_graph.png)

*图 2.1：$f(x) = x^2$ 在 $x=1$ 处的切线斜率为 2*

---

### 常用导数表

| $f(x)$            | $f'(x)$           |
|-------------------|-------------------|
| $c$               | $0$               |
| $x^n$             | $n x^{n-1}$       |
| $\sin x$          | $\cos x$          |
| $e^x$             | $e^x$             |
| $\ln x$           | $1/x$             |

---

### 链式法则

若 $y = f(g(x))$，则

$$ \frac{dy}{dx} = f'(g(x)) \cdot g'(x) $$

例：$y = \sin(x^2)$ → $y' = \cos(x^2) \cdot 2x$  


# 第3章 积分

## 3.1 定积分的定义（黎曼和）

将 $[a,b]$ 分成 $n$ 等份，$\Delta x = \frac{b-a}{n}$，取右端点：

$$ \int_a^b f(x) dx = \lim_{n \to \infty} \sum_{i=1}^n f(a + i \Delta x) \Delta x \tag{3.1} $$

---

### 牛顿-莱布尼茨公式

若 $F'(x) = f(x)$，则

$$ \int_a^b f(x) dx = F(b) - F(a) $$

---

### 例题 3.1

计算：$\int_0^1 x^2 dx$

**解：**  
原函数 $F(x) = \frac{1}{3} x^3$

$$
\int_0^1 x^2 dx = \left[ \frac{1}{3} x^3 \right]_0^1 = \frac{1}{3} - 0 = \frac{1}{3}
$$

---

### 换元积分法

令 $u = \sin x$，$du = \cos x dx$

$$ \int \cos x \sin x dx = \int u du = \frac{1}{2} u^2 + C = \frac{1}{2} \sin^2 x + C $$