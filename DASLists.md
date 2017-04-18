These are all of the little lists that exist in DAS that need to be learned!

- [ ]  [3 Rules of Happened Before](https://github.com/kfow/L4CSTopics/blob/master/DASLists.md#3-rules-of-happened-before)
- [ ]  [2 Problems of Concurrency in Distributed Systems](https://github.com/kfow/L4CSTopics/blob/master/DASLists.md#2-problems-of-concurrency-in-distributed-systems)
- [ ]  [2 Requirements of Election Algorithms](https://github.com/kfow/L4CSTopics/blob/master/DASLists.md#2-requirements-of-election-algorithms)
- [ ]  [3 Requirements of Distributed Mutual Exclusion Algorithms](https://github.com/kfow/L4CSTopics/blob/master/DASLists.md#3-requirements-of-distributed-mutual-exclusion-algorithms)
- [ ]  [2 Assumptions of Cristians Simple Method](https://github.com/kfow/L4CSTopics/blob/master/DASLists.md#2-assumptions-of-cristians-simple-method)
- [ ]  [2 Fundamental Concepts of Distributed Object Model](https://github.com/kfow/L4CSTopics/blob/master/DASLists.md#2-fundamental-concepts-of-distributed-object-model)
- [ ]  [3 Implementation Choices of Request Reply Protocol](https://github.com/kfow/L4CSTopics/blob/master/DASLists.md#3-implementation-choices-of-request-reply-protocol)
- [ ]  [3 Major Requirements of a DFS](https://github.com/kfow/L4CSTopics/blob/master/DASLists.md#3-major-requirements-of-a-dfs)
- [ ]  [3 Implications Shared By All Distributed Systems](https://github.com/kfow/L4CSTopics/blob/master/DASLists.md#3-implications-shared-by-all-distributed-systems)
- [ ]  [3 Types of Multicast Ordering](https://github.com/kfow/L4CSTopics/blob/master/DASLists.md#3-types-of-multicast-ordering)
- [ ]  [4 Main Tasks of Recovery Manager](https://github.com/kfow/L4CSTopics/blob/master/DASLists.md#4-main-tasks-of-recovery-manager)
- [ ]  [Rules for Vector Clocks](https://github.com/kfow/L4CSTopics/blob/master/DASLists.md#rules-for-vector-clocks)


### 3 Rules of Happened Before
1. If A happened before B the A -> B
2. send(A) -> receive(A)
3. If A->B and B->C then A->C (Transitivity)

### 2 Problems of Concurrency in Distributed Systems
1. Inconsistent Reads
2. Lost Update Problem

### 2 Requirements of Election Algorithms
E1. Safety
E2. Liveness

### 3 Requirements of Distributed Mutual Exclusion Algorithms
ME1. Safety
ME2. Liveness
ME3. Ordering

### 2 Assumptions of Cristians Simple Method
1. Time Out and Time Back are same or very similar
2. Timeserver does not fail

### 2 Fundamental Concepts of Distributed Object Model
1. Remote Object Reference
2. Remote Interface

### 3 Implementation Choices of Request Reply Protocol
1. Maybe
  * It maybe happens more than once, dunno though
2. At Least Once
3. At Most Once
### 3 Major Requirements of a DFS

### 3 Implications Shared By All Distributed Systems

### 3 Types of Multicast Ordering
1. FIFO
2. Casual
3. Total

### 4 Main Tasks of Recovery Manager

### Rules for Vector Clocks
