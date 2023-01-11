# producer-consumer-problem

In computing, the producer-consumer problem (also known as the bounded-buffer problem) is a family of problems described by Edsger W. Dijkstra since 1965.

Dijkstra found the solution for the producer-consumer problem as he worked as a consultant for the Electrologica X1 and X8 computers: "The first use of producer-consumer was partly software, partly hardware: The component taking care of the information transport between store and peripheral was called 'a channel' ... Synchronization was controlled by two counting semaphores in what we now know as the producer/consumer arrangement: the one semaphore indicating the length of the queue, was incremented (in a V) by the CPU and decremented (in a P) by the channel, the other one, counting the number of unacknowledged completions, was incremented by the channel and decremented by the CPU. [The second semaphore being positive would raise the corresponding interrupt flag.]"

Dijkstra wrote about the unbounded buffer case: "We consider two processes, which are called the 'producer' and the 'consumer' respectively. The producer is a cyclic process and each time it goes through its cycle it produces a certain portion of information, that has to be processed by the consumer. The consumer is also a cyclic process and each time it goes through its cycle, it can process the next portion of information, as has been produced by the producer ... We assume the two processes to be connected for this purpose via a buffer with unbounded capacity."

He wrote about the bounded buffer case: "We have studied a producer and a consumer coupled via a buffer with unbounded capacity ... The relation becomes symmetric, if the two are coupled via a buffer of finite size, say N portions"

And about the multiple producer-consumer case: "We consider a number of producer/consumer pairs, where pairi is coupled via an information stream containing ni portions. We assume ... the finite buffer that should contain all portions of all streams to have a capacity of 'tot' portions."

Per Brinch Hansen and Niklaus Wirth saw soon the problem of semaphores: "I have come to the same conclusion with regard to semaphores, namely that they are not suitable for higher level languages. Instead, the natural synchronization events are exchanges of message."
