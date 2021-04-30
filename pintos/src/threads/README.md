# Threads: Design Document

<!-- toc -->
- [Part 1: Alarm](#part-1:-alarm)
- [Part 2: Priority Donation](#part-2:-priority-donation)
- [Part 3: Advanced Scheduler](#part-3:-advanced-scheduler)

## Part 1: Alarm

description here

### DATA STRUCTURES

- A1: Copy here the declaration of each new or changed `struct` or `struct member, global or static variable, typedef, or enumeration`.  Identify the purpose of each in 25 words or less.
    > answer here

### ALGORITHMS

- A2: Briefly describe what happens in a call to timer_sleep(), including the effects of the timer interrupt handler.
    > answer here

- A3: What steps are taken to minimize the amount of time spent in the timer interrupt handler?
    > answer here

### SYNCHRONIZATION

- A4: How are race conditions avoided when multiple threads call timer_sleep() simultaneously?
    > answer here

- A5: How are race conditions avoided when a timer interrupt occurs during a call to timer_sleep()?
    > answer here

### RATIONALE

- A6: Why did you choose this design?  In what ways is it superior to another design you considered?
    > answer here

## Part 2: Priority Donation

description here

### STRUCTURES

- B1: Copy here the declaration of each new or changed `struct` or `struct member, global or static variable, typedef, or enumeration`.  Identify the purpose of each in 25 words or less.
    > answer here

- B2: Explain the data structure used to track priority donation. Use ASCII art to diagram a nested donation.  (Alternately, submit a .png file.)
    > answer here

### ALGORITHMS

- B3: How do you ensure that the highest priority thread waiting for a lock, semaphore, or condition variable wakes up first?
    > answer here

- B4: Describe the sequence of events when a call to lock_acquire() causes a priority donation.  How is nested donation handled?
    > answer here

- B5: Describe the sequence of events when lock_release() is called on a lock that a higher-priority thread is waiting for.
    > answer here

### SYNCHRONIZATION

- B6: Describe a potential race in thread_set_priority() and explain how your implementation avoids it.  Can you use a lock to avoid this race?
    > answer here

### RATIONALE

- B7: Why did you choose this design?  In what ways is it superior to another design you considered?
    > answer here

## Part 3: Advanced Scheduler

description here

### STRUCTURES

- C1: Copy here the declaration of each new or changed `struct` or`struct' member, global or static variable, typedef, or enumeration`.  Identify the purpose of each in 25 words or less.
    > answer here

### ALGORITHMS

- C2: Suppose threads A, B, and C have nice values 0, 1, and 2.  Each has a recent_cpu value of 0.  Fill in the table below showing the scheduling decision and the priority and recent_cpu values for each thread after each given number of timer ticks:

    | timer ticks | recent_cpu A | recent_cpu B | recent_cpu C | priority A | priority B | priority C | thread to run |
    | ----------- | ------------ | ------------ | ------------ | ---------- | ---------- | ---------- | ------------- |
    | 0
    | 4
    | 8
    |12
    |16
    |20
    |24
    |28
    |32
    |36

- C3: Did any ambiguities in the scheduler specification make values in the table uncertain?  If so, what rule did you use to resolve them?  Does this match the behavior of your scheduler?
    > answer here

- C4: How is the way you divided the cost of scheduling between code inside and outside interrupt context likely to affect performance?
    > answer here

### RATIONALE

- C5: Briefly critique your design, pointing out advantages and disadvantages in your design choices.  If you were to have extra time to work on this part of the project, how might you choose to refine or improve your design?
    > answer here

- C6: The assignment explains arithmetic for fixed-point math in detail, but it leaves it open to you to implement it.  Why did you decide to implement it the way you did?  If you created an abstraction layer for fixed-point math, that is, an abstract data type and/or a set of functions or macros to manipulate fixed-point numbers, why did you do so?  If not, why not?
    > answer here
