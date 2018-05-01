Javascript comes with 9 native object constructors. they are 
- Object()
- Number()
- String()
- Boolean()
- Function()
- Array()
- Date()
- Regex()
- Error()

Js is constructed with these 9 objects along with string,number and boolean primitive values. 
Along with these, there is Math. But Math is not a constructor function but you can treat it as though the object is already available. Like for ex- Math.PI.

Primitive types(aka simple values): string,number,boolean,null,undefined
These are called simple values because they dont store any other data/value other than what they store unlike objects which can have multiple properties and values.
Primitive values represent the lowest form of data & info available in javascript.

Primitive values are stored by value where as complex values(objects) are stored by reference.
Ex: 
var num1 =10;
var num2 = num1;
console.log(num1 == num2) ---> true because they are compared by value.
var num3 = new Number(10)
var num4 = num3
console.log(num1 == num3) ----> False because objects are stored by reference and here they are diff.
console.log(num3 == num4) ----> true as references are same!

string,boolean,number can be converted to object and then discarded after comparison.
null,undefined -->cannot be converted to string using null.toString()/undefined.toString() as they cannot be converted to objects.

** Dot Notations vs Bracket Notations
An object's properties can be accessed either using dot notation or using brackets.
. notation is the most commonly used notation.
[] notations is useful under following circumstances
- When the property name is stored in a variable, then the property can be accessed using the variable inside a bracket
  ```
    var obj = {fooBar:'This is foo bar'}
    var x = 'foo';
    var y = 'bar';
    var result = obj[x + y] . 
    console.log(result);   ===> returns 'This is foo bar'
  ```
  - When the property name is a javascript keyword. Using dot notation to access this property value can throw syntax error but not with [] notation.
  ```
    var obj = {'name':'example','class':'sample'}
    var result = obj[class]
    console.log(result)  ===> This returns sample.
  ```

