# Assignment: Collision Resolution Techniques

## Introduction

In this assignment, you will implement and compare two common collision resolution techniques used in hash tables: **Chaining** and **Quadratic Probing**. The assignment is designed to test your understanding of how collisions are handled in hash tables and your ability to implement each method efficiently. You will also analyze how different load factors affect the performance of these techniques.


## Requirements


Implement a hash table class that supports two different collision resolution techniques:

1. **Chaining**
2. **Quadratic Probing**

Your implementation should allow for switching between the two techniques based on a flag set during initialization.




## Instructions


**Step 1 - Define a Hash Table Class**: Create a class called `HashTable` with the following methods:

- `insert(key, value)`: Inserts a key-value pair into the hash table.
- `get(key)`: Retrieves the value associated with a key.
- `delete(key)`: Deletes a key-value pair from the hash table.
- `hash_function(key)`: Returns the hash index for a given key.

**Step 2 - Collision Resolution with Chaining**:

- Use linked lists or arrays to store multiple key-value pairs in the same bucket when collisions occur.
- Implement `insert`, `get`, and `delete` using this method.

**Step 3 - Collision Resolution with Quadratic Probing**:

- In the case of a collision, search for the next available slot using quadratic probing. 
- The probe sequence should follow this formula: `h(k, i) = (h'(k) + i^2) % m`, where `i` is the number of probes.
- Implement `insert`, `get`, and `delete` using this method.

**Step 4 - Switch Between Techniques**:

- Implement a flag in the constructor that allows the user to choose between chaining and quadratic probing.
- The flag should determine which collision resolution method is used when inserting, getting, or deleting values.

**Step 5 - Handle Resizing**:

- Implement resizing functionality: when the load factor exceeds 0.75, double the size of the hash table and rehash all the elements.

**Step 6 - Analyze Performance**:
- After implementing both techniques, run a set of tests to compare their performance.
- Analyze the number of collisions, memory usage, and time complexity for both methods with various load factors.


## Testing


Use the following code to test your implementation after you have defined the class:

```python
# Test for Chaining
hash_table_chaining = HashTable(10, method="chaining")
hash_table_chaining.insert("apple", 5)
hash_table_chaining.insert("banana", 7)
hash_table_chaining.insert("cherry", 3)
print("Chaining - Get apple:", hash_table_chaining.get("apple"))  # Should return 5
print("Chaining - Get banana:", hash_table_chaining.get("banana"))  # Should return 7
hash_table_chaining.delete("apple")
print("Chaining - Get apple after deletion:", hash_table_chaining.get("apple"))  # Should return None

# Test for Quadratic Probing
hash_table_quadratic = HashTable(10, method="quadratic_probing")
hash_table_quadratic.insert("apple", 5)
hash_table_quadratic.insert("banana", 7)
hash_table_quadratic.insert("cherry", 3)
print("Quadratic Probing - Get apple:", hash_table_quadratic.get("apple"))  # Should return 5
print("Quadratic Probing - Get banana:", hash_table_quadratic.get("banana"))  # Should return 7
hash_table_quadratic.delete("apple")
print("Quadratic Probing - Get apple after deletion:", hash_table_quadratic.get("apple"))  # Should return None
```


## Conclusion

In this assignment, you implemented two collision resolution techniques: chaining and quadratic probing. You should now be familiar with how to handle hash table collisions using these techniques and understand the trade-offs between them.

