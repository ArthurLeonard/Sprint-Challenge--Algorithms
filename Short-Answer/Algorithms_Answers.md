Add your answers to the Algorithms exercises here.
a) Running time: O(n)
   Explanation: n^2 + n^2 + n^2 + ... will reach n^3 after n iterations.

b) Running time: O(n^3)
   Explanation: There are three nested loops dependent on n. The last loop is dependent on k and will run exactly 9 times each time. This gives us 
   something less than 9n^3 since not all nested loops start at 0. But in big O notation we call this O(n^3).

c) Running time: O(n)
   Explanation: The recursion will end after n calls. Even though the running time is simply O(n) using recursion will make the function extremely slow.
   This function is a pretty horrendous implementation of a function that should simply return 2*n immediately.

Exercise II:

	We should use binary search in order to minimize the number of dropped eggs. We will start at floor n/2 and drop an egg. If it breaks we will 
  move down to floor n/4 and drop another egg. If it doesn't break we will move to floor 3n/4 and drop an egg. Each egg drop will eliminate exactly 
  half of the remaining floors as a possible candidate for floor _f_. As the interval we are looking at shrinks it will eventually reduce to one floor  
  and we will be done. The maximum number of steps required will be log base 2 n and this algorithm will run in O(log(n)) time.
