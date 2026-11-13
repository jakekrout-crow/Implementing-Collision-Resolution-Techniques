# <Implementing-Collision-Resolution-Techniques>

# Description
This project was made as part of an assignment for a CS2000 class
This project aims to explore some different techniques to resolve overlapping insertions in hash tables by making use of both chaining and quadratic probing

# Usage
to use this code, create a new code block in assignment.ipynb and include the values and insertion method you would like to test
below are examples for both methods:

## for chaining:

hash_table_chaining = HashTable(10, method="chaining")
hash_table_chaining.insert("apple", 5)
hash_table_chaining.insert("banana", 7)
hash_table_chaining.insert("cherry", 3)

in the above example, you can also replace each string or number with a different string or number respectively

## for quadratic probing:

hash_table_quadratic = HashTable(10, method="quadratic_probing")
hash_table_quadratic.insert("apple", 5)
hash_table_quadratic.insert("banana", 7)
hash_table_quadratic.insert("cherry", 3)

in the above example, you can also replace each string or number with a different string or number respectively


# about the author:
Joan Krout wrote this code while attending atlas school and taking the CS2000 class while in the Systems Programming course track.
