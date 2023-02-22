# RegEx
### Regular expressions, or regex, is a tool used to sort data more efficiently compared to sorting methods in Javascript. Regex helps keep your code efficient and easy to read.

## Summary

In this tutorial, we will discuss the components of regex and how to use them.

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

Some characters do not call a character to be searched, instead they do what we could call "commands". These are called anchors. The following are used primarily in Javascript:

- ^: Beginning of a string or line. In all engines except Ruby, the ^ can be used to assert the beginning of a string is the current position when [multiline](#flags) is not specified. So for example if we wanted to search an entire string for all the "a"s in it, we would use ^ to do so.

- \$: End of a string or line. This is used in different ways depending on context. On all engines, "\$" will indicate the end of a string. For example, if your string is "the apple" and we use "e$", it will indicate the e at the end of "apple", but not at the end of "the".


### Quantifiers

Quantifiers specify the amount of instances a character, group, or character class is present.

- *: Matches zero or more times.
- +: Matches one or more times.
- ?: Matches zero or one time.
- {n}: Matches exactly *n* times.
- {n,}: Matches at least *n* times.
- {n,m}: Matches from *n* to *m* times.

### OR Operator

The OR operator is used to find either/any of the inserted queries. For example:

    /(t|T)he/g

<mark>The</mark> bunny likes <mark>the</mark> apple

In this example, we are finding every "the" and we are including capitalized "the"s.

### Character Classes

Character classes or character sets can be used to find specific groupings of characters. These classes are wrapped in square brackets [].

    /[ay]/g

Is it gr<mark>ay</mark> or grey?

### Flags

When searching for something in regex, we use flags. The standard flag is simply "//" which will find the first result matching your query. The other types of flags are:

1. //g (global. Will allow multiple results on a global scope.)
2. //i (case insensitive. Ignores capitalization and will find results that match your query reguardless of capitalization.)
3. //m (multiline. Allows ^ and $ to match newline characters.)
4. //s (single line. Allows . to match newline characters)
5. //u (unicode. Treat a pattern as a sequence of Unicode code points.)
6. //y (sticky. Perform a "sticky" search that matches starting at the current position in the target string.)

### Grouping and Capturing

When searching, we can specify multiple groups of searches. These groups are wrapped in parentheses ().

    /(or)|(ap)|(st)/g

I like <mark>ap</mark>ples, <mark>st</mark>rawberries and <mark>or</mark>anges.

In this example, we've utilized or operators to look for all the specified letter combinations.

### Bracket Expressions

Bracket expressions are used to match a single character or collating element. For example:

    /gr[ae]y/g

Is it <mark>grey</mark> or <mark>gray</mark>?

In this example, we are searching for either spelling of the word gray. Since we used bracket expression, regex knows to look for words with either a or e inbetween gr and y.

### Greedy and Lazy Match



### Boundaries



### Back-references



### Look-ahead and Look-behind



## Author

Emma Waltho, beginner web developer, CSS enthusiast. [GitHub](https://github.com/ewaltho)