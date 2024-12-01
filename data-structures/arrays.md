## ARRAYS
### Arrays in Java are ordered collections of elements, each identified by an index. These elements can be of any data type, including integers, characters, or even custom objects. To declare an array in Java, you specify the data type of its elements, followed by square brackets [].
### Concepts
- Static arrays
  - The statics arrays can be 1D, 2D or 3D and beyond
- Dynamic arrays
  - Unlike traditional arrays with fixed sizes, dynamic arrays, represented by the ***ArrayList class***, can grow or shrink as needed. This flexibility makes them a popular choice for many Java applications.
- Common operations
  - Accessing Elements: To access an element in an array, you use the index corresponding to its position. Remember that array indices start at 0. For instance, to access the first element in a 1D array, you would use index 0.
  - Modifying Elements: Arrays are mutable, meaning you can change the values of their elements after declaration. This allows you to update data as needed.
  - Iterating Through Arrays: Using loops, such as for or while, you can iterate through the elements of an array, making it easy to perform repetitive tasks.
- Advanced Array Operations
  - Searching and Sorting: Java provides efficient algorithms for searching and sorting arrays. For example, you can use the Arrays.sort() method to sort an array in ascending order.
  - Copying Arrays: You can create a copy of an array using various methods, ensuring that you don’t modify the original array inadvertently.
  - Transforming an Array into a List: Arrays.asList(anArray). Unfortunately, this method comes with some drawbacks:
    - It’s not possible to use an array of primitive types
    - We can’t add or remove elements from the created list, as it’ll throw an UnsupportedOperationException
  - From an Array to a Stream: Stream<String> aStream = Arrays.stream(anArray);
  - Sorting Arrays: There are overloadings to sort:
    - Primitive type arrays: which are sorted in ascending order
      - Arrays.sort(elements);
    - Object arrays (those Object must implement the Comparable interface): which are sorted according to the natural order (relying on the compareTo method from Comparable)
    - Generic arrays: which are sorted according to a given Comparator
      - Arrays.sort( strArray, Comparator.comparing(String::toString).reversed() );
    - The algorithms behind the sort method are quick sort and merge sort for primitive and other arrays, respectively
  - Searching in an Array, this is for a sorted array:
    - Arrays.binarySearch(anArray, 4)
  - Concatenating Arrays
    - Arrays.setAll(resultArray, i -> (i < anArray.length ? anArray[i] : anotherArray[i - anArray.length]));
- Best Practices for Using Arrays in Java
  - Use Enhanced For Loops, the foreach loop is an option when:
    - we don’t need to modify the array (putting another value in an element won’t modify the element in the array)
    - we don’t need the indices to do something else
  - Declare Arrays with Initial Values
  - Consider ArrayList for Dynamic Sizing
  - Use Built-in Methods
  - Handle Exceptions


  - https://www.geeksforgeeks.org/java-array-programs/
  - https://ioflood.com/blog/array-java/
  - https://www.geeksforgeeks.org/quizzes/java-quiz/arrays-gq/
