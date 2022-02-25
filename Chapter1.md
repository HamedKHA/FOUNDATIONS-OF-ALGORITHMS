# FOUNDATIONS-OF-ALGORITHMS
FOUNDATIONS OF ALGORITHMS solutions

These solutions are personal ones and not official solutions.


# Section 1.1

### 1. 

    max(A,n): // A is an array. n is the size of the array.
      maximum = A[1]
      for i=2 to n:
         if A[i] > maximum:
           maximum = A[i]
      return maximum   
     
### 2.

One can use an efficient sorting algorithm with time complexity of `nlg n` like mergesort and then traverse m first elements of the array and print them out.

### 40.

#### a
It is better to first look at what we want to prove. For this purpose first open `f(n)+g(n)∈ O(max(f(n),g(n)))` according to the definition of big O:

      ∃c>0 ∃N ∀n>N: f(n)+g(n) ≤ c * max(f(n),g(n))  (1)
      
Now, for proving this we have:


      f and g are asymptotically positive functions
      ------------------- So
      ∃N ∀n>N: f(n)>0
      ∃N'∀n>N': g(n)>0
      ------------------- So
      ∃N"=max(N,N') ∀n>N": f(n)>0, g(n)>0
      ------------------- By above statement in mind
      f(n) ≤ max(f(n),g(n))
      g(n) ≤ max(f(n),g(n))
      ------------------- Adding two sides of inequalities
      f(n) + g(n) ≤ max(f(n),g(n)) + max(f(n),g(n)) = 2 * max(f(n),g(n))
      ------------------- So
      f(n) + g(n) ≤ 2 * max(f(n),g(n))
      ------------------- At the end
      By considering N"=max(N,N') and c=2 we have statement (1)

#### b

For proving we have to have following statement:

    ∃c>0 ∃N ∀n>N: f²(n) ≥ c * f(n)  (1)

So, 

      f is asymptotically positive function
      ------------------- So
      ∃N ∀n>N: f(n)>0 (2)
      ------------------- We know following statement always is true
      f(n)≥f(n)
      ------------------- According to statement (2) we can do
      ∃N ∀n>N: f(n) * f(n)≥f(n) => f²(n) ≥ 1 * f(n)
      ------------------- So
      By considering c=1 and N in statement (2), we have proved statement (1).

#### c

    
    


