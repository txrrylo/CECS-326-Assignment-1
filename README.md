# CECS 326 Assignment 1 - Introduction to Operating Systems

## Assignment Description: Answer the following questions from the Chapter 1 reading from your textbook. Be thorough and complete with your answers. You may work on these questions with one or two other partners, but *all* students must submit the document individually in their own repositories along with each student's name documented with the submission.
 

### 1. What are the two main functions of an operating system?
*The two main functions of an operating system are used as an extended machine and a resource manager. The extended machine acts as an interface between the user and the hardware, making the computer easier to use without worrying about the technical details. The resource manager manages system resources, like deciding which program gets CPU time, how memory is allocated, and handling file storage, so everything can run efficiently.*

### 2. What is the difference between timesharing and multiprogramming systems?
*Multiprogramming is about efficiency where it keeps multiple programs in memory at once so the CPU always has something to do while reducing idle time. However, timesharing is about fairness as it rapidly switches between multiple users or tasks which it gives the illusion that they have their own personal computer, even though they’re actually just sharing resources.*

### 3. The family-of-computers idea was introduced in the 1960s with the IBM System/360 mainframes. Is this idea now dead as a doornail or does it live on?
*Not dead at all as it’s practically everywhere. Modern processors like the x86 family or ARM processors continue to evolve on a day to day basis while maintaining compatibility with older models. Even operating systems like Windows, macOS, and Linux follow this concept which runs on different hardware but keeping a familiar experience across devices.*

### 4. What is the difference between kernel and user mode? Explain how having two distinct modes aids in designing an operating system.
*A computer runs in kernel mode when it needs full access to hardware and system resources like managing memory or handling system calls. In user mode, applications run with restrictions to prevent them from accidentally (or intentionally) breaking the system. This separation is crucial for security and stability as it stops regular programs from interfering with critical system operations.*

### 5. On early computers, every byte of data read or written was handled by the CPU (i.e., there was no DMA). What implications does this have for multiprogramming?
*Without Direct Memory Access (DMA), the CPU had to personally handle every tiny data transfer, which was a huge waste of time. This made multiprogramming inefficient because the CPU couldn’t switch to another task while waiting for slow input/output operations. Modern systems use DMA so the CPU can focus on processing while data transfers happen in the background.*

### 6. There are several design goals in building an operating system, for example, resource utilization, timeliness, robustness, and so on. Give an example of two design goals that may contradict one another.
*One common trade-off is security versus performance. The more security checks an OS performs (like encryption or access control), the slower it runs. Another example is usability versus resource efficiency. Allowing users to keep many applications open makes life easier, but it also consumes more CPU and memory, which can slow things down.*

### 7. Which of the following instructions should be allowed only in kernel mode?
    (a) Disable all interrupts. *Yes, because it could freeze the system if misused*
    (b) Read the time-of-day clock. *No, because it doesn't affect anything*
    (c) Set the time-of-day clock. *Yes, since changing the clock affects the whole system*
    (d) Change the memory map. *Yes, because it controls how memory is allocated, which could lead to security risks if done improperly)

### 8. Consider a system that has two CPUs, each CPU having two threads (hyperthreading). Suppose three programs, P0, P1, and P2, are started with run times of 5, 10 and 20 msec, respectively. How long will it take to complete the execution of these programs? Assume that all three programs are 100% CPU bound, do not block during execution, and do not change CPUs once assigned.
*Since the system has four logical processors, it can run up to four programs at the same time. With only three programs running, they will all execute in parallel. The longest-running program (P2) takes 20 milliseconds, so all programs will finish in 20 milliseconds.*

### 9. What is a trap instruction? Explain its use in operating systems.
*A trap instruction is like a program’s way of calling for help from the operating system. It’s used when a program needs the OS to do something it can’t do on its own, like opening a file, creating a new process, or handling an error (like dividing by zero). When a trap happens, control shifts from the program to the OS, which then handles the request safely.*

### 10. Modern operating systems decouple a process address space from the machine’s physical memory. List two advantages of this design.
_First, it provides memory isolation, meaning each program gets its own protected memory space, preventing one program from accidentally overwriting another’s data. Second, it allows virtual memory, meaning programs can use more memory than is physically available by temporarily storing data on disk. This makes the system more flexible and efficient._
