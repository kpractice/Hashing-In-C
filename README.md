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
Collision handling implementation in C is available in hash_collision_handling_sep_chain.c file <br>

What is Hash Collision? <br>

Lets assume the hash function is defined as: <br>

#define TABLE_SIZE 1013 //Prime Number

int getHash(char *word)
{
    while(*word != '\0')
    {
        hash += (word[i]-'a');
    }
    
    return hash%TABLE_SIZE
}

Input strings are: “gpq”, “kon” <br>

Hash value for “gpq” = 37 <br>
Hash value for “kon” = 37 <br>
 
Getting same hash value for two different input values is called as collision. <br>

How to avoid collision? <br>
Come up with a very good hash function where in it always returns unique hash value for each input. In practice, for millions of input values, it is not feasible. <br>
Hence there should be a strategy to accommodate collisions. <br>

Two methods for handling collisions: Separate Chaining and Open Addressing. <br>

Separate Chaining: <br>
Maintains an array list for all hash values. <br>
For hash key of ‘0’: 2 elements are associated: 12, 15 <br>
For the key 2: 1 element is associated: 31 <br>
For the key 6: 3 elements are associated: 34, 45, 46 <br>

Whenever a new element is received, calculate the hash <br>
If the hash already exists in the list, append the element to the linked list [either at front or back] <br>
If hash doesn’t exist, insert the hash and link with the element <br>

￼
