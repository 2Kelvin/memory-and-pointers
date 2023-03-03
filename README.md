# Memory and Pointers

`Pointers` => **the address of a piece of data in memory.** Also called `references`

Everytime you create a variable, **the computer creates a space for it in memory.** The values assigned to these variables are then stored at those memory spaces.

Variables created inside functions are stored in a memory section called `stack`. While variables created outside functions are stored in a memory section called `globals`

Use `&` operator to find out the memory address/ location of a variable => it takes in a piece of data and tells you where it's stored

```c
int x = 11;

printf("x is stored at %p\n", &x);
```

`&x` is the address of x and `%p` is used to format addresses. The location is displayed in a hex base format.

This address is the **location where you can find the variable in memory.** An address is also called a `pointer` because `it points to a variable in memory`

Pointers make it easy for functions to **share memory** i.e. read, write & update the memory data found at that location.

**How to use pointers(references) to read & write memory data:**

- [x] Get the address of the variable (`&variableName`) e.g. **&x** and then declare a **pointer variable** to store the variable's memory address. Also, before the declaration, say what type of data is stored in the pointer variable.

        ```c
        int  xAddress = &x;
        ```

- [x]  Read the content (values) of the memory address. Use `*` operator => it takes in an address and and tells you what's stored there

        ```c
        int valueStored = *xAddress;
        ```

- [x] Change the content of an address i.e change the value stored in the address. Use the __*__ operator before the address (on the left side of the assignment) and assign it the new value

        ```c
        *xAddress = 7;
        ```

    