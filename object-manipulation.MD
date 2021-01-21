# Object Manipulation

#### The most significant lesson I have learned is how to manipulate information.  For the most part, information will come back in two different forms; either as an object, or as an array.  In this article, I will discuss how to manipulate an object.  

### **Creating objects.**
#### In javascript, object are created by using curly braces {} and are a set of keys and values.  The key is listed on the left side of the colon, and the value on the right.  Take for example a class of students.  Each student inside of the class has their own unique characteristics, but are still part of the same class.  Given that, we can create objects of students and this is what one could look like.  
  ```
    students : {
       {
        name: Carl,
        age: 32,
        hairColor: 'brown',
        eyeColor: 'blue'
      }
      {
        name: Tammy,
        age: 35,
        hairColor: 'black',
        eyeColor: 'brown'
      }
      { 
        name: Sam
        age: 30,
        hairColor: 'red',
        eyeColor: 'green' 
      }
      }
  ```
  Each of these students have the same keys; age, hairColor, and eyeColor.  However their values are different.  If we wanted to access the hair color of Sam, we could use dot notation to access the information.  This would look like 
  ```
  students.Sam.hairColor 
  ```
The expected return should be 'red'.  We can also use bracket notation to access the same information.  
```
students[Sam][hairColor]
```
The expected return should be 'red' as well.  From what I can understand, there does not seem to be a difference in efficiency between the two, and its all a matter of personal preference.  

### Looping Through
#### Accessing objects with dot or bracket notation is great, however this will usually only return one value in an object.  Most of the time, when developers are manipulating data, we are looping through information, searching for values that match, and returning those values.  When accessing objects we can loop through them by using the following syntax;
```
for (variable in object)
```
If we wer to use the syntax to loop over the object of students we could use the following;
```
for (names in students) 
```
This should return all of the key value pairs in the object. 

#### If we just wanted to access the keys of the students object we can use the following syntax;
```
Object.keys(students)
```
The expected return from this object will now be an array and its shape would look like the following;
```
[name, age, hairColor, eyeColor],
[name, age, hairColor, eyecolor],
[name, age, hairColor, eyeColor]
```
#### If we wanted to loop through the values of the object, we could use the following;
```
Object.values(students)
```
The return would look something like this;
```
[Carl, 32, 'brown', 'blue'],
[Tammy, 35, 'black, 'brown],
[Sam, 30, 'red', 'green']
```
#### If we wanted to loop through the student object and get both the key and the value we can use the following to grab all of the ages for the students;
```
for ( const [age, number] of entries)
```
#### This would be expected to return the following;
```
[age 32]
[age 35]
[age 30]
```
#### In closing, objects are very powerful ways to store data, but they are not as easy to manipulate as arrays.  However, by using the Object.keys() and more, the big O notation will be greatly reduced. 