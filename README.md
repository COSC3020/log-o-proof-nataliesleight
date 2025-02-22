# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

Let $x$ be some arbitrary number such that $x ≠ 1$ and $x > 0$. Then by the Change of Base Formula for logarithms, 

$\log_2 n = \frac{\log_x n}{\log_x 2}$

and

$\log_5 n = \frac{\log_x n}{\log_x 5}$ .

Placing these values into the formal definition of $O$ as $f(n)$, they become 

$T(n) \in O(\log_{2} n) \iff \exists c, n_0: T(n) \leq c \cdot \frac{\log_x n}{\log_x 2} \forall n \geq n_0$

and 

$T(n) \in O(\log_{5} n) \iff \exists c, n_0: T(n) \leq c \cdot \frac{\log_x n}{\log_x 5} \forall n \geq n_0$

respectively. 

Because $\frac{1}{\log_x 2}$ and $\frac{1}{\log_x 5}$ are nonnegative constants, they can be paired with/absorbed into 
the $c$ constant that $f(n)$ is multiplifed by in the definition of $O$. Thus both of the equations become

$T(n) \in O(\log_{2} n) \iff \exists c, n_0: T(n) \leq c \cdot \log_x n \forall n \geq n_0$ .

and thus, $O(\log_{2} n) = O(\log_{5} n)$ .

This shows that the base of a logarithm does not affect its asymptotic complexity.

### Sources:

I used this link for the markdown fraction format: https://discourse.jupyter.org/t/how-to-display-a-fraction-in-a-markdown-cell/20657

I used this link for the change of base formula: https://www.cuemath.com/change-of-base-formula/ 

“I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.” - Natalie Sleight
