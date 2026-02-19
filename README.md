# Difference-Arrays-ArrayLists

## Overview
This project demonstrates the differences between **Arrays** and **ArrayLists** in Java.  
Arrays are fixed-size data structures, while ArrayLists are dynamic and part of the Java Collections Framework.  

## Arrays
- Fixed size (cannot grow or shrink).
- Stores elements of the same type.
- Fast access via indices.
- Syntax example: `int[] arr = new int[5];`

## ArrayLists
- Dynamic size (can grow or shrink).
- Stores objects (primitives must be wrapped, e.g., `Integer`).
- Provides utility methods like `add()`, `remove()`, `size()`.
- Syntax example: `ArrayList<Integer> list = new ArrayList<>();`

## Conceptual Differences

| Feature       | Array | ArrayList |
|---------------|-------|-----------|
| Size          | Fixed | Dynamic   |
| Data Type     | Primitives & Objects | Objects only (primitives via wrappers) |
| Performance   | Faster direct access | Slight overhead due to resizing |
| Flexibility   | Limited | High, with many utility methods |

## Example Code

The following program demonstrates the differences:

```java
import java.util.ArrayList;

public class DifferenceArraysArrayLists {
    public static void main(String[] args) {
        // Arrays: fixed size
        int[] numbersArray = new int[5];
        numbersArray[0] = 10;
        numbersArray[1] = 20;
        numbersArray[2] = 30;
        // numbersArray[5] = 60; // ERROR: ArrayIndexOutOfBounds

        System.out.println("Array elements:");
        for (int num : numbersArray) {
            System.out.println(num);
        }

        // ArrayList: dynamic size
        ArrayList<Integer> numbersList = new ArrayList<>();
        numbersList.add(10);
        numbersList.add(20);
        numbersList.add(30);
        numbersList.add(40);
        numbersList.add(50);
        numbersList.add(60); // No error, list expands automatically

        System.out.println("\nArrayList elements:");
        for (int num : numbersList) {
            System.out.println(num);
        }

        // Demonstrating flexibility
        numbersList.remove(2); // Removes element at index 2
        System.out.println("\nArrayList after removing index 2:");
        for (int num : numbersList) {
            System.out.println(num);
        }
    }
}
