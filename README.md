# Regular Expression Tutorial for Validating an Email Address.

What is Regular Expression?

Imagine you are writing an app and you want to allow people to sign up using their email address. Well how to make sure that the information that they are providing to you is a valid email? Well toay we will be taking a look at a snippet of regex code that is commonly used for email validation, and understanding how it works!

## Summary

This is the snippet of Regex that we will be working with today:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

What are anchors? Anchors arent used to match characters, however are used to map positions before, between or after character. In our example expression above the ^ indicates the start while the $ indicates the finish hence "anchoring" the regex match.

### Quantifiers

In this example, we used + to communicate there is another sequence to be matched as a greedy quantifier. We also used {2,6} as another greedy quantifer to specify the input should be a minimum of 2 characrtors to a maximum of 6 characters.

### Character Classes

In our example Regex, we use the character class /d which in Javascript classifies the use of any integer from 0 to 9.

### Grouping and Capturing

In our example we are currently using three groups. Group #1 is is the username of the email account [a-z0-9_\.-]. Group #2 is used to capture the domain name of the account [\da-z\.-]. And the finally Group 3# is used to capture the domain extention [a-z\.]{2,6}.

### Bracket Expressions

Similar to the grouping, there are also three bracket expressions. Information in the brackets identifies which infrmation is allowed to be match [].

Expression #1: [a-z0-9_\.-] allows for lowercase letters a-z, numbers from 0-9, an underscore, periods and hyphens.

Expression #2: [\da-z\.-] includes all digits, lowercase characters, periods and hyphens.

Expression #3: [a-z\.] includes case sensitive characters from a-z and periods.

### Greedy and Lazy Match

In this example we have only used greedy quantifiers + and {}, meaning that it will allow the match to expand as long as it neess to go. If these quantifiers were lazy quantifiers, they would appear as +? or {}?, this will direct the system to make the shortest match.

## Author

My name is George Wise, and I am slowly but surely becoming more and more comfortable calling myself a web developer!

Check out my github repo: https://github.com/Stubblefish/Regex-Tutorial
