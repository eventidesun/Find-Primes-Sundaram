# Find Primes Using Sieve of Sundaram

A prime number finder using Sieve of Sundaram - an algorithm for finding all the primes less than a given number N.

This algorithm works on the observation that all given primes that are greater than 2 can be written in the form of 2i+1.
So this algorithm works to remove numbers that are of the form i + j + 2ij for all 1 ≤ i ≤ j such that i + j + 2ij ≤ n.
This method follows the operation of crossing out composite numbers that are multiples of the current prime number.

Steps:
1. To find all the primes less than or equal to N:
   n = (N - 2)/2
   This will later help us map back to the primes as 2i + 1

3. Then we mark a boolean array of size n + 1 mark all these as true.

4. For all the pairs (i, j) such that:
   1 ≤ i ≤ j i + j + 2ij ≤ n
   we would mark i + j + 2ij as false.

5. Finally the numbers i that remain true would give primes as 2i + 1.

These steps are shown through the code presented in FindPrimesSundaram.java.

Image of the output (finding all the primes below 100)
<img width="688" alt="Screenshot 2025-05-07 at 2 08 32 PM" src="https://github.com/user-attachments/assets/6deaca06-cc8c-420a-88bd-ef7946296bf0" />
