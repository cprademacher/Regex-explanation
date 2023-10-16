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

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
