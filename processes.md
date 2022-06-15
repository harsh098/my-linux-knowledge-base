# Processes in Linux
A process is simply an instance of one or more related tasks (threads) executing on your computer. It is not the same as a program or a command.  
A single command may actually start several processes simultaneously.Some processes are independent of each other and others are related.  
A failure of one process may or may not affect the others running on the system.
### Process Types
|Process Type|Description|Example|
|------------|-----------|-------|
|Interactive Processes|started by user via terminal or GUI|ps, top, firefox|
|Batch Processes|Scheduled from and executed automatically from terminal then disconnected on FIFO basis|updatedb, ldconfig|
|Daemons|Server processes that run continuously. Many are launched during system startup and then wait for a user or system request indicating that their service is required.|httpd, sshd|
|Threads|Lightweight processes. These are tasks that run under the umbrella of a main process, sharing memory and other resources, but are scheduled and run by the system on an individual basis. An individual thread can end without terminating the whole process and a process can create new threads at any time. Many non-trivial programs are multi-threaded.|firefox, gnome-terminal-server|
|Kernel Threads|Kernel tasks that users neither start nor terminate and have little control over. These may perform actions like moving a thread from one CPU to another, or making sure input/output operations to disk are completed.|kthreadd, migration, ksoftirqd|  

### Scheduler
A critical kernel function called the `scheduler` constantly shifts processes on and off the CPU, sharing time according to relative priority, how much time is needed and how much has already been granted to a task.

### States
Some important process states include 
  1. Running/Active
  2. Sleep/Queued
  3. Zombie  

