# The Real Numbers

## Some Preliminaries

::: theorem
**Theorem 1**. *If $m|n$ for $m$ and $n\in \mathbb{Z}$, then $m|n^2$.*
:::

::: proof
*Proof.* If $m$ divides $n$ if and only if there exists an integer $k$
such that $n=km$. Therefore, $n^2=(km)^2=k(km^2)$. ◻
:::

::: {#sqr_div .theorem}
**Theorem 2**. *If $m \nmid q^2$ for any $q \in \{ 1,2,\dots,m-1 \}$,
then $m|n^2$ implies $m|n$.*
:::

::: proof
*Proof.* $m\nmid n$ if and only if there exists $k\in \mathbb{Z}$ and
$q\in\{1,\dots,m-1\}$ such that $n=km+q$. Therefore,
$n^2=(mk)^2+2qmk+q^2$, which after factoring is $mp+q^2$ where
$p\in\mathbb{Z}$. Thus, $m|n^2$ only if $m|q^2$, but we assumed the
negation, so $m \nmid n^2$. ◻
:::

#### Exercise 1.2.1.

(a) Assume for the sake of contradiction that $\sqrt{3}$ is rational.
    Then there exists co-prime integers $p$ and $q$ such that
    $(p/q)^2=3$. Thus $p^2=3q^2$, and since 3 divides neither $1^2$ nor
    $2^2$, by [2](#sqr_div){reference-type="ref+label"
    reference="sqr_div"}, $p=3k$ for some integer k. Therefore
    $q^2=3k^2$ and so $q=3r$ for some integer $r$. That would mean $p$
    and $q$ are not co-prime, which is a contradiction. Moreover, 6
    $\nmid q^2$ for any $q\in \{1,2,3,4,5\}$, and so a similar argument
    can be made.

(b) In trying to use a similar argument, we will fail to infer that $q$
    is also even. In detail, if $(p/q)^2=4$ then $p^2=4q^2$ and so
    $p=2k$ for an integer $k$. Thus $4k^2=4q^2$, and so $k^2=q^2$, which
    fails to provide any information about the parity of $q$.

<!-- -->

(a) If

::: {#even_pow .theorem}
**Theorem 3**. *An integer $p$ is even if and only if $p^n$ is even for
any natural $n$.*
:::

::: proof
*Proof.* ($\implies$) If $p$ is even, then $p=2k$ for some integer $k$,
and so $p^2=(2k)^2=2(2k^2)=2r$ where $r$ is an integer. Thus $p^2$ is
even. Furthermore, if $p^n$ is even then $p^{n+1}=p^np$ which is the
product of even integers, and thus even. ($\impliedby$) Conversely, if
$p$ is odd, then $p=2k+1$ for some integer $k$, and so
$p^2=2(2k^2+2k)+1=2r+1$ for some integer $r$. Thus $p^2$ is odd.
Furthermore, if $p^n$ is odd, then $p^{n+1}=p^np$ which is the product
of odd integers, and thus odd. ◻
:::

#### Exercise 1.2.2.

Assume for the sake of contradiction that there exists some rational $r$
satisfying $2^r=3$. Then there exists integers $p$ and $q$ such that
$r=p/q$, and so $2^p=3^q$. We know $r$ cannot be 0, because $1 \neq 3$,
and so $p$ and $q$ are not 0. Also $p$ and $q$ cannot be negative,
because if $p$ were negative then $r$ would be negative, and
$1/2^r \neq 3$ for any natural $r$. Therefore $p$ and $q$ must be
natural. By [3](#even_pow){reference-type="ref+label"
reference="even_pow"}, we know $2^p$ is even and $3^q$ is odd. An even
number is never odd, and so we have a contradiction.

#### Exercise 1.2.3.

(a) False. Let $A_n=\{n,n+1,\dots\}$. Assume for the sake of
    contradiction that there exists some natural $a$ in
    $\bigcap_{n=1}^\infty A_n$. Then $a$ must be in every
    $\{A_n\}_{n=1}^\infty$, but $a \notin A_{a+1}$. Therefore
    $\bigcap_{n=1}^\infty A_n = \emptyset$.

(b) True.

(c) False.
    $\{1\} \cap (\{1\}\cup\{1,2\}) = \{1\} \neq \{1,2\}=(\{1\}\cap\{1\})\cup\{1,2\}.$

(d) True.

(e) True.

#### Exercise 1.2.4.

To construct $A_n$, we may lay the natural number out diagonally as
follows.

   $A_1$    $A_2$      $A_3$      $A_4$     $\dots$
  ------- ---------- ---------- ---------- ---------
     1        3          6       $\vdots$  
     2        5       $\vdots$             
     4     $\vdots$                        
     ⋮                                     

Here we have an infinite set $A_n$ for every $n\in\mathbb{N}$. Moreover,
each natural number appears in exactly one set, so
$A_i\cap A_j=\emptyset$ for $i\neq j$ and
$\bigcup_{i=1}^\infty A_i = \mathbb{N}$.

#### Exercise 1.2.5 (De Morgan's Laws).

We will assume De Morgan's law for predicate logic.

(a) $x\in(A\cap B)^c \iff \neg(x\in A\cap B) \iff \neg(x\in A \text{ and } x \in B) \iff \neg(x\in A) \text{ or } \neg(x\in B) \iff x\in A^c \text{ or } x\in B^c \iff x \in A^c \cup B^c$.

(b) The inverse follows from the above, and so
    $(A\cap B)^c = A^c \cup B^c$.

(c) $x\in (A\cup B)^c \iff \neg(x\in A \text{ or } x\in B) \iff x\in A^c \text{ and } x\in B^c\iff x\in A^c\cap B^c$.

#### Exercise 1.2.6.

(a) If $a$ is positive then $a=|a|$. If $a$ and $b$ are positive, then
    $a+b$ is positive, so $|a+b|=a+b=|a|+|b|$.

    If $a$ is negative then $-a=|a|$. If $a$ and $b$ are both negative,
    then $a+b$ is negative, so $|a+b|=-(a+b)=(-a)+(-b)=|a|+|b|$.

(b) $(a+b)^2=a^2+2ab+b^2$ and
    $(|a|+|b|)^2=|a|^2+2|a||b|+|b|^2=a^2+2|a||b|+b^2$, because
    $|a|^2=|a^2|=a^2$. Therefore $(a+b)^2 \leq (|a|+| b|)^2$ if and only
    if $ab\leq|a||b|$. We may re-arrange that inequality as
    $\pm a\leq |a|$, which is always the case. Finally, if $x$ and $y$
    are positive, $x\leq y$ if and only if $x^2\leq y^2$, and so
    $|a+b|\leq|a|+|b|$.

(c) Assuming the triangle inequality,
    $|a+b+c|=|a+t|\leq|a|+|t|=|a|+|b+c|\leq|a|+|b|+|c|$. Therefore
    $|a-b|=|(a-c)+(c-d)+(d-b)|\leq |a-c|+|c-d|+|d-b|$.

(d) Let $|a|\geq |b|$. Then $|a|-|b|=\epsilon$, for some
    $\varepsilon \geq0$. Therefore
    $||a|-|b||=|\varepsilon|=\varepsilon=|a|-|b|$. By the unremarkable
    identity, that is equivalent to $|(a-b)+b|-|b|$, which by the
    Triangle Inequality is $\leq |a-b|$.

::: {#sub_range .theorem}
**Theorem 4**. *If $A \subseteq B$ then $g(A) \subseteq g(B)$.*
:::

::: proof
*Proof.* $y\in g(A)$ if and only if $\exists x \in A$ such that
$g(x)=y$. Furthermore, since $x\in A$, then $x\in B$, and so
$\exists x \in B$ such that $g(x)=y$. Therefore $y\in g(B)$. ◻
:::

#### Exercise 1.2.7.

(a) $f(A\cap B)=[1,4]=f(A)\cap f(B)$. And
    $f(A\cup B)=[0,16]=f(A)\cup f(B)$.

(b) Let $A=[-2,-1]$ and let $B=[1,2]$. Then
    $f(A\cap B)=\emptyset \neq [1,4] = f(A)\cap f(B)$.

(c) If $y\in g(A\cap B)$ then, by
    [4](#sub_range){reference-type="ref+label" reference="sub_range"},
    $y\in g(A)$ and $y\in g(B)$ and so $y\in g(A) \cap g(B)$.

(d) *Conjecture.* $g(A\cup B) = g(A) \cup g(B)$. *Proof.* If
    $y\in g(A) \cup g(B)$ then $y\in g(A)$ or $y\in g(B)$. If
    $y\in g(A)$ then $y\in g(A\cup B)$, because $A\subseteq A\cup B$.
    Likewise for $y\in g(B)$. Conversely, if $y\in g(A\cup B)$, then
    $\exists x \in A$ or $\exists x \in B$ such that $g(x)=y$. If
    $x\in A$ then $y \in g(A)$ whereby for free we get that
    $y\in g(A) \cup g(B)$. Likewise for $x \in B$.

#### Exercise 1.2.8.

(a) $f(n)=2n$.

(b) $f(n) = n/2$ if $n$ is even, otherwise $(n+1)/2$ if $n$ is odd.

(c) $f(n) = n/2$ if $n$ is even, otherwise $-(n-1)/2$ if $n$ is odd.

::: theorem
**Theorem 5**. *For any $x$ in the domain of $f$, $x\in f^{-1}(A)$ if
and only if $x\in A$.*
:::

::: proof
*Proof.* By definition $x\in f^{-1}(A)$ if and only if
$x\in \{x\in D: f(x) \in A\}$, therefore $f(x)\in A$. ◻
:::

#### Exercise 1.2.9.

(a) $f^{-1}(A) = [0,2]$ and $f^{-1}(B) = [0,1]$. So
    $f^{-1}(A\cap B) = [0,1] = f^{-1}(A) \cap f^{-1}(B)$. And
    $f^{-1}(A\cup B) = [0,2] = f^{-1}(A) \cup f^{-1}(B)$.

(b) $x\in g^{-1}(A\cap B) \iff g(x) \in A\cap B \iff g(x) \in A$ and
    $g(x) \in B$ $\iff x\in g^{-1}(A)$ and $x \in g^{-1}(B)$
    $\iff x\in g^{-1}(A)\cap g^{-1}(B)$.

    $x\in g^{-1}(A\cup B) \iff g(x)\in A$ or $g(x) \in B$
    $\iff x\in g^{-1}(A)$ or $x\in g^{-1}(B)$
    $\iff x\in g^{-1}(A) \cup g^{-1}(B)$.

#### Exercise 1.2.10.

(a) *Counterexample.* If $a=b$ then $a-b=0$ and $\varepsilon > 0$ so
    $a-b < \varepsilon$. Therefore $a<b+\varepsilon$. So the posterior
    condition holds, but $a=b$ so clearly the anterior condition does
    not hold.

(b) *Proof.* Since $\varepsilon > 0$, then $\varepsilon + b > b$.
    Therefore, if $a<b$, then $a<b<b+\varepsilon$.

(c) *Proof.* If $a\leq b$ then $a\leq b < b+\varepsilon$ for
    $\varepsilon > 0$. Conversely, let $a<b+\varepsilon$ for
    $\varepsilon > 0$, and assume for the sake of contradiction that
    $a > b$. Because $a > b$ then $a-b$ is some positive
    $\varepsilon_0$. But we know $a<b+\varepsilon$ for any positive
    $\varepsilon$. so surely, $a-b<\varepsilon_0$, but that is a
    contradiction to the fact that $a-b=\varepsilon_0$. Therefore it
    must be that $a\leq b$.

#### Exercise 1.2.11.

(a) There exists real numbers satisfying $a<b$ where $(a+1)/n \geq b$
    for all $n\in \mathbb{N}$. I will guess that the claim is true.

(b) For all real numbers $x>0$, there exists some $n\in \mathbb{N}$ such
    that $x\geq 1/n$. I will guess that the negation is true.

(c) There exists two distinct real numbers that has no rational number
    between them.

#### Exercise 1.2.12.

(a) $y_1=6>-6$, and
    $y_n>-6 \implies 2y_n > =-12 \implies 2y_n -6 > -18 \implies (2y_n-6)/3 > -6 \implies y_{n+1} > -6$.

(b) $y_1=6 > 2 = (2y_1-6)/3=y_2$, and
    $y_n>y_{n+1} \implies (2y_n-6)/3 > (2y_{n+1}-6)/3 \implies y_{n+1} > y_{n+2}$.

#### Exercise 1.2.13.

(a) $(A_1)^c=A_1^c$, and $(A_1\cup A_2)^c=A_1^c \cap A_2^c$ as shown in
    Exercise 1.2.5. Finally
    $(\bigcup_{i=1}^nA_i)^c = \bigcap_{i=1}^n A_i^c \implies \bigcap_{i=1}^{n+1} A_i^c = (\bigcup_{i=1}^nA_i)^c \cap A_{n+1}^c = (\bigcup_{i=1}^nA_i \cup A_{n+1})^c = (\bigcup_{i=1}^{n+1}A_i)^c$.

(b) Let $B_i=\{i, i+1,...\}$ for any $i \in \mathbb{N}$. Then
    $\bigcap_{i=1}^\infty B_i = \emptyset$, but
    $n \in \bigcap_{i=1}^{n}B_i$.

(c) ($\subseteq$)
    $(\bigcup_{i=1}^\infty A_i)^c \subseteq \bigcap_{i=1}^\infty A_i^c$
    if and only if $x\notin (\bigcup_{i=1}^\infty A_i)^c$ or
    $x\in \bigcap_{i=1}^\infty A_i^c$, which is the case when
    $x\in(\bigcup_{i=1}^\infty A_i) \cup (\bigcap_{i=1}^\infty A_i^c)$,
    and so, using the infinite distributive law,
    $x\in \bigcap_{j=1}^\infty(\bigcup_{i=1}^\infty A_i\cup A_j^c)$.
    Note that
    $\bigcup_{i=1}^\infty A_i\cup A_j^c = \ldots \cup A_j \cup A_j^c \cup \ldots = \mathcal{U}$.
    So, $x \in \mathcal{U}$, which is always the case.

    ($\supseteq$) Similar to before,
    $(\bigcup_{i=1}^\infty A_i)^c \supseteq \bigcap_{i=1}^\infty A_i^c$
    if and only if $x\notin \bigcap_{i=1}^\infty A_i^c$ or
    $x\in (\bigcup_{i=1}^\infty A_i)^c$, which is the case when
    $x \notin \bigcap_{i=1}^\infty A_i^c \cap \bigcup_{i=1}^\infty A_i$.
    Moreover, by the infinite distributive law, we know
    $x\notin \bigcup_{j=1}^\infty(\bigcap_{i=1}^\infty A_i^c \cap A_j)$.
    Note that
    $\bigcap_{i=1}^\infty A_i^c \cap A_j = \ldots \cap A_j^c \cap A_j \cap \ldots = \emptyset$.
    Therefore $x\notin \emptyset$, which is always the case.

## The Axiom of Completeness

#### Exercise 1.3.1.

(a) A real number $i$ is the *greatest lower bound* for a set
    $A \subseteq R$ if it meets the following two criteria: (i) $i$ is a
    lower bound for A; (ii) if $l$ is any lower bound for $A$ then
    $l \leq i$.

(b) *Lemma.* Let $l \in \mathbb{R}$ be a lower bound for
    $A \subseteq R$. Then $l = \inf A$ if and only if for every
    $\varepsilon > 0$, there exists some $a\in A$ such that
    $a < l + \varepsilon$. *Proof.* If $l=\inf A$ then
    $l + \varepsilon > l$ and thus is not a lower bound, consequently it
    is not the case that $l + \varepsilon \leq a$ for every $a \in A$.
    In other words, there is some $a \in A$ such that
    $l + \varepsilon > a$. Conversely, if $l$ is a lower bound, and
    every value greater than $l$ given by $l + \varepsilon$ is no longer
    a lower bound, then all lower bounds must be less than or equal to
    $l$. Therefore $l = \inf A$.

#### Exercise 1.3.2.

(a) *Example.* $B = \{1\}.$ The max and min of $B$ is $1$, so the $\inf$
    and $\sup$ of $B$ is 1. Therefore $\inf B \geq \sup B$.

(b) *Impossible.* If set $B$ contains it's infimum then it is clearly
    non-empty. Additionally, since $B$ is finite, it has a maximum,
    which is it's supremum. Therefore, it must contain it's supremum.

(c) *Example.* Let $B = \{ r \in Q : 1 < r \leq 2 \}$. We have
    $\sup B = 2$, which is in $B$, but $\inf B = 1$, which is not in
    $B$.

#### Exercise 1.3.3.

(a) Since $A$ is bounded below, $B$ is non-empty. Moreover,
    $\inf A \in B$ and $\inf A \geq b$ for any $b \in B$. Therefore,
    $\inf A$ is also the maximum of $B$, and so $\sup B = \inf A$.

(b) For any non-empty $A \subseteq \mathbb{R}$ that is bounded below,
    let $B$ be the set of it's lower bounds. We know $B$ is non-empty
    because $A$ is bounded below, and that it is bounded above by any
    $a \in A$. Therefore, by the Axiom of Completeness,
    $\sup B \in \mathbb{R}$, and finally, by part (a), we know that
    $\inf A \in \mathbb{R}$.

#### Exercise 1.3.4.

(a) Let $\alpha = \max\{\sup A_1, \sup A_2\}$, and let
    $a \in A_1 \cup A_2$, so that $a \in A_1$ or $a \in A_2$. If
    $a \in A_1$, we know $\alpha \geq \sup A_1$, and so $\alpha \geq a$.
    The same can be said for $a \in A_2$. Therefore, for $\alpha$ is an
    upper bound for $A_1 \cup A_2$. Additionally, for any
    $\varepsilon > 0$, $\alpha - \epsilon$ is less than $\sup A_1$ or
    $\sup A_2$. If $\alpha - \varepsilon < \sup A_1$, then there exists
    $a \in A_1$ such that $\alpha - \varepsilon < a$. Moreover, $a$ must
    but be in $A_1 \cup A_2$. The same can be said for $A_2$. Therefore
    $\alpha = \sup(A_1 \cup A_2)$.

    So now we know that $\max\{\sup A_1\} = \sup A_1$, and
    $\max\{\sup A_1, \sup A_2\} = \sup(A_1 \cup A_2)$. Assume that
    $\sup(\bigcup_{k=1}^n A_k) = \max\{\sup A_k\}_{k=1}^n$. Then,
    $\sup(\bigcup_{k=1}^{n+1} A_k) = \sup(\bigcup_{k=1}^{n} A_k \cup A_{n+1}) = \max\{\sup \bigcup_{k=1}^{n} A_k, \sup A_{n+1}\} = \max\{\max\{\sup A_k\}_{k=1}^n, \sup A_{n+1}\} = \max\{\sup A_k\}_{k=1}^{n+1}$.
    And so the formula is valid for any finite $n$.

(b) The formula does not always hold in the infinite case. If
    $\sup(\bigcup_{k=1}^\infty A_k)$ is not bounded above, then it can
    of course have no least upper bound. Let $A_k = \{ k \}$, so that
    $A_k$ is non-empty and bounded above by $k$. Now, for any $b$, we
    know $b+1 \in A_{b+1}$, and so $b+1 \in \bigcup_{k=1}^\infty A_k$.
    Therefore, $\bigcup_{k=1}^\infty A_k$ is not bounded above.

#### Exercise 1.3.5.

(a) \(i\) For any $a \in A$, by definition $\sup(A) \geq a$, and so, for
    $c \geq 0$, we also have $c\sup(A) \geq ca$. Therefore, $c\sup(A)$
    is an upper bound of $cA$. (ii) For any $\varepsilon > 0$, there is
    some $a \in A$ such that $\sup(A)-\varepsilon < a$, and likewise,
    $c\sup(A) - \varepsilon < ca$. Therefore, $c\sup(A)$ is the supremum
    of $cA$.

(b) \(i\) For any $a\in A$, by definition $\inf(A) \leq a$, and so, for
    $c < 0$, we also have $c\inf(A) \geq ca$. Therefore $c\inf(A)$ is an
    upper bound of $cA$. (ii) Let $l$ be any upper bound of $cA$, that
    is, $b \geq ca$ for any $a \in A$. Equivalently, $b/c \leq a$, and
    so, $b/c \leq \inf(A)$. Multiplying through by $c$, we get
    $b \geq c\inf(A)$. Therefore, $c\inf(A)$ is the supremum of $cA$
    when $c<0$.

#### Exercise 1.3.6.

(a) By definition $s \geq a$ for any $a \in A$, and $t \geq b$ for any
    $b \in b$. Therefore, $s + t \geq a + b$ for any $a$ and $b$. So,
    $s+t$ is an upper bound for $A + B$.

(b) Let $u$ be an arbitrary upper bound for $A+B$, then by definition
    $u \geq a+b$ for any $a\in A$ and $b\in B$. Equivalently,
    $u-a \geq b$, and so $u-a$ is an upper bound for $B$. Therefore,
    $u-a \geq t$ must hold.

(c) Following from above, we have $u-a\geq t$ for an arbitrary
    upper-bound of $A+B$ given by $u$, and any $a \in A$. Equivalently,
    $u-t\geq a$, so $u-t$ is an upper bound for $A$, and necessarily,
    $u-t\geq s$. Equivalently, $u\geq t+s$, and therefore $s+t$ is the
    supremum of $A+B$.

(d) By Lemma 1.3.8, every any $\varepsilon > 0$, there exists $a\in A$
    and $b \in B$ such that $s-\varepsilon < a$ and $t-\varepsilon < b$.
    Therefore, $s+t-\varepsilon < a+b$, and by the converse of Lemma
    1.3.8, $s+t$ is the supremum of $A+B$.

#### Exercise 1.3.7.

Let $a$ be an upper bound for $A$ and also an element of $A$. (ii) Any
other upper bound can be no less than $a$, because $a \in A$, so $a$ is
the supremum.

#### Exercise 1.3.8.

(a) $\sup = 1$, $\inf = 0$.

(b) $\sup=1$, $\inf=-1$.

(c) $\sup=1/3$, $\inf=1/4$.

(d) $\sup=1$, $\inf = 0$.

#### Exercise 1.3.9.

(a) By Lemma 1.3.8, we know that there exists $b \in B$ satisfying
    $\sup(B) - \varepsilon < b$ for every $\varepsilon > 0$. Let $b$
    satisfy the case when $\varepsilon = \sup(B) - \sup(A)$. That means
    $\sup(A) < b$, and so $b$ is an upper bound for $A$.

(b) Let $A=\{1\}$ and let $B=\{n/(n+1): n\in \mathbb{N}\}$. We have
    $\sup(A)=1=\sup(B)$, but $1 > b$ for any $b\in B$, and therefore
    there is no $b\in B$ that is an upper bound for $A$.

#### Exercise 1.3.10. (Cut Property)

(a) Let $c=\sup(A)$. Since $A$ is non-empty, by the Axiom of
    Completeness, $\sup(A) \in \mathbb{R}$. Because
    $A\cup B = \mathbb{R}$, and $A \cap B = \emptyset$, every real
    number must be in exclusively one or the other. So, if
    $\sup(A) \in A$, then we know $\sup(A) < b$ for every $b \in B$.
    Otherwise, if $\sup(A) \in B$, then $\sup(A) = \inf(B)$, because,
    for any $\varepsilon > 0$, we have
    $\sup(A) + \varepsilon > \sup(A)$. So, since $\sup(A) = \inf(B)$, it
    must be that $\sup(A) \leq b$ for every $b\in B$. Additionally, by
    definition, $\sup(A) \geq a$ for every $a\in A$.

(b) Let $E$ be a non-empty set that is bounded above, and let $A$ be the
    set of reals where $a > x$ for every $a\in A$ and $x\in E$. Since
    $E$ is bounded above, there exists some $y \in \mathbb{R}$ such that
    $y \geq x$ for every $x \in E$. Therefore, $y+1 > x$, and so $A$ is
    non-empty. Then, by the Cut Property, there exists
    $c \in \mathbb{R}$ such that $x \leq c \leq a$ for every $x \in E$
    and $a \in A$. If $c\in E$, then $c$ is the maximum of $E$ and thus
    $\sup(E)=c$. If $c\notin E$ then $c\in A$, and so $c$ is the minimum
    of $A$. Then, for any $\varepsilon > 0$, we may construct
    $x = c-\varepsilon/2$, which must be in $E$ as it is less than
    $\min(A)$, to satisfy $c - \varepsilon < x$. Therefore,
    $\sup(E) = c$.

(c) Let $A = \{r \in \mathbb{Q}: r^2 < 2 \text{ or } r < 0 \}$ and let
    $B = \{r \in \mathbb{Q}: r^2 \geq 2 \text { and } r \geq 0\}$. We
    have $A \cup B = \mathbb{Q}$, and $A \cap B = \emptyset$.
    Additionally, $a < b$ for any $a \in A$ and $b \in B$. There is only
    one $c$ that satisfies, $a \leq c \leq b$. That is, when $c^2 = 2$,
    but then $c \notin \mathbb{Q}$.

#### Exercise 1.3.11.

(a) *True.* $\sup(B) \geq b$ for every $b \in B$, and any $a \in A$ is
    also in $B$, so $\sup(B) \geq a$ for any $a \in A$. Therefore,
    $\sup(B)$ is an upper bound for $A$, and so $\sup(B) \geq \sup(A)$.

(b) *True.* If $\sup(A) < \inf (B)$ then $\inf(B) - \sup(A) > 0$, so let
    $\inf(B) - \sup(A) = \varepsilon_0$. Let
    $c = \sup(A) + \varepsilon_0/2$. Then,
    $c < \sup(A)+\varepsilon_0 = \inf(B) \leq b$ for any $b \in B$.
    Also, $c > \sup(A) \geq a$ for any $a \in A$. Thus, $a < c< b$ for
    all $a \in A$ and $b \in B$.

(c) *False.* Let $A = [0,2)$ and $B = (2, 4]$. Then, for $c =2$, it
    follows that $a<c<b$ for every $a\in A$ and $b \in B$. But,
    $\sup(A) = 2 = \inf(B)$, and the converse of (b) does not hold.

## Consequences of Completeness

#### Exercise 1.4.1.

(a) Let $a$ and $b$ be rational numbers, so that $a=p/m$ and $b=q/n$ for
    $p,q\in \mathbb{Z}$ and $m,n\in \mathbb{N}$. Then, $ab=pq/mn$, which
    is a rational because $pq\in \mathbb{Z}$ and $mn \in \mathbb{N}$.
    Additionally, $a+b=(pn+bm)/mn$ which is rational. Therefore,
    $\mathbb{Q}$ is closed under addition and multiplication.

(b) Let $a\in \mathbb{Q}$ and $t\in \mathbb{I}$. Then, if $a+t$ were
    some rational $b$, that would mean $t=b-a$, which would be a
    contradiction as $b-a \in \mathbb{Q}$. Also, if $at$ were some
    rational $b$, that would mean $t=b/a$, which would be a
    contradiction as $b/a \in \mathbb{Q}$ for $a \neq 0$. Therefore,
    $a+t\in I$ and $at \in I$.

(c) $\sqrt{2}\times \sqrt{2} = 2$ which is not in $\mathbb{I}$, so
    $\mathbb{I}$ is not closed under multiplication. Also,
    $\sqrt{2} + (1 - \sqrt{2}) = 1$, which is not in $\mathbb{I}$, and
    thus $\mathbb{I}$ is not closed under addition.

#### Exercise 1.4.2.

First, to show that $s$ is an upper bound for $A$. By the Archimedean
Property, for any $\varepsilon > 0$, there exists $n\in \mathbb{N}$ such
that $1/n < \varepsilon$, and so $s+\varepsilon > 1/n > a$ for any
$a \in A$. Therefore, $s\geq a$ for any $a\in A$, making $s$ an
upper-bound. Now, to show that $s$ is the least upper-bound. Similar to
before, for any $\varepsilon$ there exists $n$ such that
$s-\varepsilon < s-1/n < a$ for some $a \in A$. Therefore, $s$ is the
supremum.

#### Exercise 1.4.3.

$0 \notin (0,1)$ so $0\notin \bigcap_{n=1}^\infty (0,1/n)$.
Additionally, for any $\varepsilon > 0$ there exists $n\in \mathbb{N}$
such that $1/n < \varepsilon$, and so $\varepsilon \notin (0,1/n)$.
Therefore $\bigcap_{n=1}^\infty (0,1/n)$ is empty.

#### Exercise 1.4.4.

Since $T \subseteq [a,b]$ and $\sup[a,b] = b$, it must be that $b$ is an
upper-bound for $T$. Additionally, for any $\varepsilon > 0$, there
exists $c\in [a,b]$ such that $b-\varepsilon < c$. And since
$\mathbb{Q}$ is dense in $\mathbb{R}$, there exists $r\in \mathbb{Q}$
such that $b-\varepsilon < r < c$. Therefore $\sup T = b$.

#### Exercise 1.4.5.

For any reals $a<b$, we know $a+\sqrt{2}<b+\sqrt{2}$ are also reals, and
so, there exists $r\in \mathbb{Q}$ satisfying
$a+\sqrt{2} < r < b+\sqrt{2}$. Therefore, $a < r-\sqrt{2} < b$, where
$r-\sqrt{2}$ is certainly irrational. Therefore $\mathbb{I}$ is dense in
$\mathbb{R}$.

#### Exercise 1.4.6.

(a) Let $a=0$, and $b=1/11$. By inspection, there is no
    $p\in \mathbb{Z}$ and $q\in \mathbb{N}$ satisfying $q \leq 10$ and
    $0<p/q<1/11$. Therefore rationals of that form are not dense in
    $\mathbb{R}$.

(b) Let $a<b$ be real numbers. Then there exists $n \in N$ satisfying
    $1/n < b-a$ and so $1/2^n < 1/n < b-a$. Equivalently $b-1/2^n > a$.
    Now let integer $m = 2^na+ 1$, so that $m>2^na\geq m-1$. Immediately
    we get that $m/2^n>a$. Additionally, $2^n(b-1/2^n) > 2^na \geq m-1$
    and so $b>m/2^n$. Therefore, there exists $m\in \mathbb{Z}$ and
    $n\in \mathbb{N}$ satisfying $a<m/2^n<b$.

(c) The smallest positive rational satisfying $10|p|\geq q$ is $p=q/10$.
    In that case $p/q=1/10$. Therefore, there is no such $p/q$
    satisfying $0<p/q<1/11$ and so they are not dense in $\mathbb{R}$.

#### Exercise 1.4.7.

Assume for the sake of contradiction that $\alpha= \sup T$ satisfies
$a^2>2$. Clearly $\alpha > \alpha - 1/n$. Now to show that $a-1/n$
remains an upper-bound, that is, $(\alpha-1/n)^2 \geq 2$. Expanding the
left side of the inequality, we get
$(\alpha-1/n)^2 = \alpha^2 - 2\alpha /n + 1/n^2 > \alpha^2 - 2\alpha/n$.
Now, let $n$ satisfy $n > 2\alpha / (\alpha^2 - 2)$ so that
$2\alpha /n < \alpha^2 -2$. Thus,
$\alpha^2 - 2\alpha /n > \alpha^2 - (\alpha^2 -2) = 2$. Therefore if
$\alpha^2 > 2$ it can not be the supremum.

#### Exercise 1.4.8.

1.  *Example.* Let
    $A = (2n-1)/2n = \{ \frac{1}{2}, \frac{3}{4}, \frac{5}{6}, \ldots \}$
    and
    $B = 2n/(2n+1) = \{ \frac{2}{3}, \frac{4}{5}, \frac{6}{7}, \ldots\}$.
    These sets satisfy $A \cap B = \emptyset$, $\sup A = \sup B = 1$,
    and $1\notin A \cup B$.

2.  *Example.* Let
    $J_n = (2-\frac{1}{n}, 2+\frac{1}{n}) = \{ x \in \mathbb{R}: 2-\frac{1}{n}< x < 2+\frac{1}{n}\}$.
    Then for any $n$, $2-1/n < 2-1/(n+1)$ and $2+1/(n+1) < 2+1/n$.
    Therefore $J_n \subseteq J_{n+1}$. Now let $A = \{ 2-1/n : n\in N\}$
    or the set of left-hand endpoints, and $B = \{ 2+1/n: n\in N\}$ or
    the set of right-hand endpoints. Then $\sup A = 2$ and $\inf B = 2$
    but $2\notin A$ and $2\notin B$ so $a_n < 2 < b_n$ for all $n$.
    Therefore $2\in J_n$ for any $n$ and so
    $2\in \bigcap_{n=1}^\infty J_n$. Now to show that
    $\bigcap_{n=1}^\infty J_n$. Assume for the sake of contradiction
    that there is some $c \neq 2$ in $\bigcap_{n=1}^\infty J_n$. We may
    not have $c > 2$ because $c\notin J_n$ for $1/n < c-2$. Moreover it
    can not be that $c < 2$ because $c\notin J_n$ for $1/n>2-c$.
    Therefore $\bigcap_{n=1}^\infty$ is finite as it contains only 2.

3.  *Example.* Let
    $L_n = \mathbb{N}\cap [n,\infty) = \{ n, n+1, \ldots \}$. Then any
    $n \notin L_{n+1}$ and so $\bigcap_{n=1}^\infty L_n = \emptyset$.

4.  *Impossible.* Let $I_n = [a_n, b_n]$ and
    $J_n = \bigcap_{k=1}^n I_k$. Then for any $x \in J_n$ it must be
    that $x \geq a$ for all $a \in \{a_1, \ldots, a_n\}$ and $x\leq b$
    for all $b \in \{b_1, \ldots, b_n\}$. By our assumption that
    $\bigcap_{k=1}^n I_k = J_n$ is non empty for every
    $n\in \mathbb{N}$, we must conclude that $J_n$ is a valid closed
    interval. Additionally, since
    $\bigcap_{k=1}^n I_k \supseteq \bigcap_{k=1}^{n+1} I_k$ it follows
    that $J_n \supseteq J_{n+1}$ for any $n \in \mathbb{N}$. Finally, by
    the Nested Interval Property,
    $\bigcap_{n=1} ^\infty I_n = \bigcap_{n=1}^\infty J_n \neq \emptyset$.

## Cardinality

#### Exercise 1.5.1.

Let $n_1 = \min\{n\in \mathbb{N}: f(n) \in A\}$, and in general, let
$n_k = \min\{ n\in \mathbb{N}: f(n) \in A, n > n_{k-1}\}$. That means
$n_k$ is the $k^{th}$ smallest natural number in $f^{-1}(A)$. Surely
each $n_k$ is unique because the sequence is strictly increasing. Also,
let $n \in f^{-1}(A)$, surely $\{ m \in f^{-1}(A) : m < n\}$ is finite,
so $n$ is greater than some number of elements in $f^{-1}(A)$. Let that
number be $k$, then $a_k = n$. We may use this correspondence of natural
number to define $g:\mathbb{N}\to A$, where $g(k) = f(n_k)$ for every
$k\in N$.

#### Exercise 1.5.2.

The Nested Interval Property asserts the existence of some
$x\in \mathbb{R}$ in the infinite intersection of nested closed
intervals. So the error in the proof is that the element in
$\bigcap_{n=1}^\infty I_n$ is not necessarily rational, and so there is
no certainty of a contradiction.

#### Exercise 1.5.3.

(a) Let $A_1$ and $A_2$ be countable sets, and let
    $B_2 = A_2 \backslash A_1$. Since $A_1$ countable, there exists a
    1-1 correspondence $f: \mathbb{N}\to A_1$. Also, since
    $B_2 \subseteq A_2$, either $B_2$ is countable or finite. If $B_2$
    is countable, then there exists a 1-1 correspondence
    $g: \mathbb{N}\to B_2$. Then, we may define the function
    $g:\mathbb{N}\to A_1 \cup B_2$ given by
    $h = \begin{cases}f((n+1)/2) & \text{ if n is odd }\\ g(n/2) & \text{ if n is even }\end{cases}$.
    Since $A_1$ and $B_2$ are disjoint, for every $n\in \mathbb{N}$,
    $g(n)$ is in exclusively one of $A_1$ or $B_2$. Furthermore, for any
    $a\in A_1$, there is exactly one $n\in \mathbb{N}$ satisfying
    $f(n) = a$, and there is exactly one $m\in N$ satisfying
    $h(m) = f(n)$ given by $m=2n-1$. Similarly, for every $b\in B_2$,
    there is exactly one $n$ satisfying $g(n)=a=h(2n)$. Therefore, $h$
    is a 1-1 correspondence. Otherwise, if $B_2$ is finite, then it has
    some $k$ elements and there exists a 1-1 correspondence
    $g:\{1,2,\ldots,k\} \to B_2$. Then, we may define
    $h = \begin{cases} g(n)& n \leq k \\ f(n-k) &n > k\end{cases}$. Now,
    for every $a\in A_1$ there is exactly one $n\in \mathbb{N}$ and
    $m\in\mathbb{N}$ satisfying $f(n)=a=h(m)$ for $m=n+k$. Moreover, for
    any $b \in B_2$, $f(n)=b=h(n)$ for exactly one $n\in \mathbb{N}$.
    Therefore, $h$ is once again a 1-1 correspondence. The union of any
    two countable sets is countable. The general statement for the union
    of $m$ sets follows by induction. We have that $A_1$ and $A_2$ being
    countable implies $A_1 \cup A_2$ is countable. Now assume
    $\bigcup_{n=1}^m A_n$ be countable, then
    $\bigcup_{n=1}^m A_n \cup A_{n+1}$ is the union of countable sets,
    and thus itself countable.

(b) Induction cannot be used to show that $\bigcup_{n=1}^\infty A_n$ is
    countable, because induction only proves the statement for the union
    of any finite number of sets. There is no $m\in \mathbb{N}$ where
    $m = \infty$.

(c) Let $A_1, A_2, \dots$ all be countable, meaning
    $B_m = A_m \backslash \bigcup_{n=1}^{m-1} A_n$ is also countable.
    Therefore, we can enumerate $B_m$ so that
    $B_m = \{ b_{m,n} : n\in N \}$. Then, we may lay all the elements of
    $B_m$ along the $m^\text{th}$ row of a 2-dimensional array,
    something like

    ::: center
      ----------- ----------- ----------- -----
       $b_{1,1}$   $b_{1,2}$   $b_{1,3}$   ...
       $b_{2,1}$   $b_{2,2}$      ...     
       $b_{3,1}$      ...                 
           ⋮                              
      ----------- ----------- ----------- -----
    :::

    Now, for every $a \in \bigcup_{n=1}^\infty A_n$, if $a \in A_m$,
    then $a \in B_m$ if and only if $a\notin A_k$ for all $k<m$. Since
    the sequence of sets $A_1,A_2,\ldots$ is countable, the subset of
    them additionally containing $a$ is also countable. Therefore, if
    $A_m$ is the first qualifying set (i.e. $f(1) = A_m$, where
    $f:\mathbb{N}\to \{A_n : a\in A_n, n\in N\}$), then $a\in B_m$ and
    $a\notin B_k$ for all $k \neq m$. And so, every
    $a \in \bigcup_{n=1}^\infty A_n$ has exactly one position in the
    grid.

    Now we design a similar grid for the natural numbers, something like

    ::: center
      --- ----- ----- -----
       1    3     6    ...
       2    5    ...  
       4   ...        
       ⋮              
      --- ----- ----- -----
    :::

    We can see that each natural has exactly one position in the grid.
    So, we may define $f: \mathbb{N}\to \bigcup_{n=1}^\infty A_n$ where
    $f(n) = b_{i,j}$ where $i$ and $j$ denote the row and column that
    $n$ appears at the intersection of in the grid of natural numbers.

#### Exercise 1.5.4.

(a) For any interval $(a,b)$, we can define $f(x) = (2x - a - b)/(b-a)$
    which sets $(a,b) \sim (-1,1)$. Thus, since $(-1,1)\sim \mathbb{R}$,
    we have $(a,b) \sim \mathbb{R}$.

(b) There is probably a number of valid functions proving
    $(a,\infty) \sim \mathbb{R}$. One example is $f(x) = \ln(x-a)$. For
    any $y\in R$, we have $\ln(x) = y$ when $x = e^y +a$, so $f$ is
    onto. Also, $d/dx \ln(x-a) = 1/(x-a)$, which is positive for all
    $x > a$. Therefore, $f$ is 1-1.

(c) Let $f:(0,1) \to [0,1)$ be given by $f(x) = \inf(x,1)$. Since
    $0<x<1$, we have that $f(x)$ always a non-empty empty, and so it has
    an infimum, and moreover that infimum is in $[0,1)$. Less nicely, we
    may also define the inverse, $f^{-1}: [0,1) \to (0,1)$ where
    $f^{-1}(x)$ is lower bound of the open set for which $x$ is the
    infimum.

#### Exercise 1.5.5.

(a) For any set $A$, let $f: A\to A$ be given by $f(a) = a$. Then every
    element is mapped to by and only by itself. Therefore $A \sim A$ is
    always the case.

(b) $A\sim B$ means there exists a 1-1 correspondence $f: A\to B$. Let
    $g:B\to A$ be given by $g(b) = \{ a\in A : f(a) = b\}$. Since $f$ is
    1-1, whenever $f(a_1) = f(a_2) = b$, it must be that $a_1 = a_2$,
    and so $g(b)$ always maps to exactly one element in $A$. Also, if
    $g(b_1) = g(b_2)$, that means $f(a)=b_1$ and $f(a)=b_2$ for some
    $a\in A$, which is only possible if $b_1 = b_2$. Therefore $g$ is
    1-1. Additionally, for any $a \in A$, $g(b)=a$ for $b$ satisfying
    $f(a)=b$, which always exists since $f$ is onto. Therefore $g$ is a
    1-1 correspondence, and we may conclude that $A\sim B$ if and only
    if $B \sim A$.

(c) If $A\sim B$ and $B\sim C$ then there exists 1-1 onto functions
    $f: A\to B$, and $g: B\to C$. Let $h:A\to C$ be given by
    $h(a) = g(f(a))$ for any $a \in A$. Let $c$ be an arbitrary element
    in $C$, then there is exactly one $b\in B$ satisfying $g(b) = c$,
    and similarly exactly one $a\in A$ satisfying $f(a) = b$. And so,
    that makes exactly one $a\in A$ satisfying
    $h(a) = g(f(a)) = g(b) = c$. Therefore, $h$ is 1-1 and onto, and we
    may conclude that if $A\sim B$ and $B\sim C$ then $A\sim C$.

#### Exercise 1.5.6.

(a) Take the collection of disjoint open intervals
    $\{ (1,2), (2,3), (3,4) \ldots \}$, where the $n^{th}$ interval is
    given by $(n,n+1)$.

(b) *Solved with hint.* Assume for the sake of contradiction that there
    exists some uncountable collection of disjoint open intervals. Then,
    each interval has a real lower and upper bound, and since
    $\mathbb{Q}$ is dense in $\mathbb{R}$, we may find a unique rational
    number in each interval. That would mean $\mathbb{Q}$ is
    uncountable, which is not true, and thus a contradiction.

#### Exercise 1.5.7.

(a) Let $f:(0,1) \to S$ be given by $f(x) = (0,x)$.

(b) Let $f:S \to (0,1)$ be given by $f(x,y) = 0.x0y$. For example,
    $f(0.1,0.223) = 0.10223$. This function in 1-1 but not onto. For
    example, there is no element of $S$ that maps to $0.123$ under $f$
    because there is no 0.

#### Exercise 1.5.8.

*Solved with [hint](https://math.stackexchange.com/a/2876333/1027565)*.
Assume there were some $x\in B$ with $x>2$. Then, $\{x\}$ is a finite
subset of $B$ with sum greater than $2$, which would violate the
premise. Therefore, $B \subseteq (0,2]$. Furthermore, if $2\in B$, then
$B = \{2\}$, because otherwise there would be some other $x\in B$
violating $x+2 \leq 2$. If $2\notin B$, then it follows that
$B\subseteq (0,2)$. In that case, we may write
$B \subseteq \bigcup_{n=2}^\infty [\frac{2}{n},\frac{2}{n-1})$. To prove
it, first note that
$\bigcup_{n=2}^{m=2} [\frac{2}{n},\frac{2}{n-1}) = [1, 2) = [2/m, 2)$.
Then, assume $\bigcup_{n=2}^m [\frac{2}{n},\frac{2}{n-1}) = [2/m, 2)$,
and take the union of both sides with $[2/(m+1), 2m)$ to get
$\bigcup_{n=2}^{m+1} [\frac{2}{n},\frac{2}{n-1}) = [2/(m+1), 2)$. Now,
let $x$ be an arbitrary element of $b$, then there exists
$n\in \mathbb{N}$ so that $1/n < x/2$ and equivalently $2/n < x$. Then
certainly
$x\in [2/n, 2) = \bigcup_{k=2}^n [2/k, 2/(k-1)) \subseteq \bigcup_{k=2}^\infty [2/k, 2/(k-1))$.
Thus proving that
$B \subseteq \bigcup_{n=2}^\infty [\frac{2}{n},\frac{2}{n-1})$.
Importantly, for any $n\in N$, it must be the case that $[2/n, 2/(n+1))$
has at most $n$ elements. To see why, assume for the sake of
contradiction that the interval has finite $k>n$ elements. Then the sum
of those elements is surely at least $k\times 2/n$, as $2/n$ is the
smallest element. But $k\time 2/n > 2$ for $k>n$, which violates our
premise. If each interval cannot contain more than a finite number of
elements from $B$, it surely cannot contain an infinite amount. And so,
we have $B$ as a subset of an infinite sum of countable sets, which
makes it then either countable or finite.

#### Exercise 1.5.9.

(a) $(\sqrt{2})^3 - 2(\sqrt{2}) = 0$.

    $(\sqrt[3]{2})^3 - 2 = 0$.

    $(\sqrt{3})^4 + (\sqrt{2})^2 - 11 = 0$.

(b) The set of possible values for the $k^{th}$ integer coefficient of a
    polynomial may be enumerated as $\{n^k_0, n^k_1, \ldots \}$. Then,
    for a polynomial of degree $k$, let $P_{n,k}$ be the set of all
    coefficient orderings who's sum is $n$ when mapped to the natural
    numbers. So
    $P_{n,k} = \{(n^k, n^{k-1}, \ldots, n^0) : n^k + n^{k-1} + \dots + n^0 = n\}$.
    As a lenient bound, $1 < n^m \leq n$, and so $P_{n,k}$ is finite.
    Moreover, let $C_k$ be the set of all coefficient ordering of degree
    $k$. Then $C_k = \bigcup_{n=1}^\infty P_{n,k}$, which means $C_k$ is
    countable. Let $c^k_n$ be the $n^{th}$ coefficient ordering of a
    polynomial of degree $k$, and let $R(c^k_n)$ be the set of it's
    roots. We have that $R(c^k_n)$ is always finite, and thus
    $\bigcup_{n=1}^\infty R(c^k_n) = A_k$ is countable.

(c) Every algebraic number is in some $A_k$, and every element of any
    $A_k$ is and algebraic number, and so the set of all algebraic
    number is $\bigcup_{k=1}^\infty A_k$. Therefore, there is a
    countable number of algebraic numbers. As a result, there are an
    uncountable number of transcendental numbers, because otherwise
    $\mathbb{R}$ would be countable.

#### Exercise 1.5.10.

(a) We may write the interval $[0,1]$ as
    $\{0\} \cup \bigcup_{n=1}^\infty [1/n,1]$. Thus,
    $C = C \cap [0,1] = C \cap \left(\{0\} \cup \bigcup_{n=1}^\infty [1/n,1]\right) = (C\cap\{0\}) \cup \bigcup_{n=1}^\infty(C \cap [1/n,1])$.
    Surely $C\cap \{0\}$ is finite. Now assume for the sake of
    contradiction that $C\cap [a,1]$ is countable for all $a\in(0,1)$.
    For any $n$, it follows that $1/n \in (0,1)$ and thus
    $C\cap [1/n,1]$ is countable. That would make $C$ a union of
    countable sets, and thus countable. Since $C$ is supposed to be
    uncountable, it must be that there exists some $a\in(0,1)$ such that
    $C\cap[a,1]$ is uncountable.

(b) If $\alpha = 1$ then $C \cap [\alpha,1]=C\cap\{1\}$ is finite.
    Surely $\alpha > 0$, because by definition $\alpha \geq a$ for all
    $a\in A$, and $a\subseteq (0,1)$. Thus, if $\alpha < 1$, then
    $\alpha \in (0,1)$. In that case, assume for the sake of
    contradiction that $C\cap[\alpha,1]$ is uncountable. Then
    $\alpha=\max A$, and so for any $[a,1]$ where $a>\alpha$, it must be
    that $C\cap[a,1]$ is countable, because $a \notin A$. It then
    follows that $C\cap(\alpha,1]$ must be countable. If that is true,
    then $(C\cap \{\alpha\})\cup (C\cap(\alpha,1])$ must be countable,
    as it is a union of finite and countable sets. Moreover, that set is
    the same as $C\cap(\{\alpha\}\cup(\alpha,1]) = C \cap [\alpha, 1]$.
    But there lies a contradiction, as we supposed that
    $C \cap [\alpha, 1]$ was uncountable. Therefore,
    $C \cap [\alpha, 1]$ must be countable.

(c) *Counter-example.* Let $C\subseteq [0,1]$ be given by
    $\{1/n: n\in \mathbb{N}\}$. Written out, $C$ looks something like
    $\{\ldots, \frac{1}{4}, \frac{1}{3}, \frac{1}{2}, 1\}$. Now for any
    $a\in(0,1)$ there exists $n \in \mathbb{N}$ satisfying
    $n < \frac{1}{a}$, or rather $\frac{1}{n}>a$. As a result,
    $C \cap [a,1] \subseteq C \cap [\frac{1}{n},1]$. Note that
    $C\cap [\frac{1}{n},1] = \{\frac{1}{n}, \frac{1}{(n-1)}, \ldots, 1\}$
    which is finite with exactly $n$ elements. Therefore, $C\cap[a,1]$
    must also be finite for any $a\in(0,1)$.

#### Exercise 1.5.11 (Schroder--Bernstein Theorem).

(a) We may then define $h(a) = \begin{cases}
            f(a) & a\in A \\
            g^{-1}(a) & a\in A'
        \end{cases}$ for all $a\in A$. Since $h$ is a 1-1 map from $A$
    onto $B$, we may conclude that $A\sim B$.

(b) If $A_1 = \emptyset$, then $g$ is onto and so we have our 1-1
    correspondence. Assume for the sake of contradiction that there
    exists $m>n$ where $A_m\cap A_n$ is not empty. That means
    $(g\circ f)^m(x_0) = (g\circ f)^n(x_1)$ for some $x_0$ and $x_1$ in
    $X$. Since $g$ and $f$ are 1-1, we may iteratively take the inverse
    of each to get $(g\circ f)^{m-n}(x_0)=x_1$. Observing that the left
    side is of the form $g(y)=x_1$ for some $y \in Y$, it follows that
    $x_1 \in g(Y)$. Therefore, $x_1 \notin A_1$, but that would imply
    that $(g \circ f)^n(x_1)\notin A_n$, which is a contradiction. And
    so, we must admit that $A_m \cap A_n = \emptyset$ for all
    $m \neq n$. Moreover, assume for the sake of contradiction that
    $f(A_m)$ and $f(A_n)$ are not disjoint for some $m \neq n$, that is,
    they share some $y \in Y$. Let $x_0 \in A_m$ and $x_1 \in A_n$
    satisfy $f(x_0)=y=f(x_1)$. Since $f$ is onto, it must be that
    $x_0 = x_1$, which contradicts the fact that $A_m$ and $A_n$ are
    themselves disjoint. Therefore, $f(A_m) \cap f(A_n) = \emptyset$.

(c) $f(A) = \{f(x):x\in A\} = \{f(x):x\in A_1 \cup A_2 \cup \ldots \} = \{f(x):x\in A_1\} \cup \{f(x): x\in A_2\} \cup \ldots = f(A_1)\cup f(A_2) \cup \ldots = \bigcup_{n=1}^\infty f(A_n) = B$.
    And so, if $f$ did not map $A$ onto $B$, then there would have to
    exists some $b\in B$ for which no $a\in A$ satisfied $f(a)=b$. In
    that case, $b \notin f(A) = B$, which is contradiction. So, $f$ does
    map $A$ onto $B$.

(d) If $A'$ is empty, any function maps onto it. So let $A'$ be
    non-empty. An arbitrary element $a$ is in $A'$ if and only if
    $a\notin A$. That is, $a \notin \bigcup_{n=1}^\infty A_n$, and by De
    Morgan's law, $a\in \bigcap_{n=1}^\infty A_n^c$. Certainly then,
    $a \notin A_1$, which means $a\in g(Y)$, and so $g^{-1}(a) \in Y$.
    Note that, for $n>1$, we have $a \in A_n^c$ if and only if
    $a\notin g(f(A_{n-1}))$, that is, $g^{-1}(a)\notin f(A_{n-1})$.
    Therefore,
    $g^{-1}(a) \in \left( \bigcup_{n=1}^\infty f(A_n) \right)^c = B'$,
    and so $g$ maps $B'$ onto $A'$.

## Cantor's Theorem

#### Exercise 1.6.1.

From a previous exercise we found that $(0,1) \sim \mathbb{R}$, and also
that $\sim$ is a transitive operator. So, if $(0,1)$ is countable, then
$\mathbb{N}\sim (0,1)$, and so $\mathbb{N}\sim \mathbb{R}$, meaning
$\mathbb{R}$ is countable. Similarly, if $\mathbb{R}$ is countable then
$(0,1)$ is countable. Equivalently, $(0,1)$ is uncountable if and only
if $\mathbb{R}$ is uncountable.

#### Exercise 1.6.2.

(a) The first digit of $x$, given by $b_1$, equals $2$ if
    $a_{11} \neq 2$ and $3$ otherwise. Therefore, $b_1\neq a_{11}$, and
    as results, $x \neq f(1)$.

(b) The second decimal digit of $x$ is $b_2$, and $b_2\neq a_{22}$,
    which is the second digit of $f(2)$. Therefore, $x\neq f(2)$. In
    general, for any $n\in \mathbb{N}$, the $n^{th}$ digit of x, given
    by $b_n$, satisfies $b_n\neq a_{nn}$, and so $x\neq f(n)$.

(c) We have that, for any $n$, it follows that $x \neq f(n)$. So,
    assume, for the sake of contradiction, that $x$ has been enumerated,
    that is, $f(n) = x$ for some $n$. Then, it follows that
    $x \neq f(n) = x$. That is a contradiction, and so it must be that
    $x$ was never enumerated, and so no $n$ maps to $x$ under $f$.
    Therefore, we cannot construct a map from $\mathbb{N}$ onto $(0,1)$,
    proving that it is uncountable.

#### Exercise 1.6.3.

(a) We guarantee only that $x=0.b_1b_2\ldots$ is real number, which
    poses no contradiction with a supposed enumeration of the rationals.

(b) Assume that $f$ maps natural numbers to the terminating decimal
    expansion of every real number. Such an assumption is fine, because
    if $f$ really is 1-1 and onto, then it remains so for the real
    numbers. Then, the diagonally constructed element, $x$, will also be
    a terminating expansion, as it contains no $9$s. So, there is no
    possibility of $x$ being the non-terminating equivalent of an
    enumerated number. Therefore, $x$ remains distinct from every
    enumerated number.

#### Exercise 1.6.4.

Every sequence has a well defined $n^{th}$ digit, and so each sequence
is countable. Now, assume for the sake of contradiction that the set of
all binary sequences, $S$, is itself countable. Then, we must be able to
enumerate the sequences in a grid like so

::: center
  ---------- ---------- ---------- -----
   $a_{11}$   $a_{12}$   $a_{13}$   ...
   $a_{21}$   $a_{22}$     ...     
   $a_{31}$     ...                
      ⋮                            
  ---------- ---------- ---------- -----
:::

Now, define the sequence $x = (b_1,b_2,\ldots)$ where
$b_n = \begin{cases}
    0 & a_{nn}=1\\
    1 & a_{nn}=0
\end{cases}$. Then, for any $n\in \mathbb{N}$ the sequence at row $n$
must differ from $x$ in the $n^{th}$ digit. Moreover, $x$ is just a
sequence of $0$s and $1$s, and so it is a valid member of $S$.
Therefore, $x\in S$ has not been enumerated, and so $S$ must be
uncountable.

#### Exercise 1.6.5.

(a) $P(A)=\{\emptyset,\{a\},\{b\},\{c\},\{ab\},\{ac\},\{bc\},\{abc\}\}$

(b) For any $a\in A$ and $p\in P(A)$, either $a\in p$ or $a\notin p$.
    So, if $A$ has $n$ elements, then there are $2^n$ ways to construct
    a valid set for $p(A)$.

#### Exercise 1.6.6.

(a) Let $f(a)=\{a\}$, $f(b)=\{b\}$, $f(c)=\{c\}$. Or another:
    $f(a)=\{abc\},f(b)=\emptyset,f(c)=\{bc\}$.

(b) Let $g(1)=\{1\}$, $g(2)=\{2\}$, ...

(c) We cannot construct an onto mapping from $A$ to $P(A)$ because
    $P(A)$ has more elements.

#### Exercise 1.6.7.

(a) $B=\emptyset$. $B=\{b\}$

(b) $B=\emptyset$

#### Exercise 1.6.8.

(a) We assume that $f(a')=B$. If $a'\in B$, then $a'\in f(a')$, and thus
    $a'\notin B$.

(b) Conversely, if $a'\notin B$, then $a'\notin f(a')$, and thus
    $a'\in B$.

#### Exercise 1.6.9.

To show that $P(\mathbb{N})\sim\mathbb{R}$ it will suffice to show that
$P(\mathbb{N})\sim(0,1)$. For any $x\in (0,1)$, where the decimal
expansion of $x=.a_1a_2a_3\ldots$, let $nd$ (where $n$ and $d$ are
concatenated) be an element of $f(x)$ if and only if $a_n=d$. For
example $f(0.021)=\{10,22,31,40,50,\ldots\}$. To verify that
$f(x)\in P(\mathbb{N})$ for any $x$, note that $n\in \mathbb{N}$ and
$d\in \{0,1,\ldots,9\}$, and so $nd$ is just a natural number with a
digit added to the right. So, any element of $f(x)$ is natural number,
meaning $f(x)$ is a set of naturals and therefore in $P(\mathbb{N})$. To
verify that $f$ is 1-1, we take for granted that if two elements of
$(0,1)$ have the exact same decimal expansion, then they must be the
same number. Conversely, if they are different, then they differ at some
digit. Let $x=.a_1a_2\ldots$ differ from $y=b_1b_2\ldots$ at the
$n^{th}$ digit, so that $a_n\neq b_n$. Then, by the definition of $f$,
it follows that $a_n\in f(x)$ but $a_n \notin f(y)$ so $f(x)\neq f(y)$.
Therefore, $f$ is 1-1.

Now we construct a similar sort of function from $P(\mathbb{N})$. Let
$S\in P(\mathbb{N})$, and let $a_n$ be the $n^{th}$ decimal of $g(S)$.
Then define $a_n=\begin{cases}
    1 & n\in S \\
    0 & n\notin S
\end{cases}$, and in the special case that $S=\emptyset$, let
$g(S)=0.2$. For example, $g(\{1,4,5\})=.10011000\ldots$ and so on. To
verify that $g$ maps into $(0,1)$, note that $0<g(S) \leq 0.2$. To
verify that $g$ is 1-1, let there be some $n\in S_1$ where
$n \notin S_2$ so that $S_1\neq S_2$. Then the $n^{th}$ digit of
$g(S_1)=1$ while the corresponding digit in $g(S_2)=0$, thus they have a
differing decimal expansion, and so it follows that $g(S_1)\neq g(S_2)$.

By now we have a 1-1 function $f:(0,1)\to P(\mathbb{N})$ and a 1-1
function $g:P(\mathbb{N})\to (0,1)$. So, we may use the
Bernstein-Schroeder theorem to conclude that $P(\mathbb{N})\sim (0,1)$,
and as a result, $P(\mathbb{N})\sim\mathbb{R}$.

#### Exercise 1.6.10.

(a) We may represent a function $f: \{0,1\}\to \mathbb{N}$ as a pair of
    natural numbers $(n_0, n_1)$ where $f(0)=n_0$ and $f(1)=n_1$. Let
    $A_k$ be the set of all pairs where $n_0 + n_1 = k$. Every
    $(n_0, n_1)$ sums to exactly one number, and thus appears only in
    $A_{k}$ where $k=n_0 + n_1$. Moreover, each $A_k$ is finite, and so
    the union of all such $A_k$, that is, $\bigcup_{n=1}^\infty A_k$, is
    countable. Therefore, the set of all such $f$ is countable as well.

(b) A function $f$ from $\mathbb{N}$ to $\{0,1\}$ may be represented as
    an infinite sequence $(a_1,a_2,a_3,\ldots)$, where $a_n = f(n)$, and
    vice versa. That is, the value of the $n^{th}$ digit of the sequence
    indicates which element of the set, $\{0,1\}$, that $f(n)$ maps to.
    Any $f$ may be represented as a valid binary sequence, and every
    binary sequence is the representation of exactly one $f$. To see
    why, let $S_1=(a_{11}, a_{12}, \ldots\}$ and $S_2$ be different
    binary sequences. Then there is some $n$ such that the $n^{th}$
    element of We determined in Exercise 1.6.4 that the set of all such
    sequences is uncountable, and thus the set of all such $f$ is as
    well.

(c) *Solved with
    [hint](https://math.stackexchange.com/a/4858163/1027565)* To
    construct an uncountable antichain from $P(\mathbb{N})$, we first
    partition $\mathbb{N}$ into sets of two. Let $A_n = \{2n, 2n+1\}$,
    so for example, $A_1 = \{2,3\}, A_2 = \{4, 5\}, A_3 = \{6,7\}$ and
    so on. Consider a set constructed by selecting exactly one number
    from each $A_n$. We may represent such a set as the binary sequence
    $S=(a_1,a_2,a_3,\ldots)$, where $a_n = 0$ if the smaller element of
    the $n^{th}$ set is chosen, and $a_n=1$ if the larger is chosen.
    Then, any infinite binary sequence represents a valid sequence of
    choices, and any two binary sequences that differ must differ at
    some index. So, the two sets represented by different sequences each
    contain an element that the other does not, and thus are not subsets
    of eachother. Therefore, we may follow the uncountability arugment
    for inifinte binary sequences, and conclude that we have constructed
    an uncountable antichain of $P(\mathbb{N})$.
