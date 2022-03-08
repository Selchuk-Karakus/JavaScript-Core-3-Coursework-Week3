# Code reading

## Question 1

Take a look at the following code:

```
1    let x = 1;
2    function f1()
3    {
4        let x = 2;
5        console.log(x);
6    }
7    console.log(x);
```

Explain why line 4 and line 6 output different numbers.
## Answer 1
<!-- They are in different scopes. The 1st x variable is initialized inside the global scope and the 2nd x variable is initialized inside the local scope of the f1 function-->
## Question 2

Take a look at the following code:

```
let x = 10

function f1()
{
    console.log(x)
    let y = 20
}

console.log(f1())
console.log(y)
```

What will be the output of this code. Explain your answer in 50 words or less.
## Answer 2
<!-- The 1st console.log will output 10 and the 2nd console.log will complain that variable y is not defined.  This is because the variable y is initialized as a local variable therefore is not accessible from the global scope. -->

## Question 3

Take a look at the following code:

```
const x = 9;

function f1(val) {
  val = val + 1;
  return val;
}

f1(x);
console.log(x);

const y = { x: 9 };

function f2(val) {
  val.x = val.x + 1;
  return val;
}

f2(y);
console.log(y);
```

What will be the output of this code. Explain your answer in 50 words or less.
## Answer 2
<!-- The variable x's value is a number therefore gets passed by value to the function f1. So, the output of the console.log is still 9.  However, in the 2nd example we are passing an object to the function f2.  Objects are passed by copy of reference so the operation applied affects the original object. x is now 10 -->
