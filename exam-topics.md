# Exam topics
Here is a detailed list what topics you should know for the exam, and also what you do not need to know.

***Note for old students***:
This list is sometimes updated, so there might be differences from when you took the course! If you plan to write a reexam, please make sure you know all topics in this list, even if it was not part of your course instance.

## General knowledge
- Given a problem, knowing which data structure or algorithm to use
- Solving coding problems
- Order-of-growth, big-O notation
- Specific algorithms
- Specific data structures

## Solving coding problems
- Given some simple code, figuring out what it does
- Given some code with holes, fill in the holes so that it works
- Given some code with an error, correct the bug
- Know the pseudocode for some basic algorithms
- Coming up with pseudocode that describes an algorithm
- Given a design for a data structure, figuring out how to implement a simple operation
- Using stacks, queues, sets, maps (including ordered sets and maps), priority queues and graphs in programs
- Combining basic data structures into the data structures you need in a program (e.g., that a multimap can be implemented as a map from keys to sets of values, or how to implement a sparse matrix)

## Complexity / order of growth
- The definition of complexity class, O/Ω/Θ-notation.
- Different kinds of complexity:
    - time (the default), space, number of certain operations (usually a proxy for time complexity)
    - worst-case (the default), average-case
    - amortized complexity, expected complexity
- The difference between different kinds of averaging in complexity analyses:
    - average-case complexity: to average over all possible inputs, and not just the worst possible input (e.g., used when analysing - quicksort)
    - amortized complexity: to average over a sequence of operations, and not just one single operation (e.g., used when analysing dynamic - arrays)
    - expected complexity: to average over a number of operations on the same starting state (e.g., used when analysing randomised - algorithms)
- The most important complexity classes, names for them (constant, logarithmic, linear, quadratic, cubic, exponential), and how they - compare: for example, O(1) < O(log<sub>2</sub> *n*) = O(log<sub>10</sub> *n*) = O(log *n*) < O((log *n*)<sup>2</sup>) < O(*n*) < O(*n* log *n*) < O(*n*<sup>2</sup>) < O(*n*<sup>2</sup> log *n*) < O(*n*<sup>3</sup>) < O(2<sup>*n*</sup>) < O(10<sup>*n*</sup>).
- Simplifying complexity classes, basic reasoning with O/Ω/Θ-notation.
- Given a simple algorithm, ways of determining its complexity class:
    - how to determine the worst-case complexity for sequences and loops
    - how to add and multiply complexity classes
- Understand how we determine the complexities of the algorithms and data structures in the course, including the recursive algorithms - mergesort and quicksort, and the amortized complexity of dynamic arrays.
- Misconceptions:
    - the difference between complexity classes and speed/performance,
    - the difference between saying "X has/is of complexity *f*(*n*)" (O(*f*(*n*)) and "the complexity class of X is *f*(*n*)" or "X is precisely of - complexity *f*(*n*)" (Θ(*f*(*n*))).
- ***You do not need to know***:
    - advanced mathematics to evaluate complexity classes such as integral-based reasoning
    - probabilistic reasoning for precise average-case complexity
    - reasoning about recursive programs
    - complexity for randomized algorithms
    - optimality of searching and sorting

## Complexities for specific data structures and algorithms
- The worst-case complexities of all the important data structures and algorithms that we have introduced in the course.
- Selection sort:
    - always quadratic O(*n*<sup>2</sup>)
- Insertion sort:
    - worst-case quadratic O(*n*<sup>2</sup>)
    - linear O(*n*) for sorted lists
- Merge sort:
    - always linearithmic O(*n* log *n*)
- Quicksort:
    - worst-case quadratic O(*n*<sup>2</sup>)
    - linearithmic O(*n* log *n*) if the input is well-behaved (“average-case”)
    - expected linearithmic O(*n* log *n*) if using a random pivot
    - quadratic O(*n*<sup>2</sup>) on sorted lists, if using the take-first pivot
- Dynamic arrays:
    - worst-case linear O(*n*), for appending one element at the end (this is when the array has to be resized)
    - amortized worst-case constant O(1) for appending elements
    - constant O(1) for looking up a given index
    - worst-case linear O(*n*) for finding an element
    - worst-case logarithmic O(log *n*) for finding an element in a sorted array (binary search)
- Linked lists:
    - constant O(1) for adding an element at the front
    - worst-case linear O(*n*) for finding an element, or looking up an index
- Hash tables (searching, adding and deleting):
    - amortized worst-case linear O(*n*)
    - amortized constant O(1) if the hash function is good and the input is well-behaved
    - it is amortized because we’re using a dynamic array behind the scenes
- BSTs (searching, adding and deleting):
    - worst-case linear O(*n*)
    - logarithmic O(log *n*) if the input is well-behaved (“average-case”)
    - linear O(*n*) if the elements are added in sorted order
- Balanced BSTs (AVL tree, red-black tree):
    - worst-case logarithmic O(log *n*)
- Binary heaps (adding, removing the minimum):
    - worst-case logarithmic O(log *n*)
- Graph algorithms (Kruskal, Prim, UCS/Dijsktra):
    - in a sparse graph, O(|V|) = O(|E|), so we can use *n* = |V| or |E|
    - worst-case linearithmic O(*n* log *n*) on sparse graphs

## Algorithms to know
- Sorting an array: the general case, and some specialised sorts
- Searching in a list: linear and binary search

## Data structures to know
- Lists: arrays, dynamic arrays, linked lists, stacks, queues
    - you may assume that adding to the end of a dynamic array takes constant time
- Search trees: binary search trees, 2-3 trees, red-black trees, AVL trees
- Priority queues: binary heaps
- Hash tables: separate chaining, linear probing
- Graphs: undirected, directed, weighted, unweighted

## Sorting an array: the general case
- Which algorithms are in-place and why this is an advantage
- Insertion sort, selection sort
    - how to loop and insert/select elements
- Top-down mergesort
    - how to merge, how to split, how to recurse
- Quicksort
    - pivots you should know: first element, random element, median of three
    - why the pivot is crucial, why selecting the first element is a bad choice
    - how to partition, how to recurse
    - how to select a pivot
- Know their order-of-growth
    - in the worst case / on an already sorted array / on a random array
    - linear, linearithmic or quadratic, depending on algorithm
- ***You do not need to know***:
    - timsort, bottom-up mergesort, run-based mergesort, 2-pivot quicksort, Tukey’s ninther
    - which algorithms are stable and why this is an advantage

## Searching in a list
- Linear search in an array, and in a linked list
    - how to do it, using a loop
- Binary search in a sorted array
    - how to do it, with and without recursion
- Know the order-of-growth
    - logarithmic or linear, depending on method

## Lists
- Arrays, dynamic arrays
    - how to add an element, how to look up an element, how to remove an element
    - how to resize, when to resize (only for dynamic arrays)
- Linked lists
    - what the nodes look like
    - how to add an element, how to delete an element, how to search for an element
- Stacks, queues
    - how to implement them using a dynamic array, or a linked list
    - implementing a circular queue in an array
- Order-of-growth
    - for adding, for looking up, for removing

## Trees in general
- Size and depth of a tree
- Balanced tree, complete tree
- That the depth of a balanced tree is logarithmic in the size of the tree
- That an unbalanced tree can in the worst case be similar to a linked list

## Search trees
- Unbalanced trees
    - binary search trees (BST)
    - how the tree nodes look like
    - how to insert, how to search, how to delete
    - how to find the minimum, the maximum
    - when a BST becomes unbalanced (if the nodes are inserted in order)
- Balanced trees
    - 2–3 trees, red-black trees, AVL trees
    - how the tree nodes look like
    - how to insert (and rebalance), how to search
        - red-black trees: you may use either the insertion algorithm from the book or the slides, you choose
    - converting a 2–3 tree to/from a red-black tree
- Order-of-growth
    - for insertion, and for searching
    - for unbalanced and balanced trees
- Traversing a tree
    - preorder, inorder, postorder
- ***You do not need to know***:
    - how to delete from a balanced BST or 2–3 tree (but you do need to know for an ordinary “unbalanced” BST)
    - how to implement the ordering-based operations other than min and max (such as range queries, successor, predecessor, etc.)
    - but you do need to be able to use these operations in your programs

## Priority queues
- What is the heap property
- How priority queues are used
- Binary heaps
    - how to store a binary heap in a dynamic array
    - how to delete-min, how to insert

## Hash tables
- Hash functions
    - what is a good / bad hashing function
- What is the load factor
- That hash tables are not ordered
- How to resize, when to resize
    - that the hashing has to be redone after resizing
- Separate chaining
    - how to insert, lookup, and delete a value
- Linear probing
    - how to insert, and lookup a value
    - lazy deletion
- Order-of-growth
    - for insertion, and for searching
    - if you have a good hash function, or a bad one
- ***You do not need to know***:
    - other probing variants than linear probing
    - other ways of deleting in an open addressing hash table, than lazy deletion
    - cryptographic hash functions or similar

## Graphs
- Undirected / directed, unweighted / weighted
- How graph nodes look like
- Adjacency lists
- Features of graphs – what are…?
    - nodes, vertices, edges, paths
    - reachability
    - connected components (for undirected graphs)
    - strongly connected components (for directed graphs)
    - cyclic / acyclic graphs
    - DAGs
    - spanning trees, MSTs (for undirected graphs)
    - shortest path trees (for directed graphs)
    - sparse / dense graphs
- Searching in graphs
    - depth-first search, DFS
    - breadth-first search, BFS
    - Prim’s, Kruskal’s and Dijkstra’s algorithms
    - that DFS/BFS builds solves the reachability problem
    - that BFS builds the shortest path tree in an unweighted graph
    - that UCS/Dijkstra’s builds the shortest path tree in a weighted graph
    - when you can use UCS/Dijkstra’s
    - that Prim’s and Kruskal’s builds the MST in an undirected graph
- Order-of-growth
    - for UCS/Dijkstra’s, Prim’s and Kruskal’s algorithms (using a priority queue)
- ***You do not need to know***:
    - the algorithms by Bellman-Ford, Kusaraju, etc
    - the difference between the “lazy” and the “eager” versions of Prim and Dijkstra
    - A* search
    - Hamilton circuits, Euler circuits
