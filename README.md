# Data_Structures_and_Algorithms
All DSA techniques will be uploaded here 

Here’s a list of golden rules for Data Structures and Algorithms (DSA) that can help you decide which data structure or algorithm to use in common situations:

### 1. **Sorted Array → Use Binary Search**
   - **Why**: Binary search is optimal for searching in a sorted array with a time complexity of \(O(\log n)\).
   - **Use Case**: Find an element in a sorted array.

### 2. **Unsorted Collection → Use Linear Search**
   - **Why**: In unsorted collections, binary search is not applicable, so linear search with a time complexity of \(O(n)\) is your best option.
   - **Use Case**: Search for an element in an unsorted array or list.

### 3. **Dynamic Data with Frequent Inserts/Deletes → Use Linked List**
   - **Why**: Linked lists allow for efficient insertion and deletion operations with a time complexity of \(O(1)\) if you have a reference to the node.
   - **Use Case**: Implement dynamic data storage like stacks and queues.

### 4. **Need Fast Access by Index → Use Array**
   - **Why**: Arrays provide constant-time \(O(1)\) access to elements if you know the index.
   - **Use Case**: When you need to access elements frequently by index.

### 5. **Frequent Searches and Inserts → Use Hash Table**
   - **Why**: Hash tables provide average-case \(O(1)\) time complexity for search, insert, and delete operations.
   - **Use Case**: When fast access, insertions, and deletions are needed, like in caches or dictionaries.

### 6. **Sorted Data with Fast Insertions and Deletions → Use Binary Search Tree (BST)**
   - **Why**: BSTs allow you to maintain sorted data and perform search, insert, and delete operations with an average time complexity of \(O(\log n)\).
   - **Use Case**: Maintaining dynamic sorted data with balanced tree structures like AVL or Red-Black trees for efficient operations.

### 7. **Optimal Search in Graphs → Use BFS/DFS**
   - **Why**: Breadth-First Search (BFS) and Depth-First Search (DFS) are optimal for traversing or searching through graph structures.
   - **Use Case**: Use BFS for shortest path in unweighted graphs; DFS for exploring deep paths or connected components.

### 8. **Finding Shortest Path in Weighted Graph → Use Dijkstra’s Algorithm**
   - **Why**: Dijkstra's algorithm is optimal for finding the shortest path in a graph with non-negative weights with time complexity \(O(E + V \log V)\) (using a priority queue).
   - **Use Case**: Navigation systems, network routing.

### 9. **Need Constant-Time Min/Max → Use Heap**
   - **Why**: Heaps (priority queues) allow you to access the minimum or maximum element in constant time \(O(1)\) and perform insertions/deletions in \(O(\log n)\).
   - **Use Case**: Efficiently manage dynamic priority-based tasks, like scheduling or event handling.

### 10. **Recursion with Overlapping Subproblems → Use Dynamic Programming**
   - **Why**: Dynamic programming solves overlapping subproblems by storing intermediate results to avoid recomputation.
   - **Use Case**: Problems like Fibonacci series, Knapsack, or Longest Common Subsequence.

### 11. **Need to Find K-th Largest/Smallest → Use Quickselect/Heaps**
   - **Why**: Quickselect has an average time complexity of \(O(n)\), while a min/max heap can provide efficient \(O(k \log k)\) performance.
   - **Use Case**: Finding the median or any \(k\)-th order statistic.

### 12. **Fixed Size Sliding Window Problem → Use Deque (Double-ended Queue)**
   - **Why**: Deques allow efficient insertion and removal from both ends in constant time, making it useful for sliding window techniques.
   - **Use Case**: Maximum or minimum in a sliding window.

### 13. **Graph with Negative Weights → Use Bellman-Ford Algorithm**
   - **Why**: Bellman-Ford can handle graphs with negative weights, unlike Dijkstra’s algorithm.
   - **Use Case**: Finding shortest paths in graphs where some edges have negative weights.

### 14. **Cycle Detection in Graphs → Use DFS or Union-Find**
   - **Why**: DFS can detect cycles in directed or undirected graphs, and the Union-Find (disjoint-set) can detect cycles in undirected graphs.
   - **Use Case**: Detecting cycles in network connections or dependencies.

### 15. **Backtracking Problem → Use Recursive DFS**
   - **Why**: Backtracking problems, like solving a maze, Sudoku, or generating permutations, can be efficiently solved using recursive DFS.
   - **Use Case**: Constraint satisfaction problems (CSP), combinatorics.

### 16. **Need Real-Time Median Calculation → Use Two Heaps**
   - **Why**: Using a min-heap and a max-heap allows real-time median calculation in \(O(\log n)\).
   - **Use Case**: Real-time data analysis, streaming applications.

### 17. **Longest Increasing Subsequence → Use Binary Search with DP**
   - **Why**: A combination of binary search and dynamic programming yields \(O(n \log n)\) time complexity for the Longest Increasing Subsequence (LIS) problem.
   - **Use Case**: LIS problem in sequence-based optimizations.

### 18. **Heavy Use of Range Queries → Use Segment Trees/Fenwick Trees**
   - **Why**: Segment trees and Fenwick trees (Binary Indexed Trees) provide efficient updates and queries on ranges with \(O(\log n)\) time complexity.
   - **Use Case**: Range sum queries, minimum/maximum range queries.

### 19. **Sorting Large Data Efficiently → Use Merge Sort or Quick Sort**
   - **Why**: Merge Sort guarantees \(O(n \log n)\) time complexity, while Quick Sort is \(O(n \log n)\) on average and can be faster with good pivot selection.
   - **Use Case**: Sorting data sets efficiently, especially when space or time is a concern.

### 20. **Graph Traversal for Unweighted Shortest Path → BFS**
   - **Why**: BFS traverses levels in the shortest way in unweighted graphs, ensuring the shortest path in terms of edges.
   - **Use Case**: Finding the shortest path in an unweighted graph, social networks.

These "golden rules" can help you quickly determine which algorithm or data structure to apply based on the problem at hand. Let me know if you need clarification on any specific topic!


### 1. Bubble Sort:
Bubble Sort repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. This process is repeated until the list is sorted.

Example: Initial array: [5, 2, 9, 1, 5, 6]

Pass 1:

Compare 5 and 2: Swap → [2, 5, 9, 1, 5, 6]
Compare 5 and 9: No swap
Compare 9 and 1: Swap → [2, 5, 1, 9, 5, 6]
Compare 9 and 5: Swap → [2, 5, 1, 5, 9, 6]
Compare 9 and 6: Swap → [2, 5, 1, 5, 6, 9]
Pass 2:

Compare 2 and 5: No swap
Compare 5 and 1: Swap → [2, 1, 5, 5, 6, 9]
Compare 5 and 5: No swap
Compare 5 and 6: No swap (remaining elements are sorted)
Continue this process until no more swaps are needed.

### 2. Selection Sort:
Selection Sort works by finding the smallest element in the unsorted part of the array and swapping it with the first unsorted element.

Example: Initial array: [5, 2, 9, 1, 5, 6]

Pass 1: Find the smallest element (1), swap it with the first element:

Swap 5 and 1: [1, 2, 9, 5, 5, 6]
Pass 2: Find the smallest in the remaining unsorted portion [2, 9, 5, 5, 6], which is 2. No swap needed.

Pass 3: Find the smallest in [9, 5, 5, 6], which is 5, and swap with 9:

Swap 9 and 5: [1, 2, 5, 9, 5, 6]
Pass 4: Find the smallest in [9, 5, 6], which is 5, and swap with 9:

Swap 9 and 5: [1, 2, 5, 5, 9, 6]
Pass 5: Finally, swap 9 and 6:

Swap 9 and 6: [1, 2, 5, 5, 6, 9]

### 3. Insertion Sort:
Insertion Sort works by taking elements from the unsorted portion of the array and inserting them into the correct position in the sorted portion.

Example: Initial array: [5, 2, 9, 1, 5, 6]

Step 1: The first element (5) is already sorted.

Step 2: Insert 2 into the sorted section [5]:

Move 5 right and insert 2: [2, 5, 9, 1, 5, 6]
Step 3: Insert 9 into [2, 5]. No changes since 9 is greater than 5.

Step 4: Insert 1 into [2, 5, 9]:

Move 9, 5, and 2 right, and insert 1: [1, 2, 5, 9, 5, 6]
Step 5: Insert 5 into [1, 2, 5, 9]:

Move 9 right, insert 5: [1, 2, 5, 5, 9, 6]
Step 6: Insert 6 into [1, 2, 5, 5, 9]:

Move 9 right, insert 6: [1, 2, 5, 5, 6, 9]

### 4. Merge Sort:
Merge Sort divides the array into two halves, recursively sorts the two halves, and then merges them.

Example: Initial array: [5, 2, 9, 1, 5, 6]

Divide the array into two halves: [5, 2, 9] and [1, 5, 6]
Recursively sort the halves:
Sort [5, 2, 9]:
Split into [5] and [2, 9]
Sort [2, 9] → Merge to get [2, 9]
Merge [5] and [2, 9] → [2, 5, 9]
Sort [1, 5, 6]:
Split into [1] and [5, 6]
Merge [5] and [6] → [5, 6]
Merge [1] and [5, 6] → [1, 5, 6]
Finally, merge [2, 5, 9] and [1, 5, 6]:
Merge step by step to get [1, 2, 5, 5, 6, 9]

### 5. Quick Sort:
Quick Sort picks a pivot and partitions the array so that elements less than the pivot are on the left, and those greater than the pivot are on the right. It then recursively sorts the partitions.

Example: Initial array: [5, 2, 9, 1, 5, 6]

Choose a pivot (e.g., 5):

Partition: [2, 1] (less than 5) and [9, 5, 6] (greater than or equal to 5)
Recursively sort both partitions:

Sort [2, 1]: Choose 2 as the pivot, resulting in [1, 2]
Sort [9, 5, 6]: Choose 6 as the pivot, resulting in [5, 6, 9]
Combine the partitions:

Sorted array: [1, 2, 5, 5, 6, 9]
