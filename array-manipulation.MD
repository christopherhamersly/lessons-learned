# Array Manipulation

## If you have the ability to manipulate objects, you should have the ablity to manipulate arrays.  An array is a set of data, that are arranged seperated by commas and are housed inside square brackets.  Many common arrays are arrays of numbers.  You will find a variety of arrays in the world, but here are a few common examples; 
```
let numbers = [ 1, 2, 3]
let names = [ Susan, Samantha, Sarah ]
let trueOrFalse = [ true, true, false ]
```
### When dealing with arrays, there are a couple of things to remember.  Unlike objects, arrays have an index position, and a value at that index value.  Index positions in arrays start at 0 and increment by 1 for each additional value.  Take the array of true and false.  The array and index positions can be illustrated as; 
```
[ true, true, false]
   index position
--> 0 --> 1 --> 2
```
If you wanted to get the value of false from the trueOrFalse array, you would target the value at the second index position.  In code it would look like the following;
```
trueOrFalse[2];
```
The code for seeing what it would look like in the console log in javaScript would look like the following;
```
let let trueOrFalse = [ true, true, false ]

console.log(trueOrFalse[2]);
```
This would give us the expected response of false.  

### Arrays are very powerful data structures, and have a lot of built in methods in which to manipulate them.  I will be covering them in the next article, however I will cover a simple loop for this data structure.  Most of the time you are dealing with arrays, you are expected to loop over the information.  Looping is just another way to say, look over all of the information and I will tell you what I'm looking for.  Once you reach that piece of information, do something with it that I tell you.  For the majority of the time you will either use a for loop, or a while loop.  A for loop, iterates over the entire data set, and will return a value.  A while loop, will iterate over the data stopping when it reaches the information it is looking for, and returning.  Here is a typical for loop in javaScript

```
for(let i = 0; i < array.length; i++ )
```
This code block is saying; let the initial index position equal zero.  As long as the index position is less than the length of the array, keep going, and increment i (the index position).  This will return once i (the index position) equals the length of the array.  For loops are very powerful tools and when combined with other array methods, can be a great way to manipulate data.  
***
### A while loop 
Unlike a for loop, which predominately runs over an entire data set, and while loop can break out of the loop for any number of conditions.  Given the following array;
```
let string = ['the', 'big', 'red', 'dog', 'jumped', 'over', 'the', 'brown', 'log']
```

If we were given the task to check if a particular word was inside of the string, it would be more efficient to find the first time the word was found, and break out of the loop.  

Given the following code, we would have the ability to find out if 'big' was inside the string or not. 

```
while (i < string.length ) {
  if(i === 'big') {
    return 'Found it!'
  } else {
    return 'Didn't find it!'
  }
}
```

This code block would return 'Found it!'

