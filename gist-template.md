# Regex Matching a URL
Matching a URL with regex involves creating a pattern that matches the structure of a URL, which typically consists of a scheme (e.g., http, https), a domain name, a path, and optional query parameters and fragments. The goal of a URL regex pattern is to identify whether a given string matches this structure and extract the relevant components of the URL for further processing. This can be useful in a variety of contexts, such as validating user input in a web application or extracting URLs from text data for analysis.

## Summary 
The goal of a URL regex pattern is to identify whether a given string matches this structure and extract the relevant components of the URL for further processing. This can be useful in a variety of contexts, such as validating user input in a web application or extracting URLs from text data for analysis.

```regex
/^((http|https):\/\/)?([a-z0-9-]+\.)+[a-z]{2,}(\/[a-zA-Z0-9-._~:/?#[\]@!$&'()*+,;%=]*)?$/
```
This pattern matches URLs that start with "http://" or "https://", followed by a domain name consisting of one or more subdomains separated by periods, and ending with a top-level domain name consisting of two or more letters (e.g., .com, .org). The pattern also allows for an optional path and query parameters, which can contain a variety of characters.
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
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

### Anchors
To match a URL based on anchors, you can use the ^ and $ anchors to match the beginning and end of the string respectively. For example, to match a URL that starts with https and ends with .com, you can use the following regular expression:
```
^https.*\.com$
```
This regular expression will match any string that starts with https and ends with .com, regardless of what comes in between.

### Quantifiers
Quantifiers are used to match a pattern a certain number of times. Some common quantifiers are:
1. '*' - Matches the preceding character or group zero or more times
2. '+' -  Matches the preceding character or group one or more times
3.  ? - Matches the preceding character or group zero or one times
4.  {n} - Matches the preceding character or group exactly n times
5.  {n,} - Matches the preceding character or group at least n times
6.  {n,m} - Matches the preceding character or group between n and m times
For example, to match a string that contains between 3 and 5 digits, you can use the following regular expression:



### OR Operator
The OR operator | is used to match one of several alternatives. For example, to match either cat or dog, you can use the following regular expression:
```
cat|dog
```
This regular expression will match either cat or dog.

### Character Classes
Character classes are used to match any one of a set of characters. Some common character classes are:
1. [abc] - Matches any of the characters a, b, or c
2. [a-z] - Matches any lowercase letter from a to z
3. [A-Z] - Matches any uppercase letter from A to Z
4. [0-9] - Matches any digit from 0 to 9
5. [^abc] - Matches any character that is not a, b, or c
For example, to match a string that contains any letter or digit, you can use the following regular expression:
```
^[a-zA-Z0-9]+$
```
### Flags
Flags are used to modify the behavior of a regular expression. Some common flags are:
1. i - Case-insensitive matching
2. g - Global matching (matches all occurrences)
3. m - Multi-line matching (treats the input as multiple lines)
For example, to match a string that contains the word hello regardless of case, you can use the following regular expression with the i flag:
```
hello/i
```
### Grouping and Capturing
Grouping and capturing are used to capture parts of a match. To group a pattern together, you can use parentheses. To capture the matched text, you can use back-references (\1, \2, and so on) in the replacement string.
For example, to match a string that contains a repeated word, you can use the following regular expression with a capturing group:
```
\b(\w+)\b.*\b\1\b
```
### Bracket Expressions
The character classes [a-z0-9-] and [a-z] match any lowercase letter, digit, or hyphen.
```
[a-z0-9-]
and
[a-z]
```
### Greedy and Lazy Match
The + and * quantifiers are greedy by default, meaning they match as many characters as possible. The *? quantifier is lazy, meaning it matches as few characters as possible.

### Boundaries
The look-behind assertion (?<=^) matches the start of the string, and (?<=\s) matches a whitespace character.

### Look-ahead and Look-behind
The look-behind assertion (?:(?<=^)|(?<=\s)) is used to match the start of the string or a whitespace character before the URL.

## Author
This regex tutorial was created by Sutton Charpentier. [GitHub](https://github.com/SuttonCharpentier)