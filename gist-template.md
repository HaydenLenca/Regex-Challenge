# Regex Tutorial: Matching a Email

Regex is a regular expression which uses letters, symbols and numbers to match areas of interest.
It is one of the easier things to learn and use while programming while being useful.


## Summary

  In this tutorial I will be walking through the deconstruction of the email regex expression.
With regex you can use it to match many things from emails, phone numbers, urls and more.
I will show a basic email match with this ```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/```
expression. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
  ```^``` caret checks the matching character is the start of the input you are searching for.
In the expression it is used to start of the email.

  ```$``` dollar checks the matching character is the end of the input you are searching for. 
In the expression it is used to end the email.

### Quantifiers
  With quantifiers you are setting how may times it will match. When using the class ```[a-z]``` 
  tou can add a quantifier to set how many times it occurs. Adding a ```+``` to the class 
  ```[a-z]+``` it will know there should be at least one or more letters.

  ```?``` 0 or 1 time
  ```+``` 1 or more times
  After the first two classes that were searched the plus was used to show that there needs to
  be something there but can be repeat.
  ```*``` 0 or more times 
  ```{x}``` x times 
  ```{x,}``` x or more times
  ```{x,y}``` at least x times and less then y times 
  This expression was used to specify that there will be at least 2 characters an les than 6.
  
### Character Classes
  With classes you can be more specific with what you need. When using letters you can search in 
  brackets for specifics or with ```\``` and a letter to have a larger field. With the ```\```
  most lower case letters mean all once you use a capital it will be everything except.

  ```[abc]``` all specifies a, b or c
  ```[a-z]``` letters from a to z
  ```[A-Z]``` capital letters from A to Z
  ```[0-9]``` from 0 to 9
  ```[\.-]``` specific symbols
  When using symbols you will need the ```\``` to indicate it is used different because symbols are 
  used as classes

Example of using ```\```
  ```\d``` matches digits 
  ```\D``` matches everything that is not a digit

### Grouping and Capturing
  As grouping is find the different letters, numbers and symbols with how many they can occur. I used 
  this with finding the three different parts of the email. With the @ and . not changing in the email
  I grouped the other parts together. 

  ```()``` parentheses are used for grouping the characters 
  In the expression three parts are grouped. the first ```([a-z0-9_\.-]+)``` second  ```([\da-z\.-]+)```
  third ```([a-z\.]{2,6})```.

### Bracket Expressions
  Bracket expressions are similar to grouping but at a smaller scale. With brackets you can specify
  the characters you are matching like ```[bgz]``` will only match b, g and z.

### Greedy and Lazy Match
    Here it will be explained a little about greedy and lazy matches. With greedy quantifiers it
  will match as much as possible. Then lazy quantifiers will stop matching as soon as it finds what 
  it is looking for.

### Boundaries
  ```^``` the carrot is the first boundary with starting the input, meaning nothing will come 
    before it.

  ```$``` the money sign is the second boundary with ending the input, so there will be nothing 
    after.

  ```\b``` is a word boundary, meaning it can be added to the beginning of a word to stop any character 
  before the word. Or it can be placed after to stop anything preceding the word you search.

  ```\B``` is not-a-word-boundary, with this one it can be used the same way but instead of words it will 
  be used with numbers or character. 


## Author

Hayden Lenca 

[Github](https://github.com/HaydenLenca)

[Github Regex-Challenge](https://github.com/HaydenLenca/Regex-Challenge)