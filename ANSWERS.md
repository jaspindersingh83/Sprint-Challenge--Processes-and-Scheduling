1. List all of the main states a process may be in at any point in time on a
   standard Unix system. Briefly explain what each of these states mean.
* Created : When process is created but hasn't graduated to 'Ready' state on the main memory.
* Ready or Wiating: When the process is loaded in main memory but not yet been executed by any of the cores. Having many states may result in oversaturation.
* Running: When the process gets chosen for execution by the CPU as Kernel mode or User mode. Kernel mode can has unrestricted access to hardware for generally handling sysytem Calls. User mode just has access to its own instruction and data and not the kernel data and intructions
* Blocked: A process is blocked when an external trigger is needed. For eg: a user input, absence of hardware etc.
* Terminated: A process is terminated when it has finished execution or being explicity killed.

2. What is a Zombie Process? How does it get created? How does it get destroyed?

A zombie process or defunt process is the one that has been terminated but still remains on the process table as it is waiting for its parent to read its exit status after the wait call.

3. Describe the job of the Scheduler in the OS in general.
Scheduler is gate keeper that designates hardware to computation elements like processes, threads and data flows.

4. Describe the benefits of the MLFQ over a plain Round-Robin scheduler.

Round Robin: This scheduler spreads CPU time between many different vying processes all at once. It may affect the performance and ignore the priority of certain processes over others.

MLFQ: MLFQ has dyanamic queue with varying priority. It keeps changing the priority of given processes based on behavior it displays during "Running State".
So MLFQ "learns" from processes and makes a real time decision for future course of action
