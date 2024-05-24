# Difference-Arrays-ArrayLists

### Functions of Arrays and ArrayLists in Java

#### Arrays
- **Fixed Size**: Arrays are static in size. Once you define the size of an array, it cannot be changed.
- **Type-specific**: Arrays can hold elements of a specific type (e.g., `int[]`, `String[]`).
- **Memory Allocation**: Memory for arrays is allocated at the time of declaration.
- **Access Time**: Arrays provide fast access to elements as they are indexed.

#### ArrayLists
- **Dynamic Size**: ArrayLists are dynamic. They can grow and shrink in size as needed.
- **Generic**: ArrayLists can hold objects of any type using generics (e.g., `ArrayList<Integer>`, `ArrayList<String>`).
- **Memory Management**: Memory is managed dynamically, and resizing is handled automatically.
- **Convenient Methods**: ArrayLists come with built-in methods for various operations (e.g., adding, removing, finding elements).

#### Conceptual Differences
- **Size Management**: Arrays have a fixed size, while ArrayLists can resize dynamically.
- **Type Handling**: Arrays are type-specific, but ArrayLists use generics to handle different types.
- **Performance**: Arrays are generally faster for accessing elements due to their fixed size, whereas ArrayLists offer more flexibility and convenience at the cost of some performance overhead.

### Code Example

```java
import java.util.ArrayList;

public class DifferenceArraysArrayLists {
    public static void main(String[] args) {
        // Example of Array
        // Arrays have a fixed size
        int[] array = new int[5];
        array[0] = 10;
        array[1] = 20;
        array[2] = 30;
        array[3] = 40;
        array[4] = 50;

        // Accessing array elements
        System.out.println("Array Elements:");
        for (int i = 0; i < array.length; i++) {
            System.out.println(array[i]);
        }

        // Example of ArrayList
        // ArrayLists can grow and shrink dynamically
        ArrayList<Integer> arrayList = new ArrayList<>();
        arrayList.add(10);
        arrayList.add(20);
        arrayList.add(30);
        arrayList.add(40);
        arrayList.add(50);

        // Adding an element to ArrayList
        arrayList.add(60);

        // Accessing ArrayList elements
        System.out.println("\nArrayList Elements:");
        for (int element : arrayList) {
            System.out.println(element);
        }
        
        // Demonstrating size flexibility of ArrayList
        System.out.println("\nSize of ArrayList after adding elements: " + arrayList.size());

        // Removing an element from ArrayList
        arrayList.remove(1); // Removes the element at index 1 (second element)

        // Accessing ArrayList elements after removal
        System.out.println("\nArrayList Elements after removal:");
        for (int element : arrayList) {
            System.out.println(element);
        }
        
        System.out.println("\nSize of ArrayList after removal: " + arrayList.size());
    }
}
