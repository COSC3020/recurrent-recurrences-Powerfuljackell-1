# Recurrent Recurrences

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice." 

Used prior work from: https://github.com/COSC3020/recurrent-recurrences-Powerfuljackell

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$
$T(n) = T(\frac{n}{13}) + 5 $

$= T(T(\frac{n}{13 \cdot 13}) + 5) + 5)$

$= T(T(T(\frac{n}{13 \cdot 13 \cdot 13}) + 5) + 5) + 5$

$...$

$= T(\frac{n}{13^i}) + 5i$

for $i = \log n$

$T(\frac{n}{13n}) + 5logn$

$T(\frac{1}{13}) + 5logn$

$T(1) + logn \in \Theta(logn)$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

$T(n) = 13T(\frac{n}{13}) + 5 $

$= 13T(13T(\frac{n}{13 \cdot 13}) + 5) + 5)$

$= 13T(13T(13T(\frac{n}{13 \cdot 13 \cdot 13}) + 5) + 5) + 5$

$...$

$= 13^i \cdot T(\frac{n}{13^i}) + 5i$

for $i = \log n$

$13n \cdot T(\frac{n}{13n}) + 5logn$

$13n \cdot T(\frac{1}{13}) + 5logn$

$n \cdot T(1) + logn \in \Theta(n)$

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

$T(n) = 13T(\frac{n}{13}) + 2n $

$= 13 \cdot 13T(\frac{n}{13 \cdot 13}) + 2n + 2n$

$= 13 \cdot 13 \cdot 13T(\frac{n}{13 \cdot 13 \cdot 13}) + 2n + 2n + 2n$
