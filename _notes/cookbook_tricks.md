---
layout: default
title: Cookbook Tricks
tags:
  - mathematics
  - inequalities
  - analysis
---

## Inequalities and Identities

1. **Difference of squares** 
   
   $$\lVert a \rVert^2 - \lVert b \rVert^2 = \langle a-b, a+b \rangle$$

2. **Transcendental inequality** 
   
    $$\log_2(x) < x - 1$$

3. **Cauchy-Schwarz (for any inner product)**
   
   $$\lvert \langle a, b \rangle \rvert \leq \lVert a \rVert \cdot \lVert b \rVert$$

4. Convexity for $\alpha \in [0, h]$

5. **Young inequality (general)**
   
   $$ab \leq \frac{a^p}{p} + \frac{b^q}{q} \qquad \forall a,b\in\mathbb{R},$$
   
   $$\frac{1}{p} + \frac{1}{q} = 1 \qquad \forall p,q > 1$$

6. **Young inequality (frequent instance)**
   
   $$ab \leq \frac{1}{2}a^2 + \frac{1}{2}b^2 \qquad \forall a,b\in\mathbb{R}$$

7. **AM-GM inequality**

   For nonnegative reals $a_1, \dots, a_n$, an we have

   $$\frac{a_1 + \dots + a_n}{n} \geq \sqrt[n]{a_1\cdot\dots a_n}$$

   Equality only if $a_1 = \dots = a_n$.

   <div class="accordion" markdown="1">
   <details markdown="1">
   <summary>Proof</summary>

    https://en.wikipedia.org/wiki/AM–GM_inequality#Proofs_of_the_AM–GM_inequality
    
   </details>
   </div> 

8. **Weighted AM-GM inequality**

   Let $x_1,\dots,x_m>0$ and weights $\lambda_1,\dots,\lambda_m\ge 0$ satisfy $\sum_{j=1}^m \lambda_j=1$. Then

   $$\prod_{j=1}^m x_j^{\lambda_j}\le \sum_{j=1}^m \lambda_jx_j.$$

   <div class="accordion" markdown="1">
   <details markdown="1">
   <summary>Proof</summary>

    If some $\lambda_j=0$, that variable is irrelevant, so we may assume $\lambda_j>0$.

    **Key idea.** The logarithm turns products into sums, and $\log$ is concave.

    Since

    $$(\log x)^{''}=-\frac1{x^2}<0,$$

    Jensen's inequality for the concave function $\log$ gives

    $$\log\left(\sum_{j=1}^m\lambda_jx_j\right) \ge \sum_{j=1}^m\lambda_j\log x_j.$$

    But

    $$\sum_{j=1}^m\lambda_j\log x_j = \log\left(\prod_{j=1}^m x_j^{\lambda_j}\right).$$

    Therefore

    $$\log\left(\sum_j\lambda_jx_j\right) \ge \log\left(\prod_jx_j^{\lambda_j}\right).$$

    Since $\log$ is increasing,

    $$\boxed{\sum_{j=1}^m\lambda_jx_j\ge\prod_{j=1}^m x_j^{\lambda_j}.}$$

    **Equality.** Because $\log$ is strictly concave, equality in Jensen occurs, for positive weights, iff

    $$x_1=x_2=\cdots=x_m.$$

    So weighted AM–GM is really just the statement that

    $$\log(\text{weighted arithmetic mean})\ge\text{weighted mean of the logs}.$$

    Equivalently, the logarithm of the arithmetic mean dominates the logarithm of the geometric mean.

   </details>
   </div> 

9. **Generalized Hölder’s Inequality**
   
   * Let $\lambda_a, \lambda_b, \dots, \lambda_z$ be positive reals
     * $\lambda_a + \lambda_b + \dots + \lambda_z = 1$. 
   * Let $a_1, a_2, \dots, a_n$ be positive reals.
   * Let $b_1, b_2, \dots, b_n$, be positive reals.
   * $\dots$ 
   * Let $z_1, z_2, \dots, z_n$ be positive reals.
  
   $$(a_1 + \dots + a_n)^{\lambda_a} (b_1 + \dots + b_n)^{\lambda_b} \dots (z_1 + \dots + z_n)^{\lambda_z} \geq \sum_{i=1}^n a_i^{\lambda_a} b_i^{\lambda_b} \dots z_i^{\lambda_z}$$
   
   <div class="accordion" markdown="1">
   <details markdown="1">
   <summary>Proof</summary>

    1. **WLOG.** $a_1 + \dots + a_n = b_1 + \dots + b_n = \dots = z_1 + \dots + z_n = 1$
    2. **Why WLOG.** the normalizing constant $(1/N_x)^\lambda_x$ will cancel out on both sides.
    3. Then
    
       $$
       \begin{aligned}
       (a_1 + \dots + a_n)^{\lambda_a} (b_1 + \dots + b_n)^{\lambda_b} \dots (z_1 + \dots + z_n)^{\lambda_z} = 1 
       &= \sum_i^n \lambda_a a_i + \lambda_b b_i + \dots + \lambda_z z_i \\
       &= \prod_i^n a_i^{\lambda_a} b_i^{\lambda_b} \dots z_i^{\lambda_z} \qquad (\text{weighted AM-GM inequality}),
       \end{aligned}
       $$

    4. By weighted AM-GM inequality we used
       
       $$\lambda_a a_i + \lambda_b b_i + \dots + \lambda_z z_i \geq a_i^{\lambda_a} b_i^{\lambda_b} \dots z_i^{\lambda_z}$$

   </details>
   </div> 

10. **From Minkowski to Holder path**

    $$|a+b|^p = |a+b|\cdot |a+b|^{p-1} \leq (|a|+|b|)\cdot |a+b|^{p-1} = |a|\cdot|a+b|^{p-1} + |b|\cdot|a+b|^{p-1},$$

    where we used $\lvert a+b\rvert \leq \lvert a\rvert + \lvert b\rvert$.

11. Gronwall inequality
12. Bessel inequality
13. Minkowski's Inequality
14. Minkowski's Integral Inequality
15. Fenchel Inequality
16. Cauchy-Schwarz inequality for $L^2$ complex-valued functions

17. **The Matrix Exponential**
    
    $$e^A = \sum_{k=0}^{\infty} \frac{A^k}{k!}$$

18. **The Scalar Exponential**

    $$e^x = \sum_{k=0}^{\infty} \frac{x^k}{k!}$$

19. **Log and sqrt:**
    
    $$\sqrt{x} - 1 \geq \frac{\log x}{2} \qquad \forall x\geq 0$$

20. **$l1 < \sqrt n l2$**
    
    $$n\sum_{i=1}^n a_i^2 \;-\; \Big(\sum_{i=1}^n a_i\Big)^2 \;=\; \sum_{1\le i<j\le n} (a_i - a_j)^2$$

21. For $p,q\geq 0$
    
    $$\lvert p - q \rvert = \lvert \sqrt{p} - \sqrt{q} \rvert (\sqrt{p} + \sqrt{q})$$

    * derived from $a^2-b^2 = (a-b)(a+b)$

22. **Some algebraic inequality:**

    $$1−(1−t)^k \leq \min(1,kt) \text{for } t\in[0,1]$$

    <figure>
      <img src="{{ '/assets/images/notes/random/roof_of_the_curve_ineq.png' | relative_url }}" alt="Left: vectors e1=(1,0), e2=(1,1) and their dual basis covectors ě1=(1,-1), ě2=(0,1) plotted in R² with level sets of the covectors as faded diagonal and horizontal lines. Right: the canonical basis is its own dual under the canonical Euclidean inner product." loading="lazy">
      <!-- <figcaption>Left (b): the dual basis $\check e^1 = (1, -1)$, $\check e^2 = (0, 1)$ for the oblique basis $e_1, e_2$. Faded red lines are level sets of $\check e^1$ (diagonals along direction $e_2$); faded orange lines are level sets of $\check e^2$ (horizontals along $e_1$). Each covector $\check e^i$ kills $e_j$ for $j \ne i$. Right (c): the canonical basis under the canonical inner product is self-dual.</figcaption> -->
    </figure>
    
23. **Apollonius's Theorem**
    
    $$\text{Side}_1^2 + \text{Side}_2^2 = 2 \cdot (\text{Median})^2 + 2 \cdot \left(\frac{\text{Base}}{2}\right)^2$$

24. **Corollary of Appollonius's Theorem (useful for Gaussian kernels decomposition)**

    $$\lVert t-x \rVert^2 + \lVert t-y \rVert^2 = 2 \left\lVert t - \frac{x+y}{2} \right\rVert^2 + 2 \left( \frac{\lVert x-y \rVert}{2} \right)^2$$

25. **Euler–Poisson integral**

    $$\int_{\infty}^{\infty} e^{-ax^2} = \sqrt{\frac{\pi}{a}}$$

<div class="accordion" markdown="1">
<details markdown="1">
<summary>Proof</summary>

This is one of the most famous—and cleverest—tricks in all of calculus. You cannot compute the antiderivative of $e^{-ax^2}$ using standard elementary functions, so trying to solve the 1D integral directly is a dead end.

Instead, the trick is to **square the integral** and push it into two dimensions, where the geometry of the plane makes it trivial to solve.

Here is the step-by-step mathematical derivation.

**Step 1: Square the Integral**

Let the integral we want to solve be $I$:

$$I = \int_{-\infty}^\infty e^{-ax^2} dx$$

Since $e^{-ax^2}$ is strictly positive, we know that $I > 0$. Let's square $I$. To keep the variables distinct, we will use $x$ for the first integral and $y$ for the second:

$$I^2 = \left( \int_{-\infty}^\infty e^{-ax^2} dx \right) \left( \int_{-\infty}^\infty e^{-ay^2} dy \right)$$

**Step 2: Combine into a Double Integral**

Because the integrals are independent, we can combine them into a single double integral over the entire 2D Cartesian plane ($\mathbb{R}^2$):

$$I^2 = \int_{-\infty}^\infty \int_{-\infty}^\infty e^{-ax^2} e^{-ay^2} dx dy$$

Using the property of exponents ($e^A e^B = e^{A+B}$), this becomes:

$$I^2 = \int_{-\infty}^\infty \int_{-\infty}^\infty e^{-a(x^2 + y^2)} dx dy$$

**Step 3: Switch to Polar Coordinates**

This is where the magic happens. The term $(x^2 + y^2)$ perfectly maps to the squared radius in polar coordinates.
We make the standard substitution:

* $r^2 = x^2 + y^2$
* The area element $dx dy$ becomes $r dr d\theta$

We also need to change the bounds. Integrating over the entire Cartesian plane ($x$ and $y$ from $-\infty$ to $\infty$) is exactly the same as integrating the radius from $0$ to $\infty$, and the angle from $0$ to $2\pi$:

$$I^2 = \int_0^{2\pi} \int_0^\infty e^{-ar^2} r dr d\theta$$

**Step 4: Evaluate the Integral**

The problem is now trivial because that extra $r$ from the polar area element allows us to use simple u-substitution.

Let's evaluate the inner integral with respect to $r$:

$$\int_0^\infty e^{-ar^2} r dr$$

Let $u = -ar^2$. Then $du = -2ar dr$, which means $r dr = -\frac{du}{2a}$.
The integral becomes:

$$\left[ -\frac{1}{2a} e^{-ar^2} \right]_0^\infty$$

Evaluating this at the boundaries:

* As $r \to \infty$, $e^{-ar^2} \to 0$.
* At $r = 0$, $e^0 = 1$.

So the inner integral evaluates to:

$$0 - \left( -\frac{1}{2a} (1) \right) = \frac{1}{2a}$$

Now, substitute this result back into the outer integral with respect to $\theta$:

$$I^2 = \int_0^{2\pi} \frac{1}{2a} d\theta$$

Since $\frac{1}{2a}$ is just a constant, evaluating the integral over $2\pi$ gives:

$$I^2 = \frac{1}{2a} \cdot 2\pi = \frac{\pi}{a}$$

**Step 5: Take the Square Root**

We now have the value for $I^2$. Since we established at the very beginning that $I$ must be positive, we simply take the positive square root:

$$I = \sqrt{\frac{\pi}{a}}$$

</details>
</div>

## Tricks

1. **Constant function to integral to derivative:**
   
    $$h \lVert \dfrac{x_l - x_{l-1}}{h} \rVert^2 = \int_{(l-1)h}^{lh} \lVert \dfrac{x_l - x_{l-1}}{h} \rVert^2 dt = \int_{(l-1)h}^{lh} \lVert \dfrac{d}{dt} \tilde{x}_h(t) \rVert^2 dt$$

2. **The standard trick is to split the kernel mass evenly between two Cauchy–Schwarz factors:**
   * **The natural attempt — Cauchy–Schwarz in $y$ — fails because $K\in L^1$, not $L^2$**
     
     $$\lvert K(x-y) f(y)\rvert = \lvert K(x-y)\rvert^{1/2} \cdot \lvert K(x-y)\rvert^{1/2} \lvert f(y)\rvert$$

## Proof Techniques

1. Proving $\sup_s A(s) \le \inf_t B(t)$ by pairwise comparison
    
<div class="accordion" markdown="1">
<details markdown="1">
<summary>Technique</summary>

Suppose we want to prove

$$\sup_{s\in S} A(s)\le \inf_{t\in T} B(t).$$

A sufficient—and in fact equivalent—condition is

$$A(s)\le B(t)\qquad\forall s\in S,\ \forall t\in T.$$

Indeed, if $A(s)\le B(t)$ for every pair $(s,t)$, then for each fixed $t$,

$$\sup_{s\in S} A(s)\le B(t),$$

and therefore

$$\sup_{s\in S} A(s)\le \inf_{t\in T} B(t).$$

**How to discover the pairwise inequality**

Work backwards from

$$A(s)\le B(t).$$

Rearrange it until it becomes an inequality controlled by the available structure: triangle inequality, Lipschitz continuity, convexity, monotonicity, Cauchy–Schwarz, etc.

A common metric-space form is

$$f(s)-r(s)\le f(t)+r(t),$$

equivalently

$$f(s)-f(t)\le r(s)+r(t).$$

If $f$ is $1$-Lipschitz and $r(z)=d(z,x)$, then

$$f(s)-f(t) \le d(s,t) \le d(s,x)+d(t,x),$$

so

$$f(s)-d(s,x)\le f(t)+d(t,x).$$

Hence

$$\sup_s\bigl(f(s)-d(s,x)\bigr)\le\inf_t\bigl(f(t)+d(t,x)\bigr).$$

**Interval interpretation**

If one needs to choose a scalar $\alpha$ satisfying

$$L(t)\le \alpha\le U(t)\qquad \forall t,$$

then such an $\alpha$ exists whenever

$$\sup_t L(t)\le \inf_t U(t).$$

To prove this, it is often easiest to show the stronger pairwise statement

$$L(s)\le U(t)\qquad \forall s,t.$$

**Heuristic**

When you see

$$\sup A \le \inf B,$$

do not attack the supremum and infimum directly. Try instead to prove

$$A(s)\le B(t)$$

for arbitrary independent points $s,t$, and then use the structure of the problem to control the difference.

</details>
</div>