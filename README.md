# Custom Hash Table in C

A high-performance, lightweight hash table implementation built entirely from scratch in C. Designed for efficient key-value lookups, explicit memory control, and robust collision handling.

## Features

- **Separate Chaining:** Resolves collisions cleanly using dynamic linked lists.
- **Explicit Memory Management:** Custom allocation and deallocation handling to prevent memory leaks.
- **Generic Key-Value Architecture:** Built around a modular `ht_item` data structure.

---

## Architecture

At its core, the hash table relies on an array of item pointers mapped via a deterministic hash function:

```c
typedef struct {
    char* key;
    char* value;
} ht_item;