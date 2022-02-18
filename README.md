# Project-Euler-Solutions
My repository of working through solutions of ProjectEuler.com questions.

### Multiples of 3 or 5
**If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.
Find the sum of all the multiples of 3 or 5 below 1000.** 
<br />

Upon initial inspection, I wonder if the hint of the sum being multiples of 23 clues into a solution that utilizes this fact. Though I'm skeptical of it and might just see if there is a way through that method later.<br />

Consider the multiples of 3 or 5 as they tend to 1000. The numbers at where they coincide will be where they are multiples of the two, or every 3 × 5 = 15 units. Thus we can probably take out the multiples of 15 from one summation of either 3 or 5.<br />

Consider the summation of multiples of 3 and 5 s.t.,<br />
S_1 = 3 + 6 + 9 + 12 + 15 + ... + 999<br />
S_2 = 5 + 10 + 15 + 20 + ... + 995<br />
and<br />
S_3 = 15 + 30 + ... + 990<br />

Since it's a finite series, we can do this:<br />
S_1 + S_2 - S_3<br />
Doing some manipulation:<br />
S_1 = 3(1 + 2 + 3 + ... + 333)<br />
S_2 = 5(1 + 2 + ... + 199)<br />
S_3 = 15(1 + 2 + ... + 66)<br />

