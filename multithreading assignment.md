```python
1.What is multithreading in python ? why is it used? Name the module used to handle threads in python .
Ans-
    Mechanism that allows multiple threads of execution to run concurrently within a single process .A thread is a separate
    
    1.Improving performance by running multiple CPU bound tasks concurrently.
    2.creating responsive and interactive user interface that can handle multiple input and output events.
    3.Managing long-running operations that would otherwise block the main program thread, such as network comunnication,files
    
    In python ,the module used to handle is called "threading ".This module provides a way to create and manage threads 
```


```python
2.Why threading module used? write the use of the following functions:
          1.activecount()
          2.currentthread()
          3.enumerate()
        
        Ans-
        
        The threading module is used in pytho to ceate and manage threads in a multi-threaded applications.It provides
            
             1.activecount()-This function returns the number of active thread objects in the current thread's thread control blocks
             2.xurrentThread()-This function returns a reference to the current thread object which can be useful for identifying
             3.enumerate()-This function returns a list of all active thread objects in the current process .It can be used to get 
```


```python
3.Explain the following functions:
    1.run()
    2.start()
    3.join()
    4.isAlive()
    Ans- 
        
    1.run()- This method is called when a thread is starting uing the 'start'() method .It contains this code that will be executed
    2.start()-This method starts the execution of the thread.when this mrethod is called a new thread is created and the 'run'() method
    3.join()- This method blocks the calling thread until the thread on which it is called has completed its execution .It can be
    4.isAlive()- This method returns a boolean value indicating whether the thread is currently executing or not.
```


```python
4.write a python program to create two threads.Threads one must the list of squares and thread to must print the list 

Ana- 
      import threading
    
    def print_squares():
        for i in range(1,6):
            print(f"square of {i} is {i**3}")
            
    def print_cubes():
        for i in range(1,6):
            print(f"cube of {i} is {i**3"}

    if __name__=="__main__":
         t1 = threading .Thread(target=print_squares)
         t2 = threading.Thread(target=print_print_cubes)
       
         t1.start()
         t2.start()

         t1.join()
         t2.join()
  
         print("Done")

  output:
         square of 1 is 1
         cube of 1 is 1
         square of 2 is 4
         cube of 2 is 8
         square of 3 is 9
         cube of 3 is 27
         square of 4 is 16
         cube of 4 is 64
         square of 5 is 25
         cube of 5 is 125
         done

    
```


```python
5.state advantages and disadvantages of multithreading.
Ans-
    Multithreading ia a powerful programing technique that allows a program to execute multiple threads of control can current
    
     Advantages:
            1.Improving performance
            2.Responsiveness
            3.Resource sharing
            4.Modularity
            
            
     Disadvantages:
            1.complexity
            2.synchronization
            3.Increased memory usage
            4.overhead 
```


```python
6.Explain deadlock and race conditions 
Ans- 
    Deadlock: A deadlock occurs when two or more threads are waiting for each other to release a resources ,such as a lock 
    In other worsd ,each thred is blocked and waiting for a resources that another thread is holding ,and the program become
    
    Race conditon:A race condition occurs when the behaviour of a program depends on the relatives timing and interleaving
    In other words,the outcome of the program can vary depending on the order in which the threads executethis can lead to
    
    To avoid deadlocks and race conditions in mutithreaded program,it is important to follow best practices such as proper condition 
```
