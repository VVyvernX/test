# CE427 – Design and Analysis of Algorithms  
## Section II – Detailed 10 Marks Theory Notes (DEC-2 Exam)

---

# 4. Divide and Conquer

## Q1. Explain Divide and Conquer technique with examples.

### Definition
Divide and Conquer is an algorithm design paradigm that solves a problem by recursively breaking it into smaller subproblems, solving each subproblem independently, and then combining their solutions.

---

### Steps Involved
1. **Divide**  
   Split the main problem into smaller subproblems of the same type.

2. **Conquer**  
   Solve each subproblem recursively. If small enough, solve directly (base case).

3. **Combine**  
   Merge results of subproblems to form final solution.

---

### General Recurrence Relation
T(n) = aT(n/b) + f(n)  

Where:
- a = number of subproblems  
- n/b = size of each subproblem  
- f(n) = cost of dividing and combining  

---

### Example 1: Merge Sort
- Divide array into two halves  
- Recursively sort both halves  
- Merge sorted halves  

**Time Complexity:** O(n log n)

---

### Example 2: Binary Search
- Divide search space into half  
- Compare middle element  
- Recursively search left/right  

**Time Complexity:** O(log n)

---

### Example 3: Quick Sort
- Choose pivot  
- Partition array  
- Recursively sort partitions  

---

### Advantages
- Efficient for large problems  
- Reduces time complexity  
- Parallelizable  

---

### Disadvantages
- Recursive overhead  
- Stack memory usage  

---

### Conclusion
Divide and Conquer is widely used in efficient algorithms like sorting, searching, and matrix operations.

---

# 5. Greedy Algorithms

## Q2. Explain Greedy Algorithm with characteristics and applications.

### Definition
Greedy Algorithm is an approach that builds a solution step-by-step by always choosing the locally optimal choice at each stage.

---

### Key Characteristics
1. **Greedy Choice Property**  
   Local optimal choice leads to global optimum.

2. **Optimal Substructure**  
   Problem can be broken into subproblems.

3. **Irrevocable Decisions**  
   Choices are not reconsidered.

---

### General Approach
- Initialize solution  
- Select best available option  
- Add to solution  
- Repeat until complete  

---

### Applications

#### 1. Activity Selection Problem
- Select maximum number of non-overlapping activities  
- Sort by finish time  

---

#### 2. Minimum Spanning Tree

**Kruskal’s Algorithm**
- Sort edges  
- Pick smallest edge without cycle  

**Prim’s Algorithm**
- Start from node  
- Add minimum weight edge  

---

#### 3. Dijkstra’s Shortest Path
- Find shortest path from source  
- Works with non-negative weights  

---

#### 4. Fractional Knapsack
- Select items with highest value/weight ratio  
- Allows fractions  

---

#### 5. Job Scheduling
- Maximize profit with deadlines  

---

### Greedy vs Dynamic Programming

| Feature | Greedy | DP |
|--------|--------|----|
| Decision | Local | Global |
| Complexity | Low | High |
| Optimal | Not always | Always |

---

### Advantages
- Simple and fast  
- Efficient for certain problems  

---

### Limitations
- Not always optimal  
- Requires specific conditions  

---

### Conclusion
Greedy algorithms are efficient but only work when greedy property holds.

---

# 6. Dynamic Programming

## Q3. Explain Dynamic Programming with principles and applications.

### Definition
Dynamic Programming (DP) is a method used to solve complex problems by breaking them into overlapping subproblems and storing their results to avoid recomputation.

---

### Key Principles

#### 1. Optimal Substructure
Optimal solution can be constructed from optimal solutions of subproblems.

#### 2. Overlapping Subproblems
Same subproblems occur multiple times.

---

### Approaches

#### Top-Down (Memoization)
- Recursive  
- Store results in memory  

#### Bottom-Up (Tabulation)
- Iterative  
- Build solution from base cases  

---

### Applications

#### 1. Fibonacci Series
Avoid repeated calculations using DP.

---

#### 2. 0/1 Knapsack Problem
- Maximize value within capacity  
- Use DP table  

---

#### 3. Matrix Chain Multiplication
- Minimize multiplication cost  

---

#### 4. Shortest Path
- Bellman-Ford  
- Floyd-Warshall  

---

#### 5. Coin Change Problem
- Minimum number of coins  

---

#### 6. Assembly Line Scheduling
- Optimize production time  

---

### Advantages
- Avoids recomputation  
- Guarantees optimal solution  

---

### Disadvantages
- High memory usage  
- Complex to implement  

---

### Conclusion
Dynamic Programming is powerful for optimization problems where greedy fails.

---

# 7. NP-Completeness

## Q4. Explain NP-Completeness with examples.

### Definition
NP-Completeness is a concept in computational complexity that classifies problems based on their difficulty and solvability.

---

### Complexity Classes

#### 1. Class P
- Problems solvable in polynomial time  
- Example: Sorting  

---

#### 2. Class NP
- Solutions verifiable in polynomial time  

---

#### 3. NP-Complete Problems
- Hardest problems in NP  
- If one solved, all NP solved  

---

#### 4. NP-Hard Problems
- At least as hard as NP  
- May not be in NP  

---

### Polynomial Reduction
- Convert one problem into another  
- Used to prove NP-completeness  

---

### Important Problems

#### 1. Travelling Salesman Problem (TSP)
- Find shortest route visiting all cities  

---

#### 2. Hamiltonian Cycle
- Visit each vertex exactly once  

---

### Approximation Algorithms
- Provide near-optimal solutions  
- Used when exact solution is infeasible  

---

### Importance
- Helps identify computational limits  
- Guides algorithm design  

---

### Conclusion
NP-Completeness defines the boundary between efficiently solvable and intractable problems.

---

# References

1. Thomas H. Cormen, *Introduction to Algorithms (CLRS)*  
2. Ellis Horowitz, *Computer Algorithms*  
3. Gilles Brassard, *Fundamentals of Algorithms*  
4. Aho, Hopcroft, Ullman, *Design and Analysis of Algorithms*  

---
