
Hello everyone!!!!


This is ARJUN A from BANGALORE,INDIA


This is a C++ program to resolve collision in hashing using a method called SEPARATE CHAINING.




One of the main problem in Hashing is COLLISION.

COLLISION is a condition which arises when two keys map to the same index in a hash table.
  
In order to resolve COLLISION,we should find another place to put the new key without affecting 

the old key, and still allowing for quick lookup of the new key.

The best way to do this is to use a method called SEPARATE CHAINING.

In this method,we use an array of linked lists as the hash table.

When there is a COLLISION, the colliding key can be pushed onto the linked list, thus 

preserving both values.

When searching for a key, the index is hashed and then the linked list is searched.

Deletion is as simple as deletion from a linked list.

Here ,each linked list is a chain & they are separate.So,it is called SEPARATE CHAINING.


In this program,i have created a class called "hashing"

In this class,i have declared 3 variables,4 function,1 constructor & 1 destructor. 

VARIABLES

i) bucket :- is an an array to hold linked lists for each table record of type linkedlist,which i have defined above class hash.

ii)size  :- indicates number of indexes hash table must have.

iii)num_ele :- indicates number of elements added to table.

FUNCTIONS

i)int hash_str(const char *str);
  
*the hashing algorithm used here is a DJB2 hashing algorithm.
this function hash<<5 which is same as hash*(2 to the power of 5) which means hash *32.


ii)void add(string &str)

* first,hash the string to get the index.
*second,add to "hashed"th index of bucket array.
*finally,increase number of elements i.e,num_ele by one.



iii)void remove(string &str) 
*first,hash the string to get the index.
*second,delete the record containing str, from the "hashed"th index of bucket array
*finally,decrease number of elements i.e,num_ele by one.

iv)void hasher::output()
*displays all  the elements in the hash table


CONSTRUCTOR

i)hashing(int table_size)

*first,it sets table_size to number of indexes in table i.e, size
*second,allocate "size" elements for bucket array, an array of linked lists for each table index to hold all records in that index.
*finally,initialise num_ele to 0.

DESTRUCTOR

i)~hashing()

*if bucket array memory is allocated,it is deleted from that memeory.



