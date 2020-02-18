# SparkLearning
All Spark learning put in one place. 

## Table of contents:
1. [Chapter 1: Introduction to High Performance Spark](#Chapter1)


## Chapter 1: RDD<a name="Chapter1"></a>

RDD: RDD is a Distribute, immutable, fault-tolerant(The RDD itself contains all the dependency information to recalculate each partition), parallel data structure that lets users to:
	1. Persist intermediate results in memory
	2. control their partitioning to optimize data placements
	3. And manipulate them using rich set of operations. 

Spark offers 3 types of Memory Management for Data. 
	
	 * In memory as deserialized java objects: The faster, but less efficient
    * As serialized data: Converts objects into streams of bytes before sending them to the network. Adds overhead 
    in deserializing the object before using it, more CPU intensive and memory efficient.   
    * On disk: When the RDD is too large to be stored in memory we can use this type, it is the slowest, but more 
    resilient to failures. Sometimes there is no other choice if the RDD is too big.