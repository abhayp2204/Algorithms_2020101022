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

## Axioms of Computation
1. Machines are not omnipresent:
   It takes time to retrieve data.

2. Machines are not omniscient:
   Only finite information can be stored / recieved from finite volume.

3. Machines are not omnipotent:
   A finite length code only exerts a finite amount of control.
---

## Prove that there are computational problems that computers cannot solve
- There are uncountably many computational problems.
- There are only countably many computational programs.
- Hence there must exist problems for which there are no programs.

