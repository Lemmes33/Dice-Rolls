# Dice-Rolls
Problem Statement

You have rolled a dice several times, and you remember the results of N rolls, which are stored in an array A. However, there are F rolls whose results you have forgotten. The arithmetic mean of all the roll results (the sum of all the roll results divided by the number of rolls) equals M. Your task is to find the possible results of the missing rolls.

Function Signature

def solution(A, F, M)

Input Parameters

A: an array of length N, containing the remembered roll results
F: an integer, representing the number of forgotten rolls
M: an integer, representing the arithmetic mean of all the roll results
Output

an array containing possible results of the missed rolls, with F integers from 1 to 6 (valid dice rolls)
if such an array does not exist, return [0]
Examples

A = [3, 2, 4, 3], F = 2, M = 4 => return [6, 6]
A = [1, 5, 6], F = 4, M = 3 => return [2, 1, 2, 4] or [6, 1, 1, 1] (among others)
A = [1, 2, 3, 4], F = 4, M = 6 => return [0]
A = [6, 1], F = 1, M = 1 => return [0]
Assumptions

N and F are integers within the range [1..100,000]
each element of array A is an integer within the range [1..6]
M is an integer within the range [1..6]
Algorithm

The solution involves calculating the total sum of the remembered rolls and the target sum required to achieve the mean M. Then, we can try to find a combination of F integers from 1 to 6 that adds up to the remaining sum. If such a combination exists, we return it; otherwise, we return [0].