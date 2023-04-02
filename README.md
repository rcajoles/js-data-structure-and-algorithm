Javascript Data Structures & Algorithm
===========================

<br/>

## Big O
-------------------
`Big O`, also known as `Big O notation`, represents an algorithm's worst-case complexity. It uses algebraic terms to describe the complexity of an algorithm.


`Big O` defines the runtime required to execute an algorithm by identifying how the performance of your algorithm will change as the input size grows. But it does not tell you how fast your algorithm's runtime is.

`Big O notiation` measures the `efficiency` and `performance` of your algorithm using `time` and `space` complexity.

#### In Big O, there are six major types of complexities (time and space): ####

- $f(n)$ could be constant ($f(n)=1$)
- $f(n)$ could be linear ($f(n)=n$)
- $f(n)$ could be logarithmic time ($f(n)=$ n log n)
- $f(n)$ could be quaratic ($f(n)=n^2$)
- $f(n)$ could be exponential time ($f(n)=2^n$)
- $f(n)$ could be factorial time ($f(n)=n!$)

### Big O Complexity Chart ###
----------------------------
![Big O Chart!](https://paper-attachments.dropbox.com/s_2D428973624E7FC84C7D69D11421DE762BEA6B6F3361231FCDCAE0425D14526F_1664885448372_Untitled.drawio+17.png)

<br/>

### Time Complexity
--------------------
An algorithm's time complexity specifies how long it will take to execute an algorithm **as a function of its input size**.

How can we analyze the runtime of an algorihm as the size of the inputs increases?

<br/>

### Space Complexity
--------------------
An algorithm's space complexity specifies the total amount of space or memory required to execute an algorithm **as a function of the size of the input**.

How much additional memory do we need to allocate in order to run the code in our algorithm?

**Auxiliary space complexity** - refers to the space required by the algorithm, not including space taken up by the inputs.

#### Rules of thumb:
- Most primitives `(booleans, numbrs undefined, null)` are constant space
- Strings requre `O(n)` space (where `n` is the string length)
- Reference types are generally `O(n)`, where `n` is the length `(for arrays)` or the number of keys `(for objects)`.

#### Example:
```javascript
/* Sums all the items in an Array
 * @param arr - takes an argument of array
 * @return {number} - returns a constant value
 */
function sum(arr){           
    let total = 0;                         // total is constant space - count as 1
    for(let i = 0; i < arr.length; i++) {  // i is a constant space - count as 1
        total += arr[i];    
    }
    return total; 
}                   // Space Complexity of - O(1)

/* Doubles the value of items in an Array
 * @param arr - takes an argument of array
 * @return {array} - returns an array
 */
function double(arr) {
    let newArr = [];
    for(let i=0; i < arr.length; i++) {
        newArr.push(2* arr[i]); 
    }
    return newArr;  // space is directly proportionate to length of argument
}                   // Space Complexity of - O(n)

```

<br/>

### What is logarithm?
--------------------

$log_2(8)=3$ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ------------> &nbsp;&nbsp;&nbsp;&nbsp; $2^3=8$

$log_2(value)=e$  &nbsp;&nbsp;&nbsp;&nbsp; ------------> &nbsp;&nbsp;&nbsp;&nbsp; $2^e=value$ 

### Omit the `subscript 2` <br/>

$log$ === $log_2$  

>The logarithm of a number roughly measures the number of times you can divide that number 2 **before you get a value that's less than or equal to one**. 

<br/>

### Summary
--------------------

- To analyze the performance of an algorithm, we use Big O Notation.
- Big O Notation ca ngive us a high level understanding of the time or space complexity of an algorithm
- Big O Notation doesn't care about precision, only about general trends (linear, quaratic, contstant)
- The time or space complexity (as measured by Big O) depends only on the algorithm, not the hardware used to run the algorithm.
- Big O Notation is everywhere, so get lots of practise!
