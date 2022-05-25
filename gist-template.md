# Tutorial - Matching a URL using regular expressions (ReGex).
RegEx, or a regular expression, is defined as a pattern of characters that are utilized to validate chatarcter combinations. This tutorial will take a commonly used regex pattern used in programming; matching a URL; and break it down to explain what it does and how it does it.

## Summary
The URL matching regex is:

### Example
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

### Explanation
This regular expressions determines whether or not the input is a valid URL.  This regex can be used in a variety of ways; but most obvious is URL data validation.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Look-ahead and Look-behind](#sources)

## Regex Components

### Anchors
Anchors of a regular expression are the symbols that exist at the beginning and the end of a string.  The opening anchor is the symbol ^ at the beginning and the closing anchor is the $ at the end of the string. 

When used alone, the ^ anchor matches any string that begins with the characters that follow the anchor and the $ matches any string that ends with the characters that precede it. By putting the regex between these two described anchors. we are asking the function to match exactly what it begins and what it ends with.  As URL follow a pattern or the same beginning and end; this is a useful expression in validation.

### Quantifiers
Quantifiers communicate to the regex engine that it must match the quantity of the character or expression to its left. The following are the quantifiers that are used in this regex expression:

  ?, +, *, {n}, {n, }, {n,m}

In the URL matching regex they are used in the following places:

    https?          Matches: 'https', 'http'
    [\da-z\.-]+     Matches:  A single digit, group of letters (a-z), dot (.)or hyphen (-) 1 or more times
    [a-z\.]{2,6}    Matches: 2 to 6 copies of the sequence [a-z\.]
    [\/\w \.-]*     Matches:  '/', '.', '-', 'www', '//'

### OR Operator
The URL matching regex uses [] as the main OR operator.  The expression will look for any matches of any character or character classes within the brackets.

An example for the URL matching regex:

    [\da-z\.-]     Matches: Any digits (\d) OR any characters between a and z (a-z) OR any '.' (\.) OR any '-' (-).

### Character Classes
Character Classes ensure that a given sequence of characters matches a larger set of characters.

    [a-z]          Matches: lowercase alphabetic characters between a and z
    \w             Matches: a word
    \d             Matches: a single character that is a digit
    .              Matches: any character


### Grouping and Capturing
Grouping expression allows for the extraction of the characters within a given group in order to perform validation.  The text that exists between the parenthesis is consider a group. The URL matching regex has the following groups:

    (https?:\/\/)       Matches: ' ', 'https://', 'http://'
    ([\da-z\.-]+)       Matches: 'ab.c-7', 'ab'
    ([a-z\.]{2,6})      Matches: 'ab.', '.ca'
    ([\/\w \.-]*)       Matches: '/', '/ab.'

### Bracket Expressions
Bracket expressions are used between brackets. The URL matching regex has the following Bracket Expressions.

    [\da-z\.-]
    [a-z\.]
    [\/\w \.-]

### Greedy and Lazy Match
Greedy and Lazy Match qualifiers in a regular expression are used to find the greediest and laziest match defined as the following:

    Greedy              The longest match
    Lazy                The shortest match

This qualifier is used in the regex URL matching expression as follows:

    ([\da-z\.-]+)       "+" operator is defined as greedy because it allows character matching from one to an infinite amount of times.


### Sources
https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285

https://www.youtube.com/watch?v=UBVWBclqKSM

## Author
Nicole Barkley
barkleylikecharles@icloud.com

https://github.com/barkleylikecharles
