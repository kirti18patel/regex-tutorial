# REGEX TUTORIAL for Email Matching

In this tutorial, I'm going to introduce Regular Expressions and, by describing how it works, explain some important regex concepts.

## Summary

A regular expression or Regex is a sequence of characters that specifies a search pattern. Usually such patterns are used by string-searching algorithms for "find" or "find and replace" operations on strings, or for input validation. It is a technique developed in theoretical computer science and formal language theory.

We will be walking through the following regex, explaining what each component does.

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/

This regex makes sure that the given string matches the template for an email address.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors

There are two anchors in regex often use : ^ and $

^ means that the following code must appear at the beginning of the string.
$ means that the preceding code must appear at the end of the string.

Input string should match the pattern mentioned in summary section or else its not a valid input.

Although this sounds limiting, you will see how quantifiers, grouping and bracket expressions allow a large range of variation in the given string.

### Quantifiers

Quantifiers are used to specify number of times a given character is expected to appear.

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/
Above regex uses two quantifiers, + and {2,6}.

In the expression, [a-z0-9_.-]+ means that any character matching the characters inside the brackets is expected to appear at least once, with no upper limit.

The same is true of [\da-z.-]+

[a-z.]{2,6} means that 2 to 6 characters matching those inside the brackets are expected. The numbers inside the curly braces specify the lower and upper limit of the number of characters expected.

### Character Classes

It uses special character classes use to match types of characters. 

\d is used to match any digit character.
\w is used to matching any word character.
\s is used to matching a whitespace character.
"." is used to matching any character (don't need "\").

Note : \ used to differentiate the digit class from a plain letter d.

### Grouping and Capturing

Grouping and capturing is done with ( ) in regex.

Anything within a set of parentheses is taken as a single group.

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/
Between /^ and $/, there are three distinct character groups, ([a-z0-9_.-]+), ([\da-z.-]+), and ([a-z.]{2,6}).
After simplifying, it can be expressed this way: (1)@(2).(3) => (string)@(website).(com/edu/etc) template

### Bracket Expressions

The final piece necessary to our RegEx is bracket expressions. There are three within our code:
[a-z0-9_.-], [\da-z.-], and [a-z.]

A bracket expression represents a single character.
For example, in [a-z0-9_.-], this character will be matched by any lowercase letters from a-z, any digit from 0-9, or a period.

## Author

Kirti Patel is a web developer living in Canada, author of this document. The link below is my github profile : [kirti18patel](https://github.com/kirti18patel)
