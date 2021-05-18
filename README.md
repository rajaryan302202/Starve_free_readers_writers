# Starve_free_readers_writers

Readers Writers problem is a very important synchronization problem where the access to a shared database has to be managed. There are mainly 3 variants of this problem.
The simplest one, referred to as the first readers-writers problem, requires that no readers will be kept waiting unless 
a writer has already obtained permission to used the shared database. In other words, no readers should wait simply because a writer is waiting. The second readers-writers
problem requires that, once a writer is ready, that writer performs its write as soon as possible. In other words, if a writer is waiting to access the shared data, no new 
readers may start reading.

A solution to either the first readers-writers problem or the second readers-writers problem may result in starvation. 
In the first case, writers might starve whereas in the second case, readers might starve.

The third Readers-Writers problem adds the constraint that no thread shall be allowed to starve; that is, the operation of obtaining a lock on the shared data 
will always terminate in a bounded amount of time. In solution provided, we can see how mutual excluison and bounded waiting are taken care of using binary semaphores and mutex locks thereby preventing starvation overall.


