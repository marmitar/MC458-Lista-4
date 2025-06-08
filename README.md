# Analysis of Algorithms I (MC458) - Test 4

- [Questions](./Enunciado.pdf)
- [Answers](./Resposta.pdf)
- [Turn in](./Entrega.pdf)

## Selection Algorithms

---

### Question 1

Describe a **comparison-based** algorithm with running time $O(n)$ that solves the following problem:

> **Input.**
> - An array $V$ of $n \ge 1$ **distinct integers**;
> - An integer $i$ with $0 < i \le n$;
> - An integer $\ell$ with $0 < \ell \le n$.
>
> **Output.**
> The $\ell$ elements of $V$ that are **closest** to the $i$-th smallest element of $V$.

Justify that your algorithm is correct and that its running time is indeed $O(n)$.

*Observation.* You may invoke algorithms covered in class simply by name-no pseudocode is required.

Examples:

- If $V = (39, 4, 2, 16, 3, 28)$, $i = 1$, $\ell = 2$, the output is $\{2, 3\}$.
- If $V = (39, 4, 2, 16, 3, 28)$, $i = 2$, $\ell = 2$, the output may be $\{2, 3\}$ **or** $\{4, 3\}$.
- If $V = (39, 4, 2, 16, 3, 28)$, $i = 4$, $\ell = 4$, the output is $\{4, 16, 3, 28\}$.
- If $V = (39, 4, 2, 16, 3, 28)$, $i = 5$, $\ell = 2$, the output is $\{39, 28\}$.

---

### Question 2

After studying the **BFPRT** algorithm, **Xitoró** claims it would be more efficient to use
$\lfloor n/3 \rfloor$ groups of **three** elements each, instead of
$\lfloor n/5 \rfloor$ groups of **five** elements each.
**Chorãozinho** disagrees.

Who is right? Carefully justify your answer.

---

### Question 3

An electronics factory produces resistors on a single line.
Each production cycle yields:

- a batch of $n$ **yellow** resistors $\lbrace A_1, A_2, \dots, A_n \rbrace$;
- a batch of $n$ **green** resistors  $\lbrace V_1, V_2, \dots, V_n \rbrace$.

Within a batch, no two resistors of the **same color** share the same capacity.
However, for every yellow resistor $A_i$ with capacity $c(A_i)$ there is **exactly one** green resistor $V_j$ with the **same** capacity, produced in the **same cycle**: $c(A_i) = c(V_j)$.
All $2n$ resistors leave the machine **mixed**, so the matching pairs must be found before packaging.

A single **tester** is available with two connectors-one for a yellow resistor and one for a green resistor.
When activated, the tester reports whether:

1. the capacities are **equal**;
2. the yellow resistor has **higher** capacity; or
3. the yellow resistor has **lower** capacity.

The manager (Mr. G. Moore) has been promoted and poses a challenge to employees **Xitoró** and **Chorãozinho**:

- **Xitoró** must design an algorithm that finds all $n$ equal-capacity pairs using **at most $O(n)$** tester invocations.
- **Chorãozinho** must prove that Xitoró's task is **impossible**.

Both employees offer you lucrative consulting deals-each wants your help to win and become the other's boss.
You must **choose one offer** and will be paid only if you succeed.

Select **one** of the proposals and justify your choice by presenting a **detailed, complete solution** that ensures you earn your fee.
