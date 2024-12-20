+++
date = '2024-11-22T02:27:08+05:30'
draft = false
title = 'On a special property of numbers of the form @n^k + 1@'
+++

In this blog post we would be looking at some bounds on largest prime factors of numbers of the form @n^k + 1@.

**Proposition:**

Let @k@ be a positive integer, and let @\epsilon@ be a positive real number. Then there are infinitely many positive integers @n@, such that the largest prime factor of @n^k + 1@ is less than @n^\epsilon@.

**Solution:**

In the whole solution k and @\epsilon@ is fixed.

**Claim 1:**

The set of prime divisors of \{@n^k+1@ :@n\in\mathbb{N}@\} is an infinite set.

**Proof:**
For the sake of contradiction say @\exists@ only finitely many of them say@\{p_1,p_2,\dots,p_r\}@.Now set @n=p_1p_2{\dots}p_r@. Now we see none of @p_i@,where @i\in\{1,2,\dots,r\}@ divide @n^k+1@. Which is a contradiction.

Hence, the set of largest prime @p@ such that @p\mid(n^k+1)@ where @n\in\{1,2,3,\dots\}@ is infinite. If not say there are finitely many of them, say for each @n\in \mathbb{N}@ @n^k+1@ has a largest prime factor among the set@\{p_1,p_2,\dots,p_k\}@ but now again setting @n=p_1p_2{\dots}p_k@ we get a contradiction.

**Claim 2:**
@\forall\hspace{0.2 cm} \delta > 0 \hspace{0.2 cm}\exists@ infinitely many @m \in \mathbb{N}@
such that  @\frac{\varphi(2m)}{2m}<\delta@ ,where @\varphi(n)@ is the euler totient function.

**Proof:**
 Let the odd primes be \(p_1<p_2<\cdots\) and set \(m=p_1p_2\cdots p_k\). Then
 \begin{equation*}
\lim_{k\to\infty} \frac{\varphi(2m)}{2m}=\lim_{k\to\infty}\prod_{p\mid2m}{\left(1-\frac{1}{p}\right)}<e^{\lim_{k\to\infty}\left(-\sum_{p\mid2m} \left(\frac{1}{p} \right)\right)}<\delta 
\end{equation*}
Since @\sum_{p\mid2m} \frac{1}{p}@ diverges to @\infty@, @e^{\left(-\sum_{p\mid2m} \left(\frac{1}{p} \right)\right)}@ converges to @ 0@. And hence our previous line is justified, which completes our proof.

**Fact:**
-  \[x^n-1=\prod_{d\\mid n}\Phi_d(x)\]
Where @\Phi_d(x)@ is the d-th cyclotomic polynomial.
- deg(@\Phi_d(x)@) is @\varphi(d)@.

So we have
\begin{equation*}
x^{2n}-1=\prod_{d\mid2n}\Phi_d(x)
\end{equation*}
\begin{equation*}
\Rightarrow (x^n-1)(x^n+1)=\prod_{d\mid2n}\Phi_d(x)
\end{equation*}
\begin{equation*}
\Rightarrow (x^n+1)=\prod_{{d\mid2n}{\hspace{0.1cm}d\nmid n}}\Phi_d(x).
\end{equation*}

Now set n=@r^m@ for some @r \in\mathbb{N}@

@\Rightarrow n^k=r^{mk}@\\
Take @\epsilon_o=\frac{\epsilon}{k}@.

If @p\mid(n^k+1)@ then @p@ should divide some @\Phi_d(r^k)@ where @d\mid2m \hspace{0.1 cm}and \hspace{0.1 cm} d{\nmid}m@.(Here we would refer @p@ as the largest prime factor of @n^k+1@).

**Claim 3:**

If @d\mid2m \hspace{0.1 cm}and \hspace{0.1 cm} d{\nmid}m@ then we have @\varphi(d)<\varphi(2m)@.

**Proof:**

Writing d in its prime factorisation form ,writing k in its prime factorisation form and keeping in mind that @d\mid2m \hspace{0.1 cm} and \hspace{0.1 cm}d{\nmid}m@ it is quite straight forward to see.

Now since by **Claim 2** we have for any @\delta >0@ we have infinitely many @m\in\mathbb{N}@ for which @\frac{\varphi(2m)}{2m}<\delta@.

Setting @\delta=\frac{\epsilon_o}{2}@ we have infinitely many @m\in\mathbb{N}@  such that
\begin{center}
    @\frac{\varphi(2m)}{2m}<\frac{\epsilon_o}{2}@

@\Rightarrow \varphi(2m)<m\epsilon_o@
\end{center}
\begin{equation}
    \Rightarrow \varphi(d)<\varphi(2m)<m\epsilon_o 
\end{equation}
Since @p\mid\Phi_d(r^k)@ so we should have @p\le\Phi_d(r^k)@ 

Now for large enough @x \in \mathbb{N}@ we have @\Phi_d(x)\approx x^{\varphi(d)}@

@\Rightarrow \Phi_d(r^k)\approx r^{k\varphi(d)}@

so we have @p\le\Phi_d(r^k)\approx r^{k\varphi(d)}\le r^{k\varphi(2m)}<r^{km\epsilon_o}=n^{k\epsilon_o}=n^{\epsilon}@.

Now since from **Eqn 1** we get infinitely many such m's for which @\varphi(d)<m\epsilon_o@ and since @n=r^m@ we get infinitely many such @n \in\mathbb{N}@ and for all of them we have @p<n^{\epsilon}@  and hence this completes our proof.

