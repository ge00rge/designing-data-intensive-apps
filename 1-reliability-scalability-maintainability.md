
**Reliability**

The system should continue to work correctly even in the face of adversity (hardware faults, software faults, human error)
			 
Continue to work correctly even when things go wrong.

**Scalability**

Systems ability to cope with high load.

Median can be used to know how long users have to wait for a request to be successful.

We can also look at high percentiles. 

For ex: if 95th percentile response time is 1.5 secs that means 95% of requests take less than 1.5 secs and the other 5% of the time more.


Approaches for coping with load: 

1. **Scaling up** (vertical scaling): moving to a more powerful machine.


2. **Scaling out** (horizontal scaling): distributing load accross multiple smaller machines.

Some systems are elastic: automatically add computing resources when they detect a load increase, useful if load is unpredictable.

**Maintainability**

- **Operability**: Make it easy for operations teams to keep the system running smoothly. 


- **Simplicity**: Make it easy for new engineers to understand the system.


- **Evolvability**: Make it easy for engineers to make changes to the system in the future. 
