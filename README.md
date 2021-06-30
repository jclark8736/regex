# Title (replace with your title)

Introductory paragraph (replace this with your text)

Regular expressions are pieces of code which evaluate a string for certain characters, or patterns. Regular expressions are denoted in two different ways.
They can be placed inside double slashes var example = /example/, or they can be denoted by var example = new Regexp('example').
The regular expression example in this case would search through a string for text containing the word example without any characters between it. More complicated patterns and conditions can be screened for by using different methods with regular expressions, and only the most basic regex searches for exact matches.


## Summary
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` is a regular expression that validates that a string contains at least a possibly valid email address. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components
Regular expressions rely on certain defined characters in order to search for patterns within strings. . is used as a wildcard so that the regular expression validating l.tter would validate litter, letter, and latter.




### Anchors
Regex anchors are used to define the position where the match needs to be made. They are used to define where in the parsed string the matching string must be found.

^ matches leading characters within a string. For example, ^lead will match leaderboard, leader, or leaded, but not unleaded, since unleaded has the characters in lead preceded by un.

$ indicates that the matching string must precede it, so to reverse the previous example, (ate$) could return potentiate, calculate, defenestrate, but would not return defenestrated, potentiated, or calculated because the matching set must be at the end of the string.

### Quantifiers
Quantifiers are used to define the limits of the characters searched for by the regular expression. For example '[a-z0-9_]{5,8}' would return a set containing any lowercase letters from a-z that is at minimum five characters long and at maximum 8 characters long.If two numbers are present within the curly brackets, the first number given is the minimum, while the second is the maximum, and this is the typical usage. If only one number is present, the regular expression will only return exact numerical matches, for example {8} would only return strings that are exactly 8 characters long.

There are other modifiers that can be used within quantifiers, such as * which indicates a match if there are 0 or more of the preceding matches, + which looks for one or more, and ? which looks for one or null matches.

### Grouping Constructs
() parentheses are used to group together expressions while searching through the string for example (page[0-9]) would return page1, page2, etc validating both the page and the [0-9] together. 

In addition, (cat):(dog) will seek to match both of the expressions that have been grouped together. So, catdog would be returned, as would dogcat, but catfish would not since it does not satisfy both conditions.




### Bracket Expressions

[] Square brackets will search for a string within a range defined by the square brackets. For example [a-zA-Z] is a defined range that will match characters containing any letter from a-z.

### Character Classes



### The OR Operator
| a pipe is an OR operator that can be used, for example to find (^dog) | (^cat) . This query would return either dog or cat if either is present when parsing through a string.

### Flags


### Character Escapes
\ or backslash is used to define a character escape. Character escapes can be used to search for characters such as $ or . for their string value rather than using them in the regular expression itself. This is necessary because these characters are operators within a regular expression so they must be specifically preceded by a backslash in order to search for them in a string.


## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
