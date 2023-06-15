# Challenge 17 Regular Expressions Tutorial

The intention of this gist is to provide an overview of regular expressions and their usage. Regular expressions, also known as Regex, are employed when attempting to find specific patterns of characters within a string. They are particularly useful for extracting information from code or performing validation tasks. To illustrate this, the tutorial will use a code snippet that demonstrates how to match an email address. The tutorial will cover the various components of regular expressions.

## Summary

The following code will be used throughout the tutorial to give specific examples for how the components of regex can be used. The following code can be used for matching emails. One use for this code is that it can be used to validate to make sure that an email follows the correct format. 

Matching Email-

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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
- [Author](#Author)

## Regex Components

### Anchors

The anchor is what starts and ends the regular expression. 
In the matching email code, 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, 

the anchors are the `^` and the `$`. This code specifically is saying that we are looking for something that starts with 

`^([a-z0-9_\.-]+)` 

we will define what everything inside the parentheses later in this tutorial, but what the anchor means is that if we are to find a match it has follow those initial guidelines. It also has to end with 

`.([a-z\.]{2,6})$`.

So, it must start and end with the given parameters within the code. If it does not, then it is not a match.

Below you will find the Two Main Types of Anchors:

1. Start Anchor ^: This asserts that the pattern must match the start of the string.
2. End Anchor $: This asserts that the pattern must match the end of the string.

### Quantifiers

A quantifier is used to determine how many times a specific character or group of characters needs to be present in order to have a match. Quantifiers are placed after a character, character class or group, in order to determine the minimum and maximum number of times preceeding patterns should occur.  For instance, if we used the following code in our regex, `xyz+` then this will match any string xy followed by at least one z. So, if we look at our code for matching the email:

`([a-z0-9_\.-]+)` 

this will match any string that contains a-z, 0-9, _, ., or -. The quantifier `+` means that it has to contain at least one of this in order to have a match. 

### OR Operator

It is not present in the code for the given matching email code, but in order to talk about the OR Operator, we will look at the following code for matching a hex code. 

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

This is a regex for matching a hex code that uses the OR Operator. 
What this will do is it will match where it starts with the `#` and that has to come first followed by one of the following:

`[a-f0-9]{6}` which will match a 6 character long string that contains a combination of a-f letters and 0-9 numbers. 

`|` OR Operator

`[a-f0-9]{3}` it will match a 3 character long string that contains a combination of a-f letters and 0-9 numbers. 

### Character Classes
The given code for matching an email address includes the \d pattern, which will specifically match a single alphabetic character (a-z) after the @ sign. Its purpose is to ensure that only letters are matched after the @ in the email address, excluding numbers or special characters.

### Flags
A regex flag is not used in the matching email code that is being used for this tutorial. A regular expression typically comes in the form:

`/regex/` 

Where the slashes denote where the regular expresssion starts and ends. A flag can be used after the slash to give more guidelines for our matching. The flags are:

* g which stands for "global" which will allow for matching all the instances within a string that follow the matching guidelines set in the regular expression.
* m which stands for "multiline" which will search line by line rather than searching through a string as a whole. 
* i which stands for "insensitive" will make the 
regular expression case-insensitive, so capitals and lower-case letters will not deture the matching. 
### Grouping and Capturing
Contininuing with the code for matching an email:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

We can talk about grouping and capturing.

`([a-z0-9_\.-]+)` is the first group that appears in our regex. This must be true before moving on to "match" the next part of the code. 
`([\da-z\.-]+)` is the second group that appears in our regex. `([a-z\.]{2,6})` is the third group that appears in our regex. 

When matching, we have to make sure we are following the guidelines of the group before moving on to the next group. 
### Bracket Expressions
Moving on to the email matching code:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Let's discuss grouping and capturing.

[a-z0-9_\.-]

This denotes the criteria for matching within the group. In this particular code snippet, it allows for letters from a to z, numbers from 0 to 9, an underscore, a hyphen, or a period.

The period is treated as an escaped character, requiring a backslash to match it.

### Greedy and Lazy Match

The provided code for email matching does not include a greedy or lazy match.

### Boundaries

If in a string, we are looking for for specific words. Boundaries are not used in the given matching an email code. 

### Back-references

Back-references are not included in the given code. 

### Look-ahead and Look-behind


The given code for matching an email does not employ look-ahead or look-behind techniques, which would require matching in a specific order.

## Author

This tutorial was created by Alex Nanut.

Contact me:

[GitHub](https://github.com/AlexNanut))
