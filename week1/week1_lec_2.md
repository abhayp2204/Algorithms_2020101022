## There are 4 steps to solving a problem
1. Understand the computational problem.
2. Find an efficient solution.
3. See if you can do better.
4. If not, prove that we cannot do better.
---

## Membership Query
Is this thing a member of a certain subset? Output 1 if yes, otherwise no.
- Is 2 a prime number?
  
  Let us frame this as a membership query. "Is 2 a member of the set of prime numbers?".

  This is a decision problem to illustrate how all decision problems can easily be framed as membership queries.

- Is a graph connected?

  "Does this graph belong to the set of connected graphs?"

- Sort a list of numbers.

  Given the input list [3,0,1,2] is [1,2,3,0] a member of the set [0,1,2,3]. The output is 0 since it is not.

  Hence, even a sorting problem can be framed as a membership query.
---

## Axioms of Computation
1. Machines are not omnipresent:
   It takes time to retrieve data.

2. Machines are not omniscient:
   Only finite information can be stored / recieved from finite volume.

3. Machines are not omnipotent:
   A finite length code only exerts a finite amount of control.
---

## Countability and Computability
- There are uncountably many computational problems.
- There are only countably many computational programs.
- Hence there must exist problems for which there are no programs.

Let us now prove the above statements.

## Part 1 : The number of computer programs are countable
Every computer program can be rewritten to work in C. Thus there is no loss in generality if we prove
this statement while considering only C programs.

A C program can be represented as a binary string. So we  must show that {0, 1}* is countable.
To do so, we map f: N -> {0, 1}* by listing the strings in short-lex order.  
    1 -> (0 length string)  
    2 -> 0  
    3 -> 1  
    4 -> 00  
    5 -> 01  
    6 -> 10  
    7 -> 11  
    8 -> 000  
    and so on...  
For any binary string, there exists a single natural number that maps to it.
Therefore we have a bijective mapping, proving that {0, 1}* is countable.
This proves our statement.  

## Part 2 : The number of computer problems are uncountable
The total number of problems is the cardinality of the power set of {0, 1}*.  
Therefore we neet to prove that this power set is uncountable.

We will use cantor's diagonalization method for doing so.  
Each member of the power set is a bitstring.  
Go through {0, 1}* and assign 1 to it if the bitstring we get is a part of the power set, and 0 otherwise.  
  
ex. {0,01,11} is a member of the power set.

    emptystring -> 0 (not present in {0,10,11})  
    0 -> 1           ()is present in {0,10,11})  
    1 -> 0  
    00 -> 0  
    01 -> 1  
    10 -> 0  
    11 -> 1  
    000 -> 0  
    001 -> 0  

