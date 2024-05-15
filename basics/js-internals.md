
#### NOTES:
- In JS Everything is happens inside the Execution Context
- JS is a synchronous single-threaded language: execute once line at a time

### How JS code is Executed:
- Whenever any JavaScript code is executed an execution context is created and it is the Global Execution Context.
- Execution Context has 2 component:
    - memory component [variable environment]: variable and functions are stored in key-value pair
    - code component [thread of execution]: execute one command at a time in a ecific order

Example:
```js
var num = 2;
function do_multiplication(num, multiplier){
    return num * multiplier
}
var multiOne = do_multiplication(num, 4)
var multiTwo = do_multiplication(7, 5)
```
- In Variable Environment Phase, memory is allocated to all the variable and functions available the global scope
- In Thread of Execution Phase, code run line by line
    - num in assigned value 2
    - do_multiplication is not calling itself so move to next line
    - multiOne is calling function so a new execution context is created for the function and same thing happen, on return it give back control to the multiOne line
    - same with multiTwo

