_PROBLEM STATEMENT_
N - no. of tasks given by user 
two processors for executing the N tasks simultaneously
User assigns a prefix of these tasks to the first processor and the remaining tasks to the second processor.

_INPUTS:_
t - test cases 
n - no. of tasks 
array[n] - having time for each tasks 

_ALGORITHM EXPLANATION_
1.Reading Input:

First, the program reads the number of test cases t.
For each test case, it reads the integer n (number of tasks) and then the array a of size n.

2.Total Work Calculation:

The total sum of the array a is calculated as totalSum.

3.Splitting Work Between Two Processors:

The work is distributed between two processors. One processor handles the "prefix" of the array, while the other handles the remaining "suffix."
The algorithm iterates over each possible split point in the array. For each split:
prefixSum holds the sum of the work for the first processor (tasks handled from the start of the array).
The second processor handles the remaining tasks, whose work is calculated as totalSum - prefixSum.
The maximum time between the two processors is calculated at each split, and the minimum of these maximum times is stored as the result.

4.Finding the Minimum Time:

At each split, the maximum time between the two processors is calculated using the max() function.
The goal is to minimize this maximum time, which is stored in minimumTime.
