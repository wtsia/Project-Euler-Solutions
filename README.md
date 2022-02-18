# Project-Euler-Solutions
My repository of working through solutions of ProjectEuler.com questions.

## Multiples of 3 or 5
**If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.
Find the sum of all the multiples of 3 or 5 below 1000.** 

Upon initial inspection, I wonder if the hint of the sum being multiples of 23 clues into a solution that utilizes this fact. Though I'm skeptical of it and might just see if there is a way through that method later.

Consider the multiples of 3 or 5 as they tend to 1000. The numbers at where they coincide will be where they are multiples of the two, or every 3 × 5 = 15 units. Thus we can probably take out the multiples of 15 from one summation of either 3 or 5.

Consider the summation of multiples of 3 and 5 s.t., <br>
S_1 = 3 + 6 + 9 + 12 + 15 + ... + 999 <br>
S_2 = 5 + 10 + 15 + 20 + ... + 995 <br>
and <br>
S_3 = 15 + 30 + ... + 990

Since it's a finite series, we can do this: <br>
S_1 + S_2 - S_3 <br>
Doing some manipulation: <br>
S_1 = 3(1 + 2 + 3 + ... + 333) <br>
S_2 = 5(1 + 2 + ... + 199) <br>
S_3 = 15(1 + 2 + ... + 66)

"Quick side proof, S_a = 1 + 2 + 3 + ... + (n - 1) + n + = n + (n - 1) + (n - 2)... + 2 + 1, 2S_a = (n + 1) + (n + 1)  + ... + (n + 1) = n(n + 1), S_a = n(n + 1)/2"

S_1 = 3(n(n+1)/2); n = 333 <br>
S_2 = 5(n(n+1)/2); n = 199 <br>
S_3 = 15(n(n+1)/2); n = 66

Then the answer to the sum of all integers under 1000 will be given by S_1 + S_2 - S_3 = 3(333(334)/2) + 5(199(200)/2) - 15(66(67/2)) = 166,833 + 99,500 - 33,165 = 233,168
