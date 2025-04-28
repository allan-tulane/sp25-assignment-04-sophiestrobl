# CMPS 2200 Assignment 5
## Answers

**Name:** Sophie Strobl






- **1a.**
log_d n

- **1b.**
The work done by delete-min is O(d log_d n) and the work done by insert is O(log_d n)

- **1c.**
O(∣V∣ * d log_d ∣V∣+∣E∣ * log_d∣V∣)

- **1d.**
d = |E|/|V|

- **2a.**
APSP(0,0,0) = 0

APSP(0,1,0) = -2

APSP(0,2,0) = 2

APSP(1,0,0) = ∞

APSP(1,1,0) = 0

APSP(1,2,0) = 1

APSP(2,0,0) = ∞

APSP(2,1,0) = ∞

APSP(2,2,0) = 0

APSP(i, j, 1):

APSP(0,0,1) = 0

APSP(0,1,1) = -2

APSP(0,2,1) = -1

APSP(1,0,1) = ∞

APSP(1,1,1) = 0

APSP(1,2,1) = 1

APSP(2,0,1) = ∞

APSP(2,1,1) = ∞

APSP(2,2,1) = 0

APSP(i, j, 2):

APSP(0,0,2) = 0

APSP(0,1,2) = -2

APSP(0,2,2) = -1

APSP(1,0,2) = ∞

APSP(1,1,2) = 0

APSP(1,2,2) = 1

APSP(2,0,2) = ∞

APSP(2,1,2) = ∞

APSP(2,2,2) = 0

- **2b.**
APSP(i, j, 2) = min(APSP(i, j, 1), APSP(i, 2, 1) + APSP(2, j, 1))

- **2c.**
APSP(i,j,k) = min(APSP(i,j,k-1), APSP(i,k,k-1) + APSP(k,j,k-1))

The shortest path from i to j is either the shortest path without using vertex k or the path that goes through k, combining the shortest paths from i to k and from k to j.

- **2d.**
The number of distinct subproblems is: n * n * n = n^3

The total work of the dynamic programming algorithm is O(n^3)

- **2e.**
Our algorithm is preferable when the graph is dense or the graph is small enough that O(n^3) work is acceptable.

- **3a.**
No, the MST minimizes total weight, but MMET minimizes the largest edge weight, so MST may not be optimal for MMET.

- **3b.**
To find the next best tree, remove each edge from the MST one at a time, replace it with the lightest edge that reconnects the graph without creating a cycle, and pick the resulting tree with the smallest total weight. This gives the second-best spanning tree.

- **3c.**
The overall work is O(E log E)