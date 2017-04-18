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
* E1. Safety
* E2. Liveness

### 3 Requirements of Distributed Mutual Exclusion Algorithms
* ME1. Safety
* ME2. Liveness
* ME3. Ordering

### 2 Assumptions of Cristians Simple Method
1. Time Out and Time Back are same or very similar
2. Timeserver does not fail

### 2 Fundamental Concepts of Distributed Object Model
1. Remote Object Reference
2. Remote Interface

### 3 Implementation Choices of Request Reply Protocol
1. Maybe
2. At Least Once
3. At Most Once

### 3 Major Requirements of a DFS

### 3 Implications Shared By All Distributed Systems
1. Concurrency
 * How to organise concurrency across a distributed system (Dealing with mutexes etc. but by only passing messages).

2. No Global Clock
 * Need a shared idea of time between coordinating processes.

3. Independent Failures
 * Failures are almost guaranteed, need to deal with these gracefully so as to not interupt service.
 * Partial Failure
 
### 3 Types of Multicast Ordering
1. FIFO
 * If a process P mulitcasts message M first then M', M will be delivered before M'. Multicasts from other processes arrive in arbitrary order.
2. Casual
 *  Only respects happened before (->)
3. Total
 * Delivery of m before m' on any process forces delivery of m before m' on all other processes

### 4 Main Tasks of Recovery Manager
1. To save objects in permanent storage (in a recovery file) for committed transactions; 
2. To restore the server’s objects after a crash;
3. To reorganize the recovery file to improve recovery performance; 
4. To reclaim storage space (in the recovery file)

### 3 Types of Failure
1. Omission Failures
2. Arbitrary Failures
3. Timing Failures

### Rules for Updating Vector Clocks
* VC1. Initially, Vi [j] = 0 for i, j = 1, 2, …, N 
* VC2. Just before Pi timestamps an event, its sets Vi [i] = Vi [i] + 1
* VC3. Pi includes the value t = Vi in every message it sends 
* VC4. When Pi receives a timestamp in a message, it sets Vi [j] = max(Vi [j], t[j]) for j = 1, 2, ..., N
