# ch02intro
Introduction to OS, Chapter 02

Read [Introduction to OS](http://pages.cs.wisc.edu/~remzi/OSTEP/intro.pdf) and answer the following review questions.

1. **What is an operating system? What does it do?** 

The body of a software, which is responsible for making easier for programs to interact with hardware(like sharing memory), is called OS.

2. **What is virtualization?** - Virtualisation -  makes operation system possible
to simulate, on a single actual (“physical”) computer, several to many “virtual”
computers which use their own operating system and look like real computers to
programs running on them. The common virtualisation infrastructures make it possible to
“migrate” virtual machines very quickly from one physical machine to another,
and this lets you as the operator of such an infrastructure react very conveniently
cloud computing to load situations or malfunctions.

3. **How does an OS provide access to its features?** It provides some interfaces (APIs), that system calls in order to run programs. Sometimes we call them standard libraries for applications.
4. **What illusion does a virtualized CPU provide?** We can do different thing current time. For example:
	We can write a program, by listening music and other download movie from the INTERNET.  
    - **How does this affect the user experience?** Just perfectly.Because it helps for users to be more productive.
    - **How does this affect the developer experience?** Of course for developers to write code for virtualisation could be hard. 
    - **What if the CPU were not virtualized?** If not. We would do one thing at the current time. It isn't efficient. 
5. **What is a memory address?** To read memory, one must specify an address to be able to access
the data stored there; to write (or update) memory, one must also specify
the data to be written to the given address.
6. **What is memory virtualization?** In computer science, memory virtualization decouples 
		volatile random access memory (RAM) resources from individual 
		systems in the data center, and then aggregates those resources into a virtualized memory pool 
		available to any computer in the cluster
    - **Why would we want this?** 
		a)More application can run at once
		b)Larger applications can run with less RAM without need to buy more memory.
		c)Allows speed gain when only a particular segment of the program is required for the execution of the program.
8. **What happens if you write a C/C++ program that writes past the end of an array?**  It rewrites a variable stored after such array. For example it can 
		rewrite variable i used in FOR cycle. In such case some I values can be skipped or the loop will never end.
		Or it can rewrite a callstack. In such case CPU forgets the return address 
		(address where to jump after finishing the function).
     
	 - **Can this affect other programs?** Yes,it can.possibly create malfunctions in other
		programs that would be impossible to find. Because the bugs didn’t even originate in those programs.

9. **What is a thread?** A thread is a part of the operating system, which is responsible for execution of only one instruction.
10. **Why would we ever write a multi-threaded program?** - Here's some advantages of multi-threaded program:
		a)Improved performance and concurrency
		b)Simplified coding of remote procedure calls and conversations
		c)Simultaneous access to multiple applications
		d)Reduced number of required servers
11. **What is atomicity?** Atomic means that an operation is done without the chance for another thread to interrupt it and do something in the middle of it.
    - **Is a C/C++ statement atomic?** The C standard does not define whether it is atomic or not. In practice it shows it isn't.
    - **Is a Java statement atomic?** Most operations are indeed atomic. Operations involving 64 bit structures like double / long are not atomic by themselves. The 64 bit operation can be split into 2 32 bit operations. 
    - **Is an assembler statement atomic?** You cannot assume one machine code will execute atomically.  

13. **What does persistence mean?** In system memory, data can be easily lost, as devices such as DRAM store values in a volatile manner; when power goes away or the system crashes, any data in memory is lost. Thus, we need hardware and software to be able to store data persistently.
14. **How does OS hard drive virtualization differ from CPU & memory virtualization?** Because CPU virtualization - Each virtual machine appears to run on its own CPU (or a set of CPUs), fully isolated from other virtual machines. Registers, the translation 
	lookaside buffer, and other control structures are maintained separately for each virtual machine.Whereas memory virtualisation A contiguous memory space is visible to each virtual machine. However, the allocated physical memory might not be contiguous. 
	Instead, noncontiguous physical pages are remapped and presented to each virtual machine. 
15. **How does running multiple programs at the same time increase CPU efficiency?** Instead of just running one task at a time, the OS would load a lot of tasks into memory and switch between them, which improves CPU utilization. 
16. **What is multiprogramming?** A multiprogramming is a parallel processing in which 
	the multiple programs can run simultaneously.We all mostly use uniprocessor PC/Mobile/Tablet but never 
	wonder how the processor works.
