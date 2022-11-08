# KDM

THE GAME
What is Number Mind?
The game Number Mind is a variant of the well-known game Master Mind.
Instead of colored balls, you must guess a secret sequence of digits. After
each guess you’re only told in how many places you’ve guessed the correct digit.
So, if the sequence was 1234 and you guessed 2036, you’d be told that you have
one correct digit; however, you would NOT be told that you also have another
digit in the wrong place.

THE EXAMPLE
For instance, given the following guesses for a 5-digit secret sequence,
90342 ; 2 correct
70794 ; 0 correct
39458 ; 2 correct
34109 ; 1 correct
51545 ; 2 correct
12531 ; 1 correct
The correct sequence is 39542 and it is unique.

THE TASK
1. Write a program that plays the Number Mind game against itself.
2. Generate a random sequence of n digits (the secret code)
3. Generate a proposed solution based on the previous proposals
and feedback using SAT encoding. Make sure to generate new
sequences;
4. Computes the feedback (x correct) on the generated proposal and
if there are n correct guesses exit, if not generate new code.

THE LOGIC
P ( i, j ) = Digit j is in position i
The position i can be from 1 to n, meaning i = {1, … ,n}
The digit j can be from 0 to 9, because it has to be a single digit.
Meaning that j = {0, … ,9}
Propositional variables => 10 * n
Possible codes =>10ⁿ
Having the same digit multiple times is possible, with replacement.

THE RULES
We have to specify that at each place there must be exactly one
digit!
→ At least one digit in every position
→ At most one digit in every position
