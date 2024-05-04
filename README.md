# REGEX-TUTORIAL

Regular expressions are a fundamental tool for text processing and pattern matching in programming. By mastering regex, coding bootcamp students can enhance their problem-solving skills and efficiency in various projects and tasks. With practice and experimentation, you'll find regex to be an invaluable asset throughout your coding journey.

## Summary

In this explanation, I'll describe a regular expression used to validate usernames. The regex ensures that the entered username follows certain criteria such as length restrictions and allowable characters. Here's a code snippet of the regex:

## Table of Contents

- [Regex](#regex-components)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Bracket Expressions](#bracket-expressions)
- [References](#references)
- [Acceptance-Criteria](#acceptance-criteria)
- [GIST](#gist)
- [Author](#author)

## Regex Components

A regex is considered a literal, so the pattern must be wrapped in slash characters (/). If we examine the “Matching a Username” regex, you'll see that this is true:

/^[a-z0-9_-]{3,16}$/

Matching a Username

1. ^ : This caret symbol denotes the start of the string. It indicates that the username must start from the beginning of the string.
2. [a-zA-Z0-9_-] : This character class specifies the valid characters that can be used in the username. It includes:

* Lowercase letters (a-z)
* Uppercase letters (A-Z)
* Digits (0-9)
* Underscore (_) and hyphen (-)

3. {3,16} : This quantifier specifies the allowable length range for the username. It means the username must be between 3 and 16 characters long.
4. $ : This dollar sign denotes the end of the string. It indicates that the username must end at this point in the string.

### Anchors

In regular expressions, anchors are special characters used to match positions rather than actual content. They don't consume characters but instead indicate whether a match is possible at a certain position. There are two main types of anchors:

^ - The start of line anchor. It verifies if the following pattern is at the beginning of a line. For example, ^abc will match any line starting with "abc".

$ - The end of line anchor. It checks if the preceding pattern is at the end of a line. For instance, abc$ will match any line ending with "abc".

These anchors are valuable when you need to specify where in a line a match should occur.

### Quantifiers

{3,16}: This quantifier specifies the allowable length range for the username. It means the preceding character class [a-z0-9_-] must be repeated between 3 and 16 times. So, the username must contain between 3 and 16 characters composed of any combination of lowercase letters, digits, underscore, or hyphen.

### Bracket Expressions

Square brackets ([ ]) in regex denote bracket expressions or positive character groups, specifying the characters we want to match. For instance, [abc] seeks a string containing "a", "b", or "c", irrespective of string length.

A hyphen (-) between alphanumeric characters signifies a range, e.g., [a-c] and [abc] both seek the same characters.

In our username regex example:

[a-z]: Matches any lowercase letter from a to z. To include uppercase, use [a-zA-Z].
[0-9]: Matches any digit from 0 to 9.
[_-]: Matches an underscore or hyphen, both termed special characters. These non-alphanumeric characters are included by placing them after alphanumeric ranges within the brackets.
Combined as [a-z0-9_-], it matches strings containing any combination of lowercase letters, digits, underscores, or hyphens in any order. Note, the pattern doesn't require all criteria to be met; any is sufficient.

### References

https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial
https://www.regular-expressions.info/repeat.html

## Acceptance Criteria

GIVEN a regex tutorial
WHEN I open the tutorial
THEN I see a descriptive title and introductory paragraph explaining the purpose of the tutorial, a summary describing the regex featured in the tutorial, a table of contents linking to different sections that break down each component of the regex and explain what it does, and a section about the author with a link to the author’s GitHub profile
WHEN I click on the links in the table of contents
THEN I am taken to the corresponding sections of the tutorial
WHEN I read through each section of the tutorial
THEN I find a detailed explanation of what a specific component of the regex does
WHEN I reach the end of the tutorial
THEN I find a section about the author and a link to the author’s GitHub profile

## GIST

https://gist.github.com/LONZEE/39347ca2f464e0324b1c4d7e2b21b8d1.js

## Author

Github:https://github.com/LONZEE