# CMPS 2200 Assignment 2

**Name:**_____Maddie Bonanno____________________

In this assignment we'll work on applying the methods we've learned to analyze recurrences, and also see their behavior
in practice. As with previous
assignments, some of of your answers will go in `main.py`.. You
should feel free to edit this file with your answers; for handwritten
work please scan your work and submit a PDF titled `assignment-02.pdf`
and push to your github repository.


1. Derive asymptotic upper bounds of work for each recurrence below.
  * $W(n)=2W(n/3)+1$
.  

given (n/3) --> log3 n /// 2W = 2^i nodes  // +1 = constant
= 2^log3n --> **= O(n^(2(log3)))**

.  
  * $W(n)=5W(n/4)+n$
.  
given n/4 --> log 4 n /// 5(W) = 5^i nodes // + n
= 5^nlog4n --> **= O(n^(log4n))**
.  
.  
.  
  * $W(n)=7W(n/7)+n$
.  
.  n/7 --> log 7 n // 7(W) = 7^i nodes // +n
= 7^nlog7n --> **= O(n log7 n)**
.  
.  
.  
  * $W(n)=9W(n/3)+n^2$
.  
.  
  n/3 --> log 3 n // 9(W) = 9^i nodes // +n^2
= 9^n2log3n --> **= O(n^2 log3 n)**
.  
.  
  * $W(n)=8W(n/2)+n^3$
.  
.  
    n/2 --> log 2 n // 8(W) = 8^i nodes // +n^3
= 8^log 2 n^4 --> **= O(n^3 log2 n)**
.  
.  
  * $W(n)=49W(n/25)+n^{3/2}\log n$
.  
.  
.  n/25 --> log 25 n // 49(W) = 49^i nodes // + n^3/2 log n
= reduce: log 5 n // 7^i nodes // +n^3/2 log n
= 7^(logn^2 n^3/2) --> **= O(n^(logn n^3/2))**
.  
.  
  * $W(n)=W(n-1)+2$
.  
 n-1 --> n // +2 = constant
  **=O(n)**
.  
.  
.  
  * $W(n)= W(n-1)+n^c$, with $c\geq 1$
.  
.  n-1 --> n // + n^c >= n^1
= n * n^c --> **= O(n^c+1)**
.  
    
.  
  * $W(n)=W(\sqrt{n})+1$

 sqrt n --> n^1/2 (aka log)// +1
 **= O(log(1/2)n)**


2. Suppose that for a given task you are choosing between the following three algorithms:

  * Algorithm $\mathcal{A}$ solves problems by dividing them into
      five subproblems of half the size, recursively solving each
      subproblem, and then combining the solutions in linear time.
    
  * Algorithm $\mathcal{B}$ solves problems of size $n$ by
      recursively solving two subproblems of size $n-1$ and then
      combining the solutions in constant time.
    
  * Algorithm $\mathcal{C}$ solves problems of size $n$ by dividing
      them into nine subproblems of size $n/3$, recursively solving
      each subproblem, and then combining the solutions in $O(n^2)$
      time.

    What are the asymptotic running times of each of these algorithms?
    Which algorithm would you choose?


A --> 5 subproblems (5W) of 1/2 size (n/2) and combinining in linear (O(n)) time
A = 5W(n/2) + n --> 5^(log2n) --> **= O(n^log2 5)**

B --> size n problems(n) with two n-1 subproblems (2W) (n-1) and combining in constant (O(1))
B = 2W(n-1) + 1 --> 2^n leaves (size n problems) --> **= O(n^2)**

C --> size n problems (n) dividing into 9 subproblems (9W) of size n/3 (n/3), recursively solving each subproblem and combining in (O(n^2))
C = 9W(n/3) + n^2 --> 9^(log3 n^2) with size n problems accounted for --> **= O(n^(log3 n^2))**

Comparing these algorithms, algorithm A would be chosen, as it will run the fastest (log in the exponent vs constants in exponents)


3. Now that you have some practice solving recurrences, let's work on
  implementing some algorithms. In lecture we discussed a divide and
  conquer algorithm for integer multiplication. This algorithm takes
  as input two $n$-bit strings $x = \langle x_L, x_R\rangle$ and
  $y=\langle y_L, y_R\rangle$ and computes the product $xy$ by using
  the fact that $xy = 2^{n/2}x_Ly_L + 2^{n/2}(x_Ly_R+x_Ry_L) +
  x_Ry_R.$ Use the
  stub functions in `main.py` to implement Karatsaba-Ofman algorithm algorithm for integer
  multiplication: a divide and conquer algorithm that runs in
  subquadratic time. Then test the empirical running times across a
  variety of inputs to test whether your code scales in the manner
  described by the asymptotic runtime. Please refer to Recitation 3 for some basic implementations, and Eqs (7) and (8) in the slides https://github.com/allan-tulane/cmps2200-slides/blob/main/module-02-recurrences/recurrences-integer-multiplication.ipynb
 
 


