# Binary and ternary search

Algorithm description: 
* Binary search: https://en.wikipedia.org/wiki/Binary_search_algorithm

* Ternary search: https://en.wikipedia.org/wiki/Ternary_search

---

# Problem 1: Leftmost occurence

You are given sorted sequence of integer numbers $a_1$, $a_2$, . . . , $a_n$ ($a_1$ ≤ $a_2$ ≤ · · · ≤ $a_n$). Also you are given
$m$ numbers $b_1$, $b_2$, . . . , $b_m$. For each $b_j$ print such first (smallest) index $i$ in the sequence $a$ that $a_i$ = $b_j$.

Print -1 if such index doesn’t exist.

Prefer to submit your solution with PyPy if you use Python.

**Input**

The first line contains $n$ $(1 ≤ n ≤ 2 · 10^5)$.

The second line contains integers $a_1, a_2, . . . , a_n$ $(−10^9 ≤ a_i ≤ 10^9)$. The given integers are sorted by non-decreasing.

The third line contains $m$ $(1 ≤ m ≤ 2*10^5)$.

The fourth line contains integers $b_1, b_2, . . . , b_m$ $(−109 ≤ b_j ≤ 109)$.

**Output**

Print the sequence of $m$ integers, the $j-th$ of them should be equal to such smallest $i$ $(1 ≤ i ≤ n)$ that
$a_i = b_j$ . If there is no such $i$, print -1.

---

**Example**

standard input
```
8
3 4 4 4 6 7 10 10
11
100 8 7 4 3 4 3 10 6 -100 2
```
standard output
```
-1 -1 6 2 1 2 1 7 5 -1 -1
```

---

# Problem 2: Rightmost Occurrences

You are given sorted sequence of integer numbers $a_1, a_2, . . . , a_n$ $(a_1 ≤ a_2 ≤ · · · ≤ a_n)$. Also you are given
$m$ numbers $b_1, b_2, . . . , b_m$. For each $b_j$ print such last (greatest) index $i$ in the sequence $a$ that $a_i = b_j$.

Print -1 if such index doesn’t exist.

**Input**

The first line contains $n$ $(1 ≤ n ≤ 2*10^5
)$.

The second line contains integers $a_1, a_2, . . . , a_n$ $(−10^9 ≤ a_i ≤ 10^9
)$. 

The given integers are sorted by non-decreasing.

The third line contains $m$ $(1 ≤ m ≤ 2*10^5
)$.

The fourth line contains integers $b_1, b_2, . . . , b_m$ $(−10^9 ≤ b_j ≤ 10^9
)$.

**Output**

Print the sequence of $m$ integers, the $j-th$ of them should be equal to such greatest $i$ $(1 ≤ i ≤ n)$ that $a_i = b_j$. If there is no such $i$, print -1.

---

**Example**

standard input
```
8
3 4 4 4 6 7 10 10
11
100 8 7 4 3 4 3 10 6 -100 2
```
standard output
```
-1 -1 6 4 1 4 1 8 5 -1 -1
```

---

# Problem 3: Difference with Closest

You are given two arrays of integer numbers: 𝑎 and 𝑏. For each element of 𝑏 find minimal difference with some element of 𝑎. I.e. for each 𝑏𝑗 find the minimal value of |𝑏𝑗−𝑎𝑖| over all possible indices 𝑖.

**Input**

The first line contains integer 𝑛 $(1≤ 𝑛 ≤10^5)$ — the length of 𝑎. The second line contains $𝑎_1,𝑎_2,…,𝑎_𝑛$ — the elements of 𝑎. They are integer numbers between $−10^9$ and $10^9$, inclusive.

The third line contains integer 𝑚 $(1≤ 𝑚 ≤10^5)$ — the length of 𝑏. The fourth line contains $𝑏_1,𝑏_2,…,𝑏_𝑚$ — the elements of 𝑏. They are integer numbers between $−10^9$ and $10^9$, inclusive.

**Output**

Print 𝑚 numbers, where the 𝑗-th number is the minimal value of |𝑏𝑗−𝑎𝑖|.

---

**Example:**

input
```
6
6 2 6 3 1 10
4
1 7 20 8
```
output
```
0
1
10
2
```

---

# Problem 4: Threads

You are given 𝑛 spools of threads. The 1-st has $𝑎_1$ meters of a thread, the 2-nd has $𝑎_2$ meters of a thread, ..., the last (the 𝑛-th) has $𝑎_𝑛$ meters of a thread.

Beautiful embroidery requires 𝑘 pieces of thread of equal length. It is required to find out what is the greatest length of each of the 𝑘 equal pieces, if:

* Threads can not be tied (can not be join), they can only be cut;

* Each of 𝑘 pieces has a length equal to an integer number of meters.

**Input**

The first line contains two integers 𝑛 and 𝑘 (1 ≤ 𝑛, 𝑘 ≤ 1000). The second line contains 𝑛 integers $𝑎_1, 𝑎_2,…,𝑎_𝑛$ (1 ≤ 𝑎𝑖 ≤ 100000, for each 𝑖 = 1…𝑛).

**Output**

Print the only number — the greatest integer 𝑠 that it is possible to cut 𝑘 equal pieces of a thread, each of length 𝑠. If it is impossible to find such integer positive 𝑠, print 0.

---

**Examples:**

input
```
2 5
2 4
```
output
```
1
```
---

input
```
5 9
5 2 5 7 20
```
output
```
3
```
---
input
```
5 12
10 20 22 9 40
```
output
```
7
```
---

# Problem 5: Square Room and Tables

There are 𝑛 tables. Each table is a rectangle 𝑎×𝑏. You can't rotate tables, i.e. 𝑎 is a horizontal size of a table, and 𝑏 is a vertical size of a table.

For given 𝑛, 𝑎 and 𝑏 find minimal size 𝑘 of square room 𝑘×𝑘, which can fit all 𝑛 tables.

**Input**

The first line contains 𝑡 (1 ≤ 𝑡 ≤ 100) — number of test cases in the input. Then 𝑡 test cases follow.

Each of the following 𝑡 lines describe one test case. A line contains three integers 𝑛, 𝑎 and 𝑏 (1 ≤ 𝑛, 𝑎, 𝑏 ≤ 106).

**Output**

Print 𝑡 numbers — required values 𝑘 for each test case.

---

**Example:**

input
```
3
7 1 2
25 1 1
97 7 3
```
output
```
4
5
49
```

---

# Problem 6: Hamburgers

Polycarpus loves hamburgers very much. He especially adores the hamburgers he makes with his own hands. Polycarpus thinks that there are only three decent ingredients to make hamburgers from: a bread, sausage and cheese. He writes down the recipe of his favorite "Le Hamburger de Polycarpus" as a string of letters 'B' (bread), 'S' (sausage) and 'C' (cheese). The ingredients in the recipe go from bottom to top, for example, recipe "BSCBS" represents the hamburger where the ingredients go from bottom to top as bread, sausage, cheese, bread and sausage again.

Polycarpus has $𝑛_𝑏$ pieces of bread, $𝑛_𝑠$ pieces of sausage and $𝑛_𝑐$ pieces of cheese in the kitchen. Besides, the shop nearby has all three ingredients, the prices are $𝑝_𝑏$ rubles for a piece of bread, $𝑝_𝑠$ for a piece of sausage and $𝑝_𝑐$ for a piece of cheese.

Polycarpus has 𝑟 rubles and he is ready to shop on them. What maximum number of hamburgers can he cook? You can assume that Polycarpus cannot break or slice any of the pieces of bread, sausage or cheese. Besides, the shop has an unlimited number of pieces of each ingredient.

**Input**

The first line of the input contains a non-empty string that describes the recipe of "Le Hamburger de Polycarpus". The length of the string doesn't exceed 100, the string contains only letters 'B' (uppercase English B), 'S' (uppercase English S) and 'C' (uppercase English C).

The second line contains three integers $𝑛_𝑏$, $𝑛_𝑠$, $𝑛_𝑐$ $(1 ≤ 𝑛_𝑏,𝑛_𝑠,𝑛_𝑐≤100)$ — the number of the pieces of bread, sausage and cheese on Polycarpus' kitchen. The third line contains three integers $p_𝑏$, $p_𝑠$, $p_𝑐$ $(1≤𝑝𝑏,𝑝𝑠,𝑝𝑐≤100)$ — the price of one piece of bread, sausage and cheese in the shop. Finally, the fourth line contains integer 𝑟 $(1≤𝑟≤10^{12})$ — the number of rubles Polycarpus has.

**Output**

Print the maximum number of hamburgers Polycarpus can make. If he can't make any hamburger, print 0.

---

**Examples:**

input
```
BBBSSC
6 4 1
1 2 3
4
```
output
```
2
```
---
input
```
BBC
1 10 1
1 10 1
21
```
output
```
7
```
---
input
```
BSC
1 1 1
1 1 3
1000000000000
```
output
```
200000000001
```

---

# Problem 7:CPUs

There are 𝑛 jobs. A worker (single CPU) can process the 𝑖-th job in $𝑡_𝑖$ seconds. You have 𝑘 CPUs in total. You can assign only consecutive jobs to a single CPU. I.e. all assigned jobs to a single CPU should form some interval of jobs.

For example, if 𝑛=5 and 𝑘=2 then one of the possible assignments is:

* the first CPU processes jobs 1 and 2;

* the second CPU processes jobs 3, 4 and 5.

CPUs can work simultaneously. Some CPUs can be left unused. What is the minimal time you all 𝑛 jobs will be finished? I.e. find such minimal 𝑇 that all jobs can be finished after 𝑇 seconds.

For example, if $𝑛=6,𝑎=[3,1,7,2,3,3],𝑘=3$ you can assign:

* the jobs 1 and 2 to the 1-st CPU (in total it will work $𝑡_1+𝑡_2=3+1=4$ seconds);
* the single job 3 to the 2-nd CPU (in total it will work $𝑡_3$=7 seconds);
* the jobs 4, 5 and 6 to the 3-rd CPU (in total it will work $𝑡_4+𝑡_5=𝑡_6=2+3+3=8$ seconds).

It means that after 8 seconds all jobs will be done.

**Input**

The first line contains two integers 𝑛 and 𝑘 $(1≤𝑛,𝑘≤100)$. The second line contains 𝑛 integers $𝑡_1,𝑡_2,…,𝑡_𝑛$ $(1≤𝑡_𝑖≤10^7)$.

**Output**

Print minimal 𝑇 that all jobs can be finished after 𝑇 seconds. Some CPUs can be left unused.

---

Examples

input
```
5 3
3 5 8 2 7
```
output
```
9
```

---

input
```
4 5
7 1 3 6
```
output
```
7
```
---

input
```
2 2
1 2
```
output
```
2
```
---

input
```
3 1
4 8 7
```
output
```
19
```
