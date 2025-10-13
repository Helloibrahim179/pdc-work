DFA Performance Comparison: Multithreading vs Multiprocessing

In this project, we compare how the execution time of a Deterministic Finite Automaton (DFA) program changes when we use different numbers of threads and processes to perform DFA validation on a set of strings.

We tested the performance using 5, 10, and 15 threads and 5, 10, and 15 processes to understand how the number of concurrent tasks affects the overall runtime.
Multithreading Results:
| Threads | Time Taken     |
| ------- | -------------- |
| 5       | 0.0232 seconds |
| 10      | 0.0455 seconds |
| 15      | 0.0624 seconds |
Multiprocessing Results:
| Processes | Time Taken     |
| --------- | -------------- |
| 5         | 1.1520 seconds |
| 10        | 1.3786 seconds |
| 15        | 1.8513 seconds |
Comparison Summary

Multithreading performs much better than Multiprocessing for this particular task, as expected. This is because threads share the same memory space, making them more efficient in terms of time, especially when the task is not computationally heavy.

Multiprocessing uses separate memory spaces for each process, leading to higher memory usage and more time spent on inter-process communication and context switching.

Conclusion

After testing with various thread and process counts, the results clearly show that multithreading provides significant performance benefits in cases like DFA validation, where tasks are lightweight and do not require heavy CPU or memory resources. On the other hand, multiprocessing is less efficient here due to its higher memory footprint and slower execution, making it less suited for this type of workload.
