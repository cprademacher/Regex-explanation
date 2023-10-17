# Regex-explanation

This README will serve as a tutorial of a common way developers might validate passwords that users input.  

## Summary

The regex I will be describing serves as a password validator and I will be explaining each portion of the regex and why it is included/used. The regex I will be explaining is:

```^(?=.*[A-Z])(?=.*[a-z])(?=.*\d)(?=.*[@#$%^!&*])[A-Za-z\d@#$%^!&*]{8,16}$```


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
'^' and '$' assert the start and end of the string, ensuring that the entire string meets the criteria.

### Quantifiers
Quantifier are used to quantify how many times a part of your regular expression should be repeated.  Every time you want to repeat something in a regex, you can write a quantifier after it to specify how many times it should be repeated.

(?=.*[A-Z]) ensures there is at least one uppercase letter.

(?=.*[a-z]) ensures there is at least one lowercase letter.

(?=.*\d) ensures there is at least one digit.

(?=.*[@#$%^!&*]) ensures there is at least one special character.

[A-Za-z\d@#$%^!&*]{8,16} specifies that the password must consist of characters that are uppercase letters, lowercase letters, digits, or the specified special characters, and it must be between 8 and 16 characters long.

### OR Operator
If we want to decide between one thing OR another in a regex, we use the '|' symbol between the two items in question.  For our common password validation regex, we do not have the need for an OR operator, so it is not included.

### Character Classes
In the context of a regular expression, a character class is a set of characters enclosed with square brackets.  It specifies the characters that will successfully match a single character from a given input string.  The character classes in our regex are listed below.

[A-Z] ensures that we have at least one uppercase letter.

[a-z] ensures that we have at least one lowercase letter.

[@#$%^!&*] ensures we have at least one special character.

### Flags

Regex flags change the default match behavior.  Below are the flag examples:

g	- Performs a global match, finding all matches rather than just the first.

i	- Makes matches case-insensitive. Matches both uppercase and lowercase.

m -	Performs multiline matches. (Changes behavior of ^,$)

s -	Allows . to match newline characters.

u -	Enables Unicode support.

y -	Matches are sticky, looking only at exact position in the text.

Since our password validation regex is only making sure the password has at least one of each required type of character, and it is only 8-16 characters long, none of these flags are needed in our regex, and are thus not used.

### Grouping and Capturing
Capturing groups are a way to treat multiple characters as a single unit. It is done with paranthases and in our example simply groups the uppercase, lowercase, numerical, and special character callings as their own callings.

### Bracket Expressions
A bracket expression (an expression enclosed in square brackets, "[]" ) is an RE that shall match a specific set of single characters, and may match a specific set of multi-character collating elements, based on the non-empty set of list expressions contained in the bracket expression.

In our case, we use bracket expression for all but our numerical callings.  [A-Z] to find at least one uppercase letter, [a-z] to find at least one lowercase letter, and [@#$%^!&*] to find at least one special character.  

### Greedy and Lazy Match
"GREEDY" means match the longest possible string.
"LAZY" means match the shortest possible string.
For example: the greedy h.+l matches 'hell' in 'hello' but the lazy h.+l matches 'hel' in 'hello'

This is not used in our regex, but can be extemely useful.

### Boundaries

### Summary
In summary, regular expressions (regex) allow developers to to validate code, match patterns, manipulate text, parse structured data, and much more without having to write tons of lines of code to do so.  Our password validation regex in particular makes authenticating logins much more strait forward than it would be otherwise.

## Author

My name is Cody Rademacher and I am a full stack developer looking for my first role as a software engineer.  You can visit my GitHub profile at: https://github.com/cprademacher
