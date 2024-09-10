# Regex Tutorial

Regex are sequences of characters that define search patterns used to match, search, and manipulate text. Developers use regex to perform tasks such as validating input formats, searching for specific patterns within strings, replacing text, and splitting strings. Regex provides a concise and flexible way to handle complex text processing and validation tasks across various programming languages.

## Summary

Regex that will be described: 

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The snippet above is used to validate email addresses. I will be explaining below how each component of the snippet is used. 

## Table of Contents
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)


### Anchors 
Anchors are used to specify positions within a string. They do not match characters but rather assert where the match should occur. 
^ - asserts that the match must start at the beginning of the string 
$ - asserts that it must end at the end of string 

### Quantifiers
Quantifiers specify how many instances of a character or group are required for a match.
[a-z\.]{2,6} - ensures the top level domain has between two to six characters. 

## Grouping Constructs
Grouping constructs are used to group multiple tokens together to apply quantifiers or capture matches. 
([a-z0-9_\.-]+) and ([\da-z\.-]+) Both of these snippets are groups capturing the local part and domain of the email respectively. 

### Bracket Expressions
Bracket expressions define a set of characters, which can be matched at a given position in the string. They allow for specifying ranges and sets of characters. Bracket expressions are also used to match any single character from a defined set. 
[a-z0-9_\.-] - This snippet from the email regex matches any lowercase letter, digit, dot, or phyphen in the local part of the email. 

### Character Classes
Character calsses are predefined sets of characters that simplify regex patters. They stand for common groups of cahracters and include classes such as \d for digits, \w for word characters, \s for whitespace. They make it easier to write patterns that need to match specific types of characters. 
\d - is sued to match digits in the domain name 

### The OR Operator
The OR operator allows for matching one of serveral alternatives in a pattern. It separates different options that should be matched. An OR operator is useful for creating patterns that need to match multiple possibilities. 
Although an OR operator is not used in the email regex, you can use it match different domain patterns. 

### Flags
Flags modify the behavior of regex patterns, such as making matches case-insensitive or enabling multiline mode. They are added after the pattern and affect how the pattern is interpreted. They are useful for customizing pattern matching according to specific needs. 
Flags are not used in the email regex but it would make it case-insensitive.

### Character Escapes
Character escapes are used to match special characters or indicate that a character should be treated literally rather than having a special meaning. They are essential for matching characters that would otherwise be interpreted as regex operators. 
In the email regex, \. it's used to match the dot between the domain and the top level domain 

## Author
Alondra S. 
GitHub Link: https://github.com/Alondra1752/Regex-Tutorial

