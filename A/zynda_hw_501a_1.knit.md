---
title: "Econ 501A HW 1"
author: "David Zynda"
date: "August 27, 2018"
output: pdf_document
---



## Problem 1.1

_Suppose $X=\{a,b,c\}$ and $u(a) = 1$, $u(b) = 1$, and $u(c) = 2$ For each $B \subset X$, compute $C_u(b)$_



There are seven such subsets $B$ of $X$:

(1) $B = \{a\}$: $C_u(B) = a$
(2) $B = \{b\}$: $C_u(B) = b$
(3) $B = \{c\}$: $C_u(B) = c$
(4) $B = \{a,b\}$: $C_u(B) = \{a,b\}$
(5) $B = \{a,c\}$: $C_u(B) = c$
(6) $B = \{b,c\}$: $C_u(B) = c$
(7) $B = \{a,b,c\}$: $C_u(B) = c$


Technically, $\emptyset$ could also be a subset. But, following the prescription of the notes, we write:

$$C_u:\mathcal{P}(X) \setminus \emptyset \rightarrow  \mathcal{P}(X) \setminus \emptyset$$
So, I exclude it. 


## Problem 1.2 

_(a) Prove that $u^*(B)$ is increasing in $B$. That is, prove that if $B \in B'$, the $u^*(B) \le u^*(B')$. In words, increasing the set of feasible alternatives never hurts the individual and sometimes helps the individual._

$$B \subset B' \implies \sup u(x)_{x \in B} \le \sup u(x)_{x \in B'} \implies u^*(B) \le u^*(B')$$

Let $B \subset B'$. Then $B'$ contains at least one more element than $B$. If $B \subseteq B'$, then it may contain the same elements. If $B'$ has more elements than $B$, then these elements contained in $B'$ will either be larger or smaller than the maximum element of $B$ which is also found, by definition, in $B'$. If the elements in $B'$ not in $B$ are smaller than the maximum element in $B$ then $\sup u(x)_{x \in B} = \sup u(x)_{x \in B'} \implies u^*(B) = u^*(B')$.

If there is an element in $B'$ that is not in $B$ which is greater than all elements in $B$, then, $\sup u(x)_{x \in B} < \sup u(x)_{x \in B'} \implies u^*(B) < u^*(B')$.

An increasing function is one such that each subsequent value is greater than or equal to the previous value (Precisely: $\forall x,y \in \mathbb{R}: x< y \implies f(x) < f(y)$. Hence, in both cases above, $u^*(B)$ is an increasing function. 




_(b) Prove that if $y \in B$ but $y \notin C_u(B)$ then $u^*(B) = u^*(B \setminus y)$, where $B \setminus y$ denotes the set consisting of all elements of B expect $y$. In words, unchosen alternatives do not affect welfare._

Proof by contraposition: $u^*(B) \ne u^*(B \setminus y) \implies y \in C_u(B)$

Let $y \in B$ and assume $u^*(B) \ne u^*(B \setminus y)$. Then, the $\sup u(x)_{x \in B} \ne \sup u(x)_{x \in B \setminus y}$. Hence, $y$ must be the maximum element in the set of $B$. Therefore, $y \in C_u(B)$. 







## Problem 1.3

_Suppose $X \supset \{a,b,c\}$. (a) Of course, $C_u(\{a,n\})$ is a subset of $\{a,b\}$. How many subsets of $\{a,b\}$ are there? How many values might $C_u(\{a,b\})$ take and what are they?_

There are four subsets:

(1) $\emptyset$
(2) $\{a\}$
(3) $\{b\}$
(4) $\{a,b\}$

$C_u(\{a,b\})$ could take 3 values. It excludes the empty set, so we exlude case (1) from all further analysis in this part. If $a > b$ then it will take the value $a$ unles case (3) where it will only have $b$. 

If $b > a$ then it will take the value of $b$ unless case (2) in which it will take value of $a$. 

If $a = b$, then it will take value $a$ for case (1), value $b$ for case (2) and the set $\{a,b\}$ for case (3). 



_(b) Suppose that $C_u(\{a,b\}) = b$. What can we conclude about $u(a)$ versus $u(b)$? Suppose further that $C_u(\{b,c\} = c$. What can we conclude about $C_u(\{a,c\})$?_

First, we can conclude that $u(a) < u(b)$. 

Second, we can conlude that $u(a) < u(c)$ by transitivity.


_(c) Suppose $a \in B$ but $a \notin C_u(B)$ What can we conclude about $C_u(B \setminus a)$ as compared to $C_u(B)$_

We can conclude that $C_u(B \setminus a) = C_u(B)$.







## Problem 1.4


_Let $f: \mathbb{R} \rightarrow \mathbb{R}$ be a strictly increasing function. Define a function $v: X \rightarrow \mathbb{R}$ so that $v(x) = f(u^*(x))$. Then, $C_u(B) = C_v(B)$._

_(a) Prove the above proposition_

Let $x, y \in B$ and $u^*(B \setminus x) < u^*(x)$ such that $u^*(y) < u^*(x)$ and by definition $u^*(x), u^*(y) \in \mathbb{R}$.

Define $f: \mathbb{R} \rightarrow \mathbb{R}$ to be a strictly increasing function such that:

$$\forall a,b \in \mathbb{R}: a < b \implies f(a) < f(b).$$
Hence, $f(u^*(y)) < f(u^*(x))$. Define $C_v(B) = \arg \max f(u^*(z))_{z \in B}$ Now, $C_v(B) = x$.

By definition $C_u(B) = \arg \max u^*(z)_{z \in B} = x$. 

Hence, $C_u(B) = C_v(B)$. 



_(b) What if instead $f$ is a weakly increasing function? State and prove an alternative proposition in this case._ 

Let $f: \mathbb{R} \rightarrow \mathbb{R}$ be an increasing function. Define a function $v: X \rightarrow \mathbb{R}$ so that $v(x) = f(u^*(x))$. Then, $C_u(B) \ge C_v(B)$.



Let $x, y \in B$ and $u^*(B \setminus x) < u^*(x)$ such that $u^*(y) < u^*(x)$ and by definition $u^*(x), u^*(y) \in \mathbb{R}$.

Define $f: \mathbb{R} \rightarrow \mathbb{R}$ to be an increasing function such that:

$$\forall a,b \in \mathbb{R}: a < b \implies f(a) \le f(b).$$


Hence, $f(u^*(y)) \le f(u^*(x))$. Define $C_v(B) = \arg \max f(u^*(z))_{z \in B}$ Now, $C_v(B) = x' \in B \le x \in B$.
By definition $C_u(B) = \arg \max u^*(z)_{z \in B} = x$. 

Hence, $C_u(B) \ge C_v(B)$. 






## Problem 2.1 

_Recall the previous problem where $X = \{a,b,c\}$ and $u(a) = 1$, $u(b) = 1$, and $u(c) = 2$. Write down the preference derived from this $u$. That is for every pair $x,y \in X$, indicate whether $x \succeq y$ or $x \nsucceq y$_

(1) $\{a,b\}$: $a \succeq b$ and $b \succeq a$
(2) $\{a,c\}$: $c \succeq a$ and $a \nsucceq c$
(3) $\{b,c\}$: $b \nsucceq c$ and $c \succeq b$

Also note that: $a \succeq a$, $b \succeq b$ and $c \succeq c$. 





## Problem 2.2

_For each of the following four preferences, answer the follwing two questions: Is the preference complete? Is it transitive? Prove your answers_

_In parts (a), (b), and (c), let $X = \mathbb{R}^2_+$ so an element $x \in X$ is a vector: $x = (x_1, x_2)$ where $x_1$ and $x_2$ are nonnegative real numbers._

Note: I will use vector $z = (z_1, z_2)$ as I prove transitivity. 

__(a) $x \succeq y \iff x_1 + x_2 \ge y_1 + y_2$__

The preference is complete. 

$$(1) \ x_1 + x_2 < y_1 + y_2$$
$$(2) \ x_1 + x_2 = y_1 + y_2$$
$$(3) \ x_1 + x_2 > y_1 + y_2$$
Which imply:

$$(1) \ y \succ x$$
$$(2) \ x \sim y$$
$$(3) \ x \succ y$$

The preference is transitive. Let $y_1 + y_2 \ge z_1 + z_2$ Then, $x \succeq y \succeq z \iff x_1 + x_2 \ge y_1 + y_2 \ge z_1 + z_2$ and so $x_1 + x_2 \ge z_1 + z_2 \iff x \succeq z$

__(b) $x \succeq y \iff x_1 \ge y_1$ and $x_2 \ge y_2$__


This is not complete. Let $x_1 < y_1$ and $x_2 \ge y_2$. This cannot be represented by any preference relation. 

It is transitive. Suppose 
$$y_1 \ge z_1$$  
$$y_2 \ge z_2$$

Then, we have:

$$x_1 \ge y_1 \ge z_1 \implies x_1 \ge z_1$$
$$x_2 \ge y_2 \ge z_2 \implies x_2 \ge z_2 \implies x \succeq z$$

__(c) $x \succeq y \iff$ either $x_1 > y_1$ or both $x_1 = y_1$ and $x_2 \ge y_2$.__

This is complete. 



$$x_1 = y_1 \ and \ x_2 < y_2 \implies y \succ x$$
$$x_1 > y_1 \implies x \succ y$$
$$x_1 = y_1 \ and \ x_2 = y_2 \implies x \sim y$$


This is transitive. 

$$x_1 > y_1$$
$$y_1 > z_1 \implies x_1 > z_1 \implies x \succeq z$$

Or note the following:

$$x_1 = y_1 = z_1$$
$$x_2 \ge y_2 \ and \ y_2 \ge z_2 \implies x_2 \ge z_2$$
$$\implies x \succeq z$$


__(d) Now let $X = \{1,2,3\}$. There are three individuals, each with their own complete and transitive preferences: For Ann, $1 \succ_a 2 \succ_a 3$. For Bob, $2 \succ_b 3 \succ_b 1$. For Carol, $3 \succ_c 1 \succ_c 2$. Define a new preference $\succeq$ such that $x \succeq y$ if and only if at least two of the three individuals prefer $y$ to $x$. Is this new preference transitive and complete?__


This preference is complete. 

$$1 \succeq 2$$
$$3 \succeq 1$$
$$2 \succeq 3$$
So, all bases are covered. Now, this is not transitive because:

$$1 \succeq 2 \succeq 3 \succeq 1$$
Which is circular. 














