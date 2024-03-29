# YourRegexRicademy

## What is a Regex?
Regular expression, commonly reffered to as Regex, is a text format used in many computer languages that acts as a search pattern. Regular expressions can be used in code or search algorithims to find certain character patterns within a given string.

## Summary

For the beginning of our ricademy, we will be examine this regex for matching email addresses: <br>
` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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

Regular Expression:` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
<br> 
<br>
Below we'll be breaking down regex text groups into to their individual components:

1. `\^`- Using the backslash and caret, respectively, this signifies that this is the beginning of the text group and the start of the string.

2. `([a-z0-9_\.-]+)` This is the first portion of our regex. This is the portion that corresponds with the username of the email address. The (a-z) is whats telling it to match one or more lowercase letters that go through a-z. The (0-9) tells it to match numbers that match 0-9 more or equal than once, the same applies with the left over characters.

3. `@` - This is what separates the username from the domain name (username@domain.com)

4. `([\da-z\.-]+)`- This is the second portion of our regex. This is the capturing group the corresponds with the domain. All rules mentioned from No.2 can be applied to No.3.

5. `\.([a-z\.]{2,6})` This is the third and final portion of our regex. This capturing group corresponds with the top-level domain. All rules mention from No.2 can also be applied here. We also a have quantifier in our capturing group this will be futher elaborated in our [Quantifiers](#quantifiers) tab.

6. `$/` - The dollar sign with the foward slash at the end siginifies that it's the end of the string.

## Anchors
In a regex, the symbols `^` and `$` are used respectively to start and finish a string. This just ensures that the string matches its portion correctly.

## Quantifiers
Quantifiers describe how many occurrances of a characters, group, or character class must be present in the input in order to find a match. The `+` operator and the quantifier `{2,6}` are used to command that the email's tail should be between 2-6 characters long. 

## OR Operator
With an OR operator `|`, you can match characters to the left and right of the `|` character but, this isn't being currently used in our regex example. 


## Character Classes
`[]` Brackets in a regex are used to define character classes which will match any character that's inside the brackets. For example, the lowercase letters, numbers, underscores, periods and hyphens are valid examples of a character class.

## Flags
Flags are optional parameters in regular expressions that change the behavior of the string based on which flag is picked.
<li><b>(i) Case-insensitive flag</b></li>
<p>Case-insensitive flag will lookout for letters regardless of their capitilization.</p>
<li><b> (g) Global flag</b></li>
<p>In a regex when global is used, it means that the regex will search for all occurences of a pattern in the string and not just the first one.
<li> <b> (m) Multiline flag </b> </li>
<p> A multiline flag is used when you want to search a pattern across multiple lines instead of one.
<li><b> (s) Dot all flag</b></li>
<p> when a '(s)' is used, it will match any spot where there's spaces, tabs, or line breaks.</p>
<li><b> (u) Unicode flag</b></li>
<p>The '(u)' in a regex instructs the computer to implement unicode character matching rules while looking for patterns in a string. This is more important if you're working with text from non-latin writing systems.</p>
<li><b>(y) Sticky flag</b></li>
<p>What the sticky flag will do is it will look for patterns at a specific spot in the string and will go only to that spot until the match is unsuccessful.</p>

## Grouping and Capturing
`()` - Paranthesis are used to group and capture parts of a pattern. This was used we captured our username, domain, and top-level domain in our regex email address.<br>
`([a-z0-9_\.-]+)` - <b>Username</b> <br>
`([\da-z\.-]+)` - <b>Domain</b><br>
`([\da-z\.-]+)` - <b>Top-level domain</b>

## Bracket Expressions
`[]` - Bracket expressions are used to match a single character from a set of characters. For example, `[abc]` will match any single character that either 'a', 'b', or 'c'. You can also use `[a-z]` to match all lowercase letters that range from a to z. This can also be applied to numbers and other special characters as well.

## Greedy and Lazy Match
By default your regex engine should be in greedy `+`. What this means is that it will match as much of the input string as possible while still allowing the pattern to match while a <b>lazy match</b> `?` will try to find the shortest substring possible that still matches the pattern which means your regex engine will stop matching as soon it finds a valid match. 

## Boundaries
Boundaries are used to match the position between characters in a string.<br>
There's two main types of boundaries:<br><br>
<b>The caret `^`</b> which matches at the beginning of a line or string.<br>
<b>The dollar sign `$`</b> matches the position at the end of a line or string.<br> 
This same can be applied with words using <b>`\b`.</b>  


## Back-references
Back-references `\` are used to reference a previously matched group in your regex. You can also use a backslash `\` followed by a number to refer to a specific group.

## Look-ahead and Look-behind
Look-aheads and look-behinds are used to match a pattern if it's proceded or followed by another pattern without including the other pattern in the match itself.<br><br>
<b>Positive look-ahead:  `(?= )`</b><br>
<b>Positive look-behind: `(?<= )`</b><br>
<b>Negative look-ahead:  `(?! )`</b><br>
<b>Negative look-behind: `(?<! )`</b>

## Author

Steven NZ <br>
Feel free to checkout some of my work with the link below  : )<br>
Github Username: <a href ="https://github.com/SteveeZee03?tab=repositories"> SteveeZee03</a>