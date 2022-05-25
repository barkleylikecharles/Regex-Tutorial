# Tutorial - Matching a URL using regular expressions (ReGex).

RegEx, or a regular expression, is defined as a pattern of characters that are utilized to validate chatarcter combinations. This tutorial will take a commonly used regex pattern used in programming; matching a URL; and break it down to explain what it does and how it does it.

## Summary

The URL matching regex is
/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

This regular expressions determines whether or not the input is a valid URL.  This regex can be used in a variety of ways; but most obvious is URL data validation.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
There are two principal anchors in this regex epression; the ^ at the beginning and the $ at the end.  These complete an exact string match with the components included within the two anchors. When used alone, the ^ anchor matches any string that begins with the characters that follow the anchor and the $ matches any string that ends with the characters that precede it. By putting the regex between these two described anchors. we are asking the function to match exactly what it begins and what it ends with.  As URL follow a pattern or the same beginning and end; this is a useful expression in validation.

### Quantifiers
Quantifiers communicate to the regex engine that it must match the quantity of the character or expression to its left. The following are the quantifiers that are used in this regex expression:
  ?, +, *, {n}, {n, }, {n,m}

In the URL matching regex they are used in the following places:
    * https?          Matches 'https', 'http'
    * [\da-z\.-]+     Matches a single digit, group of letters (a-z), dot (.)or hyphen (-) 1 or more times
    * [a-z\.]{2,6}    Matches 2 to 6 copies of the sequence [a-z\.]
    * [\/\w \.-]*     Matches '/', '.', '-', 'www', '//'

### OR Operator
The URL matching regex uses [] as teh main OR operator.  The expression will look for any matches of any character or character classes within the brackets.

An example for the URL matching regex:
    [\da-z\.-]        Matches atches for any digits (\d) OR any characters between a and z (a-z) OR any '.' (\.) OR any '-' (-).

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
