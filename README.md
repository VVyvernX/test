# Numerical Methods – Final Exam Revision Cheatsheet

Quick revision for **Chapters 1, 5, 6, 7**

---

# Chapter 1 – Graph Theory

## Graph
A **graph** represents relationships between objects.

G = (V, E)

- V → set of vertices (nodes)
- E → set of edges (connections)

---

## Path
A **path** is a sequence of vertices connected by edges.

Example:

A → B → C → D

Length = number of edges.

Types:
- Simple Path (no repeated vertices)
- Cycle / Closed Path (start = end)

---

## Reachability
Vertex **u is reachable from v** if a path exists from **v → u**.

Used for **network connectivity analysis**.

---

## Connected Graph
A graph is **connected** if every pair of vertices has a path.

Types:
- Connected graph
- Disconnected graph

---

## Matrix Representation of Graph

### Adjacency Matrix

|   | A | B | C |
|---|---|---|---|
| A | 0 | 1 | 1 |
| B | 1 | 0 | 0 |
| C | 1 | 0 | 0 |

1 → edge exists  
0 → no edge

---

### Incidence Matrix
Shows relationship between **vertices and edges**.

---

## Tree
A **tree** is a connected graph with **no cycles**.

Properties:
- n vertices → n − 1 edges
- Only one path between vertices

---

## Applications of Graph Theory
- Computer networks
- Social networks
- Routing algorithms
- Circuit design
- Transportation systems

---

# Chapter 5 – Roots of Nonlinear Equations

Goal: Solve

f(x) = 0

---

## Bisection Method

Condition:

f(a)f(b) < 0

Formula:

c = (a + b) / 2

Steps:
1. Choose interval [a, b]
2. Find midpoint
3. Check sign change
4. Repeat until root found

Advantages:
- Simple
- Guaranteed convergence

Disadvantage:
- Slow

---

## False Position Method

Formula:

x = (a f(b) − b f(a)) / (f(b) − f(a))

Uses **linear interpolation**.

---

## Secant Method

Formula:

x(n+1) = x(n) − f(x(n))(x(n) − x(n−1)) / (f(x(n)) − f(x(n−1)))

Features:
- No derivative required
- Faster than bisection

---

## Newton–Raphson Method

Formula:

x(n+1) = x(n) − f(x(n)) / f'(x(n))

Steps:
1. Choose initial guess
2. Compute derivative
3. Apply formula
4. Repeat until convergence

Advantages:
- Very fast

Disadvantage:
- Requires derivative

---

## Successive Approximation (Fixed Point Method)

Rewrite equation:

x = g(x)

Iteration:

x(n+1) = g(x(n))

Condition for convergence:

|g'(x)| < 1

---

# Chapter 6 – Interpolation & Extrapolation

## Interpolation
Finding unknown values **within known data points**.

Example:
Value between x = 2 and x = 3.

---

## Extrapolation
Finding value **outside given data range**.

---

## Newton Forward Interpolation

Used when value is **near beginning of table**.

Formula:

y = y₀ + pΔy₀ + p(p−1)/2! Δ²y₀ + p(p−1)(p−2)/3! Δ³y₀ + ...

Where:

p = (x − x₀) / h

---

## Newton Backward Interpolation

Used when value is **near end of table**.

p = (x − xₙ) / h

Uses **backward difference table**.

---

## Central Difference Methods

Used when value is **near middle of table**.

Includes:
- Stirling
- Bessel
- Laplace-Everett

---

### Stirling Formula
Used when **p ≈ 0** (center values).

---

### Bessel Formula
Used when **p ≈ 1/2**.

---

### Laplace–Everett Formula
Uses **even differences only**.

---

## Lagrange Interpolation

Used when **data spacing is unequal**.

General formula:

P(x) = Σ yi ∏ (x − xj)/(xi − xj)

---

## Newton Divided Difference

Used for **unequal intervals**.

Formula:

P(x) = f(x₀)
+ (x − x₀)f[x₀,x₁]
+ (x − x₀)(x − x₁)f[x₀,x₁,x₂]

---

## Error in Interpolation

E(x) = ((x−x₀)(x−x₁)...(x−xₙ) / (n+1)!) f⁽ⁿ⁺¹⁾(ξ)

Error depends on:
- number of points
- derivative order
- distance of x

---

# Chapter 7 – System of Linear Equations

General form:

a₁x + b₁y + c₁z = d₁  
a₂x + b₂y + c₂z = d₂  

---

## Gaussian Elimination

Steps:
1. Write augmented matrix [A | B]
2. Convert to **upper triangular matrix**
3. Use **back substitution**

---

### Partial Pivoting
Swap rows so **largest pivot element** becomes diagonal.

Advantages:
- Improves accuracy
- Avoids numerical instability

---

## Gauss–Jordan Method

Transforms matrix to **identity matrix**.

Final form:

|1 0 0 | x|  
|0 1 0 | y|  
|0 0 1 | z|

Solution obtained directly.

---

## Gauss–Seidel Method

Iterative method.

Equations rearranged:

x = (b₁ − a₁₂y − a₁₃z) / a₁₁  
y = (b₂ − a₂₁x − a₂₃z) / a₂₂  

Steps:
1. Assume initial values
2. Compute new values
3. Repeat until convergence

---

# Ultra Quick Revision Map

Graph Theory:
Graph → Path → Reachability → Connectedness → Matrix → Tree

Root Finding:
Bisection → False Position → Secant → Newton-Raphson → Successive Approximation

Interpolation:
Forward → Backward → Stirling → Bessel → Laplace-Everett → Lagrange → Divided Difference

Linear Systems:
Gaussian Elimination → Gauss-Jordan → Gauss-Seidel
