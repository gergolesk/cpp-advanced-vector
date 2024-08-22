
# Custom Vector Implementation

This repository contains a custom implementation of a dynamic array template class `Vector`, which mimics the functionality of `std::vector` in C++. The implementation is designed to manage raw memory and provide efficient operations for managing collections of elements.

## Overview

The project consists of two main classes:

1. **RawMemory<T>**: Handles raw memory allocation and deallocation for elements of type `T`. It does not construct or destruct elements, but merely allocates the necessary memory.
  
2. **Vector<T>**: Provides a high-level interface for managing a dynamic array of elements of type `T`. It supports various operations such as element insertion, deletion, resizing, and memory management, similar to `std::vector`.

## Features

- **Memory Management**: Efficiently manages memory allocation and deallocation using `RawMemory`.
- **Copy and Move Semantics**: Supports both copy and move semantics to ensure efficient data management and prevent unnecessary data duplication.
- **Iterators**: Provides `begin()`, `end()`, `cbegin()`, and `cend()` iterators for easy traversal of elements.
- **Capacity Management**: Includes methods like `Reserve()` to manage the capacity of the vector efficiently.
- **Element Insertion and Removal**: Methods such as `PushBack()`, `PopBack()`, `EmplaceBack()`, `Insert()`, and `Erase()` allow flexible manipulation of the elements within the vector.
- **Exception Safety**: The implementation is designed with exception safety in mind, ensuring that the vector remains in a valid state even in the presence of exceptions.

## Usage

To use this `Vector` implementation, simply include the header file in your project and use the `Vector` class as you would use `std::vector`.

```cpp
#include "Vector.h"

int main() {
    Vector<int> vec;
    vec.PushBack(10);
    vec.PushBack(20);

    for (int value : vec) {
        std::cout << value << std::endl;
    }

    return 0;
}
```

## Compilation

To compile a program using this `Vector` implementation, include the necessary header and compile as usual:

```bash
g++ -std=c++17 -o my_program main.cpp
```

## License

This project is open-source and available under the MIT License. See the `LICENSE` file for more information.
