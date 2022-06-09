# Reg-NotMe (Matching URL Tutorial)

This tutorial explains how a regular expression (regex) for matching a URL functions, breaking down each component of the expression and describing what it does.



## Summary

This tutorial describes the regex, or sequence of characters that defines the specific search pattern of a URL, /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/. The characters used in this specific search pattern are called metacharacters, which instead of indicating a literal character, indicates a more generalized pattern. Regex are frequently used to validate input, as when included in code or search algorithms, regex can be used to find certain patterns of characters in a string, or find and replace a character or sequence of characters within a string.



## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

Regex components include anchors, quantifiers, Character Classes, Grouping and Capturing, Bracket Expressions, Greedy and Lazy Match. 


### Anchors

The two principal anchors in this regex expression are the ^ at the beginning and the $ at the end which constitute an exact string match with the components included within the two anchors. When used alone, the ^ anchor matches any string that begins with the characters that follow the anchor. The $ matches any string that ends with the characters that precede it. By enclosing the regex between these two anchors, we are asking the search function to match exactly is included between them (what it begins AND ends with).

### Quantifiers

Notice that some of the components of capture groups end with a ? or a *. These are generally known as quantifiers. Quantifiers are used to define the number of times a given expression may be identified. The ? makes a single instance of the character preceding the quantifier optional, whereas the * makes multiple instances of the characters preceding the quantifier optional.


### Character Classes

The main character classes to consider in the above expression include the \d character class which looks for any digit, and the \w character class that looks for any alphanumeric character.


### Bracket Expressions

The main OR operator used in the above regex is the []. The expression will match for any characters or character classes included in the brackets. For example the [\da-z\.-] expression matches for any digits (\d) OR any characters between a and z (a-z) OR any '.' (\.) OR any '-' (-).



### Greedy and Lazy Match

The quantifier metacharacters * + and {} are greedy operators which expand the match as far as possible through the string. For example, <.+> matches this entire string <div>A div with divs in a div</div>.

The URL regex uses the all of these metacharacters to quantify the number of matches of a particular string.



## Author

Thank you for visiting! Hello my name is Sophia Davis and I am a full stack web developer. Follow me www.github.com/sdavis525 and www.linkedin.com/in/sophiadavis525