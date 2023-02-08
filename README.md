# Parking_Ticket_Database

This is an in-memory parking ticket database. It takes in data from actual data summons (tickets) extracted from the New York City summons database for the fiscal year 2018. 

In this project, I practice:
  1. Writing data structures in C using pointers
  2. Basic memory runtime, memory allocation, and deallocation with malloc() and free()
  3. Using the valgrind to test usage of malloc() and free()
  4. Working with hash table chains and 2-D linked lists
  5. Writing code to traverse every record in a database to find a specific entry
  6. Writing code to use a hash function to find a specific entry in the database.
  
- **insertticket.c** is used to insert a ticket (summon) into the database. 
- **vehiclelookup.c** searches for a vehicle by hasing the license plate string to get the hash chain. The hash chain is searched and a pointer matched to the vehicle struct is returned if it is found.
- **sumlookup.c** searches for the vehicle that has specific summons by iteratively searching the database one hash chain at a time
- **largest.c** prints to stdout the largest number of tickets for any vehicle and the largest total fine for any  vehicle by iteratively searching the database one hashchain at a time. 
- **freetickets.c** frees up all of the memory before the program exits and deletes the database using an itereative search of the database one hash chain at a time.
- **delticket.c** deletes a specific summon via a hashtable lookup.
