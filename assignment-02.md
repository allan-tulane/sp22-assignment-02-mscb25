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

we have n/3, which im pretty sure will end up being a constant such as O(1)

.  
  * $W(n)=5W(n/4)+n$
.  
.  n/4 and also an n --> n/4 goes to a constant so this leaves O(n)
.  
.  
.  
  * $W(n)=7W(n/7)+n$
.  
.  n/7 to constant plus n becomes I think O(n)
.  
.  
.  
  * $W(n)=9W(n/3)+n^2$
.  
.  
.  n/3 to constant plus an n^2 which means bare minimum O(n^2)
.  
.  
  * $W(n)=8W(n/2)+n^3$
.  
.  
.  n/2 to constant plus an n^3 which means bare minimum O(n^3)
.  
.  
  * $W(n)=49W(n/25)+n^{3/2}\log n$
.  
.  
.  it's n/25 to a constant + n^3/2 over logn... which makes me think it's an n exponential over a log which has ???
.  
.  
  * $W(n)=W(n-1)+2$
.  
.  i feel like this really just means O(1)
.  
.  
.  
  * $W(n)= W(n-1)+n^c$, with $c\geq 1$
.  
.  
.  
.  n^c is a big value so prob O(n^k)
.  
  * $W(n)=W(\sqrt{n})+1$

i think exponential to a c so O(n^k)


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


I feel like the third one is definitely gonna take a hot minute with values in O(n^2) time


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
 
 


