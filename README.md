# Simple Regex Guide

This document will is a brief explanation of regex and dives into a specific example. By the end of the article you should have a decent understanding of some common and useful regex syntax.

## Summary

 Email 
```js
var Regex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
```
For this guide well walk through everything going on in the statement above to help you gain a better understanding of how regex can be used.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Character Escapes](#character-escapes)


### Anchors
|Anchors | Description|
|--------- |------------|
|    ^     | The string being compared to has whatever comes after the component at the beginning |
| $ | Similar to the above symbol this symbol indicated that the string being compared to ends with the characters defined before the $ |

### Quantifiers

|Quantifiers | Description|
|--------- |------------|
|  + | Indicates that we are looking to match the given pattern at least one time|
| {x,y} or {x} | The {x,y} indicates the its looking to match the pattern at least x times or at most y times, in the second example {x} it has to match exactly x times| 

### Grouping Constructs

Grouping is done using (), each set of instructions inside the parentheses is called a sub-expression. 

### Bracket Expressions

|Brackets | Description|
|--------- |------------|
|    []     | anything in square brackets represents ranges of characters looking to be matched |


### Character Classes

Character classes can be used to define sets of characters similar to bracket notation, an example would be '\w' is equivalent to [a-Z0-9_].
Another example would be '\d' which would be equivalent to [0-9].

### Flags

For flags the 'g' would indicate to search globally in the given string.
Another flag would be 'i' meaning that the regex is not case sensitive.

### Character Escapes

To escape a character that otherwise would have meaning in regex such as a $ you would include a backslash prior to then tell the computer to read it as a symbol with no significance. 

## Putting it All Together

```js
var Regex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;
```
So to combine all of the qualities of regex explained above and how they apply to this statement;
The fist portion 
```js
^([a-z0-9_\.-]+)
```
Means to contain any character a-z numbers 0-9 and _ at least one time.
```js
([\da-z\.-]+)
```
This next statement means  any numeral digit 0-9 or values a-z and a '.' at least once
```js
([a-z\.]{2,6})$
```
This final statement is looking for any values a-z and '.' to occur at least 2 times at most 6
## Author

Written By [Matt Fiaschetti](https://github.com/fiaschettima)