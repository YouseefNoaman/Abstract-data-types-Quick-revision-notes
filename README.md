# Abstract data types Quick revision notes
This is made to revise and remember the Abstract data types concepts easily


**Abstract data types**

* because the data types are abstract, it doesn't dictate how they are organized
* it means also the user dictates how the operations are performed
* abstract data types are usually are an interface

List in JAVA:
  + good for random data access
  + good for iterating over the items in it
  - bad for inserting items later in the middle, better at inserting at the end or the start
  - bad for deletions or removals
  - bad for searching for a specific item
  
Linked list in JAVA:
  + you need constant-time insertions/deletions from the list (such as in real-time computing where time predictability is absolutely critical)
  + good if the size of the data is unknown
  + you want to be able to insert items in the middle of the list (such as a priority queue)
  - bad for the random access
  - needs a lot of memory, because each node = value + pointer to the next element in the list
  - very slow while iterating
  - bad if the start of the iterating is from the back
  
Double linked list in JAVA:
  + solves the bad random access time of the single linked list
  + solves the traverse from the end to the front
  - needs more steps to remove or to add elements
  - needs larger memory than single linked list, because each node = value + pointer to the next element in the list + pointer to the previous element
  
  
  Stacks:
     LIFO (last in first out)
    
    * available operations:
        push: adds an element to the top of the stack
        pop: removes an item from the top of the stack
        peek: gets the element from the top of the stack
    Generally has a complexity of O(1) while doing anything, but O(n) if the end of the array is reached and needs to be resized
    
Queues:
     FIFO (first in first out)
   
    * available operations:
      
      add(enqueue): adds an item to the end of the queue
      
      remove(dequeue): removes an item from the end of the queue
    Generally has a complexity of O(1), but O(n) when resizing
   
Hashtables:

  + provides access to the data through keys
  + a key doesn't have to be an integer
  + it consists of key/value pairs
  + no need for the data types to match
  + optimized for the retrieval if you have the key
  * associative array is a type of the hashtable
  + maps any data type to an integer key
  * based on how good is the hashing algorithm, there must be a collision eventually
    a collision is when 2 different values get hashed and produce the same hash value
  * solving the collision will be by open addressing (closed hashing):
    it is a method used to solve collisions which has methods like: 
      linear probing: if there is a collision, increase the hash key by 1 and rehash, each increment is called a probe, so less probes is preferablle
  * An important metric is the LOAD FACTOR: it means number of items / size of the array (or linked list)
      it is basically used to decide when to resize the hash table, high load factor means a collision will happen, a small load factor means that the table is almost empty, so there is a waste of memory.
      
        
        
        
