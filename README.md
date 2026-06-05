# Java Data Structure: Arrays vs. ArrayLists

A Java reference guide comparing arrays and ArrayLists, written as part of M.S. Computer Science coursework. Includes a side-by-side code demonstration covering declaration, element access, resizing, removal, and type flexibility.

## Overview

Arrays and ArrayLists are both used to store collections of elements in Java, but they differ significantly in flexibility, performance, and use case. This repo breaks down those differences with working code examples.

## Arrays

An array is a fixed-size collection of elements of the same data type. it offers fast, direct access via index and is memory-efficient due to contiguous memory allocation.

**Key Characteristics:**
- Size must be declared at creation and cannot change
- Elements accessed directly by index: `arr[0]`
- No built-in methods for resizing, searching, or inserting - these must be handled manually
- Best for performance-critical, static-size use cases

```java
int[] intArray = new int[5];
intArray[0] = 10;
intArray[1] = 20;
System.out.println("Element at index 1: " + intArray[1]);  // Output: 20
System.out.println("Size: " + intArray.length);            // Output: 5
```

## ArrayLists

An ArrayList is part of Java's Collection Framework and provides a dynamic, flexible alternative to arrays. It automatically resizes as elements are added or removed.

**Key Characteristics:**
- No need to specify size at declaration - grows and shrinks dynamically
- Rich set of built-in methods: `add()`, `remove()`, `get()`, `size()`
- Works with generics to enforce type safety
- Best for scenarios requiring dynamic sizing and frequent element manipulation

```java
ArrayList<Integer> intList = new ArrayList<>();
intList.add(10);
intList.add(20);
System.out.println("Element at index 1: " + intList.get(1));  // Output: 20
System.out.println("Size: " + intList.size());                // Output: 2
```

## Side-by-Side Comparison

| Feature | Array | ArrayList |
|---------|-------|-----------|
| Size | Fixed at declaration | Dynamic |
| Syntax | `int[] arr = new int[5]` | `ArrayList<Integer> list = new ArrayList<>()` |
| Access | `arr[i]` | `list.get(i)` |
| Add element | Manual index assignment | `list.add(element)` |
| Remove element | Manual index shift | `list.remove(index)` |
| Resize | Not possible | Automatic |
| Type flexibility | Primitive or single type | Objects and generics |
| Performance | Faster for fixed data | Slight overhead from resizing |

## When to Use Each

Use an **array** when the size of your data is known and won't change, and performance is a priority (e.g. storing fixed senos readings, pixel data, or lookup tables).

Use an **ArrayList** when you need to add or remove elements dynamically and prefer the convenience of built-in methods (e.g. building a to-do list, storing search results, or managing user input).

## Running the Code

1. Clone the repository
2. Open `DifferenceArraysArrayLists.java` in any Java IDE or editor
3. Compile and run:

```bash
javac DifferenceArraysArrayLists.java
java DifferenceArraysArrayLists.java
```

## Tech

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoCOlor=white)
