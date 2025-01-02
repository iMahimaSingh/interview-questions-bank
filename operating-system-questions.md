#  Basic Operating System Interview Questions .

---

#### 1. What is an Operating System (OS)?  
Answer: 
An OS is a system software that manages hardware and software resources, acting as an interface between users and hardware. It ensures efficient execution of user programs and facilitates resource allocation.

---

#### 2. What are the main functions of an OS? 
Answer:  
1. Process Management: Handles process creation, scheduling, and termination.  
2. Memory Management: Allocates and deallocates memory to processes.  
3. File System Management: Manages file creation, deletion, and access.  
4. Device Management: Controls device communication through drivers.  
5. Security: Protects data and resources from unauthorized access.  
6. User Interface: Provides CLI or GUI for user interaction.

---

#### 3. What is a kernel?  
Answer: 
The kernel is the core component of the OS, residing in memory. It provides low-level services like process scheduling, memory management, and hardware communication, ensuring the system's stability and performance.

---

#### 4. What are the types of Operating Systems? 
Answer:  
1. Batch OS: Processes jobs in batches without user interaction.  
2. Time-Sharing OS: Allows multiple users to share CPU time interactively.  
3. Distributed OS: Manages multiple systems as one logical unit.  
4. Real-Time OS: Processes tasks within a strict time deadline.  
5. Multi-tasking OS: Runs multiple tasks simultaneously.  
6. Mobile OS: Optimized for mobile devices.

---

#### 5. What is the difference between a process and a thread? 
Answer:  
- Process: An independent execution unit with its own memory space, executed in isolation.  
- Thread: A lightweight execution unit within a process, sharing the same memory and resources.

---

#### 6. Explain process states in an OS.**  
Answer:  
1. New: Process creation initiated.  
2. Ready: Process ready for execution, awaiting CPU scheduling.  
3. Running: Instructions are being executed.  
4. Waiting: Process paused, waiting for I/O or event.  
5. Terminated: Process completed and removed from memory.

---

#### 7. What is a context switch? 
Answer: 
A context switch occurs when the CPU switches from one process to another, saving the current process's state and loading the next. It ensures efficient multitasking but adds overhead.

---

#### 8. Explain deadlock. 
Answer:  
Deadlock is a state where processes are blocked, each waiting for a resource held by another, resulting in an indefinite halt. It occurs when circular dependency exists.

---

#### 9. What are the conditions for a deadlock?  
Answer:  
1. Mutual Exclusion: Resources are non-shareable.  
2. Hold and Wait: Process holding resources waits for additional resources.  
3. No Preemption: Resources cannot be forcibly taken.  
4. Circular Wait: Processes form a circular chain of dependencies.

---

#### 10. What is virtual memory? 
Answer:  
Virtual memory is a memory management technique that creates an illusion of infinite memory by using disk space to extend physical memory. It enables efficient multitasking by paging.

---

#### 11. What is demand paging?  
Answer:  
Demand paging loads memory pages into physical memory only when they are referenced, reducing memory usage. Non-referenced pages remain in secondary storage.

---

#### 12. What is a page fault?  
Answer: 
A page fault occurs when a process references a page not currently in RAM. The OS retrieves the page from secondary storage and updates the page table.

---

#### 13. What are scheduling algorithms?  
Answer:  
Scheduling algorithms manage process execution order. Examples:  
- FCFS (First Come First Serve): Processes executed in arrival order.  
- SJF (Shortest Job First): Process with the shortest execution time is scheduled first.  
- Round Robin (RR): Each process gets a fixed time quantum cyclically.  
- Priority Scheduling: Processes are scheduled based on priority.

---

#### 14. What is the difference between multitasking and multiprocessing? 
Answer:
- Multitasking: Multiple tasks share a single CPU, executed alternately.  
- Multiprocessing: Multiple CPUs execute processes simultaneously, increasing throughput.

---

#### 15. What is a semaphore? 
Answer:  
A semaphore is a synchronization primitive used to control access to shared resources in concurrent programming, preventing race conditions and ensuring mutual exclusion.

---

#### 16. What are the types of semaphores? 
Answer:  
1. Binary Semaphore: Allows only one process (0 or 1 value).  
2. Counting Semaphore: Manages multiple instances of a resource.

---

#### 17. Explain the difference between primary and secondary memory. 
Answer:  
- Primary Memory: Volatile, high-speed memory directly accessible by the CPU (e.g., RAM, Cache).  
- Secondary Memory: Non-volatile, slower, and used for long-term storage (e.g., SSD, HDD).

---

#### 18. What is an interrupt? 
Answer:  
An interrupt is a signal sent to the CPU to indicate an event requiring immediate attention, like hardware failure or I/O completion. It temporarily halts the current task to address the interrupt.

---

#### 19. What are system calls?  
Answer:  
System calls are OS-provided APIs that enable user programs to request kernel-level services like file operations, process control, and memory allocation.

---

#### 20. What is the difference between monolithic and microkernel architecture? 
Answer: 
- Monolithic Kernel: Combines all OS functionalities in a single layer, offering better performance but less modularity.  
- Microkernel: Keeps only essential services in kernel space, improving modularity and security while reducing performance.

---

#### Medium-Level Operating System Interview Questions**

21. What is the difference between paging and segmentation?  
   - Paging divides memory into fixed-size blocks, while segmentation divides memory into variable-sized blocks based on logical divisions like functions or objects.

22. Explain the concept of multithreading.  
   - Multithreading allows multiple threads within a single process to run concurrently, sharing the same memory space to improve performance and resource utilization.

23. What are system calls, and why are they important? 
   - System calls are APIs provided by the OS to interact with hardware and perform operations like file manipulation, process control, and memory management.

24. What is a critical section, and how is it managed?  
   - A critical section is a part of the program where shared resources are accessed. It is managed using synchronization mechanisms like mutexes, semaphores, or monitors.

25. What are the differences between preemptive and non-preemptive scheduling? 
   - Preemptive scheduling allows the OS to interrupt a running process, while non-preemptive scheduling waits until the process voluntarily releases the CPU.

26. Explain Belady’s Anomaly in the context of page replacement algorithms. 
   - Belady’s Anomaly occurs when increasing the number of page frames results in more page faults in certain algorithms, like FIFO.

27. What are interrupts, and how are they handled in an OS?  
   - Interrupts are signals from hardware or software indicating an event. The OS handles them via an Interrupt Service Routine (ISR) and resumes normal execution afterward.

28. What is the difference between a hard link and a soft link in file systems? 
   - A hard link is a direct pointer to a file, sharing the same inode, while a soft link (symbolic link) is a shortcut pointing to the file's location.

29. What is the difference between synchronous and asynchronous I/O?  
   - Synchronous I/O waits for an operation to complete before continuing, while asynchronous I/O allows the program to proceed without waiting.

30. What are the advantages of virtual memory?  
    - Virtual memory provides process isolation, allows larger programs to run than physical memory, and enhances multitasking by using disk space as an extension of RAM.

31. How does the OS prevent deadlocks?  
    - Deadlocks are prevented using techniques like resource allocation graphs, avoiding circular wait, or employing the Banker’s Algorithm.

32. What is the difference between user-level threads and kernel-level threads?  
    - User-level threads are managed by user libraries and are faster, while kernel-level threads are managed by the OS and support system-wide multi-threading.

33. Explain the concept of thrashing in virtual memory systems.  
    - Thrashing occurs when excessive paging leads to low CPU utilization, as the system spends more time swapping pages than executing processes.

34. What is DMA (Direct Memory Access), and why is it important?  
    - DMA allows peripherals to access memory directly without CPU intervention, improving performance by reducing the CPU's workload.

35. What is a scheduler, and what are its types?  
    - A scheduler determines process execution order. Types include:
      - Long-term scheduler: Controls job admission.
      - Short-term scheduler: Allocates CPU to ready processes.
      - Medium-term scheduler: Manages suspended processes.

36. Explain the difference between RAID 0 and RAID 1. 
    - RAID 0 (striping) improves performance but offers no redundancy, while RAID 1 (mirroring) provides data redundancy by duplicating data on two drives.

37. What are inode and superblock in a file system? 
    - An inode contains metadata about a file, while a superblock contains information about the file system, like size, block count, and status.

38. How does the OS handle priority inversion?  
    - Priority inversion is resolved using priority inheritance, where a low-priority process inherits the higher priority of the waiting process.

39. What are the benefits and challenges of a microkernel architecture?  
    - Benefits: Better modularity and security.  
      Challenges: Higher overhead due to user-space interactions.

40. What is spooling in operating systems?  
    - Spooling (Simultaneous Peripheral Operations OnLine) queues data for devices like printers, enabling overlapping I/O and process execution.



