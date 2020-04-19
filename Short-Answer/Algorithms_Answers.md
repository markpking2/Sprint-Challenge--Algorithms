#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a) O(n). The while condition is based off a being less than n^3, and a starts at 0. For each iteration, a is incremented by n^2. After n iterations the loop would end because n^2 x n = n^3, hence O(n).

b) O(n log(n)). The first for loop runs n times. The inner while loop runs log(n) times because j is doubled for each iteration from 1 to n. Since the second loop is nested, n \* log(n) = n log(n), hence O(n log(n)). The nested loops number of iterations grows slower than the input of n.

c) O(n). The recursion base case stops if bunnies is equal to 0. For each function call, it calls bunnyEars again with bunnies - 1 as input. The functions runtime it self is constant, but it will be called n times. Hence O(n).

## Exercise II

he input of my algorithm needs the buildings number of stories, or n, as its only input.

The first story to drop the egg would be the middle story, or n/2.

After each drop, we will change the range or low/high values of the possible floors to be tested next. We will also increment the f value by 1. It is initially 0.

If an egg was dropped on floor 50 and it broke, we would then know that any floor higher than 50 should also break the egg. If an egg didn't break, we would know it could be possible for the egg to also not break if we go to a higher floor. We will do this until the low floor becomes greater than the high floor. At that time the current floor would be the f value we were seeking.

The floor of each subsequent drop would depend if the previous egg dropped was broken or not.
If the egg was broken, the low floor value in our range would stay the same. The high value would be set to the current floor - 1. The next floor to be tested would be the middle of that range, or (low + high)/2.
If the egg was not broken, the low value would become current floor + 1. The high value would remain the same. The next
floor to be tested would be the middle of that range, or (low + high)/2

The runtime of this algorithm would be O(log n). Each subsequent iteration, the amount of floors to check is cut in half.
