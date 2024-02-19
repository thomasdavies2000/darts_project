The holy grail in the game of Darts is to throw a 9 dart leg (watch this video) - reaching the score of 501 with the last dart being a double or bullseye, in only 9 darts. The most common way of achieving this is by throwing 60 (treble 20), 60, 60, 60, 60, 60, 60, 57 (treble 19), 24 (double 12). However, whilst watching the Darts World Championships one year I heard the commentators mention there are 3944 different ways of throwing a 9 dart leg. After hearing this, I started to think about how this number could be calculated. I initally thought it would be quite simple, but the more I thought about it the harder I realised it was going to be. After a lot of thinking, my initital solution was to implement a depth-first search using search trees.


As you can probably deduce, this solution is incredibly inefficient. For a few months, I stopped thinking about this problem, accepting that my solution was probably the best I could do. Then, in one of my modules at Uni I was introduced to dynamic programming, and more specifically the Change Making algorithm. This algorithm takes a value and selection of coins (with infinite supply) as inputs, and returns the minimum number of coins required to make that value. For example, if you supplied this algorithm with a value of 22p and a selection of coins of 10p, 5p, 1p, the algorithm would return 4, as 4 coins are required to make 22p: 10 + 10 + 1 + 1.

You can probably start to see how this algorithm can be modified to solve the Darts problem. The difference is that it needs to return an array of all of the possible ways it can make the required score in the lowest number of darts. I found a similar modification on Stack Overflow which I was able to use for the darts problem. Once this array is obtained, all of the permutations of these scores need to be counted too.

I'm not saying the code I wrote was particularly inventive, as it mainly was modifying code others had written to similar problems. However, I thought I'd include this project on my website anyway as I found it very interesting and satisfying to apply dynamic programming to a real life problem that I had not known how to solve before. It also reinforced my knowledge of dynamic programming, and how it can be used to apply very efficient solutions.
