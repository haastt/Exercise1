# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to a repository to complete the task. Remember to also submit your answers to Blackboard

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > *Concurrency is handling several things at once and parallelism is doing several things at once.*
 
 ### Why have machines become increasingly multicore in the past decade?
 > *CPU frequency can not get faster and the CPUs are used in general-purpose machines.*
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > *One can model things that happens simultaneously, and one can utilize the multicore hardware.*
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *Your answer here*
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > -	Process
 > o	An executing program that provides the recources that one needs to execute a program.
 > -	Thread 
 > o	A “unit of execution” which is scheduled by the OS and it can be paused and resumed.
 > -	Green thread 
 > o	A thread which is managed and scheduled by the runtime  
 > -	Co-routines 
 > o	Scheduled by the user, not runtime or OS-managed
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > -	Pthread-create() = OS-managed thread 
 > -	threading.Thread() = OS-managed thread
 > -	go = Creates a co-routine, but looks like a green thread from a programmers pov

 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > *The interpreter in pyhthon looks at one piece of code at a time, so spawning more OS threads does not increase performance.*
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > *-	Using more interpreters and sharing memory between them*
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > *Distributes/maps go routines over more OS threads*
