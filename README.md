# HashTable
Implementation of chained hash table using C

#This is a projec of a data structure. This project is done by me and my fellow project member. Using C we created the hash table. We used array of a linked list (singly linked list). 

#What is hashing? 
Hashing is a technique or process of mapping keys, values into the hash table by using a hash function. It is done for faster access to element. The efficiency of mapping depends on the efficiency of the hash function used. In a hash table, data is stored in an array format, where each data value has its own unique index value. Access of data becomes very fast if we know the index of the desired data.
Let a hash function H(x) maps the value x at the index x%10 in an array. For example if the list of values is [11, 12, 13, 14, 15] it will stored at position {1, 2, 3, 4, 5} in the array or hash table. 

#Basic operations of Hashing:
1. Insert
2. Search
3. Delete 
4. Display Elements

#We used array to store the inserted keyvalues to work with the indexes. We can see that whenever we insert a data to the hash table using array, one unique index can have more than one data to insert. Then we can end up with collision. We want to minimize the collision not want to remove the collision. To remove the collision we used Open Hashing which is also known as chaining. 

#There are 2 type to handle collision: 
1. Open hashing (Closed Addressing)
2. Closed Hashing (Opened Addressing)

#In open hashing is chaining method to handle the collision. And in the closed hashing there ar 3 types.
#The 3 types are:
1. Linear Probing
2. Quadratic Probing
3. DOuble Hashing

#Using the chaining method to minimize the collison also handle the collision. This creates a chain to a index whenever it has more than one data (inserted and then pointing the next node NULL)

#At first we declared a struct node having some data and key. Based on which the search is to be conducted in a hash table.

![HashType](https://user-images.githubusercontent.com/68398397/120454403-a9312800-c3b5-11eb-87ef-763125af6b7e.png)

#The hash method(using divisor method) to complete the hash code of the key and the value item.

![HashMethod](https://user-images.githubusercontent.com/68398397/120454570-d1b92200-c3b5-11eb-930b-1e11611174b3.png)


#Initially we are passing NULL to the indexes while using this method.

![HashInitial](https://user-images.githubusercontent.com/68398397/120455554-aedb3d80-c3b6-11eb-990e-cf3104525156.png)


#Whenever an element is to be inserted, computed the hash code of the key passed and locate the index using that hash code as an index in the array. 

![HashInsert](https://user-images.githubusercontent.com/68398397/120455614-bc90c300-c3b6-11eb-9629-eabd87906f8f.png)


#Whenever an element is to be searched, compute the hash code of the key passed and locate the element using that hash code as index in the array. 

![HashSearch](https://user-images.githubusercontent.com/68398397/120455647-c4506780-c3b6-11eb-8b08-7379d7f7d9dc.png)


#Whenever an element is to be deleted, compute the hash code of the key passed and locate the index using that hash code as an index in the array.

![HashDelete](https://user-images.githubusercontent.com/68398397/120455745-d7633780-c3b6-11eb-87c7-64ab606ee37e.png)


#Whenever print function is called it will show the data’s in the hash table using the array indexes to allocate the data. 

![HashPrint](https://user-images.githubusercontent.com/68398397/120455796-e21dcc80-c3b6-11eb-916d-107f0feb6b1f.png)


#Runtime Case in Chained Hash Table

#Inserting into the hash table

![runtime insert](https://user-images.githubusercontent.com/68398397/120455844-ec3fcb00-c3b6-11eb-8330-f7898f1cbbdf.png)


#Searching operation in runtime in chained hash table

![Runtime Search In Hash Table](https://user-images.githubusercontent.com/68398397/120455893-f3ff6f80-c3b6-11eb-8ccd-d7250a6985b8.png)


#Deleting data from the chained hash table

![Runtime Delete](https://user-images.githubusercontent.com/68398397/120455932-fbbf1400-c3b6-11eb-98c2-b2ba81e336f2.png)


#Printing Data’s present in the chained Hash Table

![Runtime Values in Hash Table](https://user-images.githubusercontent.com/68398397/120455985-05e11280-c3b7-11eb-8ee5-56440ea0308a.png)



#Efficiency Of A Hash Table
The efficiency of our hash table depends on several factors. In the worst case run-time performance occurs if every item inserted into the table hash the same hash key. Everything will then be stored in a single linked list. With n items, the find operation will require O(n) steps. 
Fortunately, if the items that we insert are somewhat random, the probability that all of them will hash to the same key is highly unlikely. In contrast, the best-case run-time performance occurs if every item inserted into the table has a different hash key. This means that there will be no collisions, so the find operation will require constant, or O(1), steps because the target will always be the first node in the linked list. 
