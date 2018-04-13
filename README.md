# Hashing-In-C

What is Hashing? <br>
Collection of keys and associated values

Keys -> Unique values in the collection <br>
Values -> Can be a single value/collection of values

Why is Hashing required? <br>
To have constant time for finding/inserting/deleting of elements

What Hashing lags at? <br>
Hash collisions -> Need to choose better hash function and adjust the table, whenever collisions happen
FindMin, FindMax, Sorting Data : Cannot work in linear time

How Hashing is represented in C? <br>
Hash table is a data structure represented with the help of linked lists/arrays
Elements in data structure:
Key,
Values,
Max Table Size [Prime Number]

<br>
Hashing implementation in C is available in hash_calculation.c file -> This doesn't handle collisions <br>
Collision handling implementation in C is available in hash_collision_handling.c file
