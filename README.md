# DSA-From-Scratch-Python

A Python Data Structures and Algorithms portfolio built from scratch[cite: 2, 4]. Features algorithms optimized from the bottom up, including dropping Fibonacci from $O(2^N)$ to strictly $O(N)$ time complexity[cite: 2, 4, 5], hash map frequency counters using immutable keys for $O(1)$ lookups[cite: 3, 7], and manually partitioned in-place divide-and-conquer sorting algorithms[cite: 2, 5].

## 📂 Repository Structure & Topics

### 01: Math & Logic
*   **Armstrong Numbers:** Mathematical digit extraction verifying if the sum of cubed digits equals the original number without using string conversions[cite: 6].
*   **Factor Optimization:** Finding all numerical factors by limiting the loop boundary strictly to $O(\sqrt{N})$[cite: 6].

### 02: Strings & Two Pointers
*   **Palindrome Checker:** Two-pointer logic (`si`, `ei`) optimized to halt exactly at the middle (`si <= ei`) to cut processing time in half[cite: 2, 9].
*   **Loop Control:** Clean loop termination utilizing boolean flag variables and Python's `while...else` blocks[cite: 2].

### 03: Hashing & Dictionaries
*   **Frequency Counters:** Implementations using immutable integer keys, optimized with the `.get()` method and `collections.Counter` for $O(1)$ lookups[cite: 3, 7].
*   **Data Retrieval:** Hashing logic to isolate the First Unique Element and identify the Majority Element appearing strictly more than $N/2$ times[cite: 3, 6].

### 04: Recursion
*   **Optimized Fibonacci ($O(N)$):** Bottom-up recursive calculation passing state forward (`a` and `b`) to achieve strictly $O(N)$ time complexity, bypassing the exponential $O(2^N)$ textbook bottleneck[cite: 2, 4, 5].
*   **Recursive Palindromes:** Passing boundaries inward recursively with explicit base cases (`si >= ei`) and returning boolean values up the recursive call stack[cite: 2, 5]. Time: $O(N)$, Space: $O(N)$[cite: 2, 5].

### 05: Sorting Algorithms
*   **Selection Sort:** Finding the absolute minimum value in the unsorted portion and swapping it directly to the front boundary[cite: 2, 5, 8]. Time: $O(N^2)$, Space: $O(1)$[cite: 2, 5, 8].
*   **Bubble Sort:** Implementations using both `while` and `for` loops, featuring the shrinking window (`n -= 1`) and early-exit boolean flag optimizations[cite: 2, 5]. Time: Best $O(N)$, Avg/Worst $O(N^2)$[cite: 5].
*   **Insertion Sort:** Traditional backward-scanning algorithm saving a key variable and manually shifting larger elements to the right until a gap opens[cite: 2, 5].
*   **Merge Sort:** Divide-and-conquer logic strictly guaranteeing $O(N \log N)$ time, featuring an independent `merge()` routine that appends to a brand new empty list[cite: 2, 5].
*   **Quick Sort:** In-place array modification utilizing both the Lomuto (small number boundary tracking) and Hoare (outside-in two pointers) partition schemes[cite: 2, 3, 5]. Time: Avg $O(N \log N)$, Worst $O(N^2)$[cite: 2, 4, 5]. Space: $O(1)$ auxiliary[cite: 5].

### 06: Applied Projects
*   **Custom Data Analyzer:** A standalone command-line application combining dictionary frequency counting, loop string checks, and a custom Quick Sort function to rank analytical data from scratch[cite: 3, 4, 5].

---

## 🔬 Standard Complexity Analysis Format
*Each algorithm in this repository includes a standard complexity defense header to document algorithmic scaling behavior[cite: 5]:*

```python
"""
Algorithm: Quick Sort (Hoare Partition Scheme)
Category: Sorting / Divide and Conquer

Description:
Selects a pivot and squeezes the array from both ends using two pointers (i, j). 
Swaps elements until pointers cross, then locks the pivot into its final position.

Complexity Analysis:
- Time Complexity (Average): O(N log N) - Recursively halves the array.
- Time Complexity (Worst): O(N^2) - Occurs if the pivot repeatedly fails to split the array evenly.
- Space Complexity: O(1) auxiliary space for in-place array modification (O(log N) recursive stack space).
"""
