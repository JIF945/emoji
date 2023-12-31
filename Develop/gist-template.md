# EMOJI

A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.

## Summary

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary.

Anchors - They do not match any character at all. Instead, they match a position before, after, or between characters. They can be used to “anchor” the regex match at a certain position. An anchor consit of a caret ^ and  $  dollar character. The caret ^ matches at the beginning of the text, and the dollar at the end. Click on anchors to see a code  snippet. 

Quantifiers - specify how many instances of a character, group, or character class must be present in the input for a match to be found. Click on the quantifilers to see a code snippet

Greedy and lazy match - By default, a quantifier tells the engine to match as many instances of its quantified token or subpattern as possible. This behavior is called greedy.

In contrast to the standard greedy quantifier, which eats up as many instances of the quantified token as possible, a lazy (sometimes called reluctant) quantifier tells the engine to match as few of the quantified tokens as needed. A regular quantifier is made lazy by appending a ? question mark to it

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

Both anchors together ^...$ are often used to test whether or not a string fully matches the pattern. For instance, to check if the user input is in the right format.

Let’s check whether or not a string is a time in 12:34 format. That is: two digits, then a colon, and then another two digits.

In regular expressions language that’s \d\d:\d\d:

    let goodInput = "12:34";

    let badInput = "12:345";

    let regexp = /^\d\d:\d\d$/;
    alert( regexp.test(goodInput) ); // true
    alert( regexp.test(badInput) ); // false

Here the match for \d\d:\d\d must start exactly after the beginning of the text ^, and the end $ must immediately follow.

The whole string must be exactly in this format. If there’s any deviation or an extra character, the result is false.

### Quantifiers

    const ghostSpeak = 'booh boooooooh';
    const regexpSpooky = /bo{3,}h/;
    console.log(ghostSpeak.match(regexpSpooky));
// Expected output: Array ["boooooooh"]

    const modifiedQuote = '[He] ha[s] to go read this novel [Alice in Wonderland].';
    const regexpModifications = /\[.*?\]/g;
    console.log(modifiedQuote.match(regexpModifications));
// Expected output: Array ["[He]", "[s]", "[Alice in Wonderland]"]

    const regexpTooGreedy = /\[.*\]/g;
    console.log(modifiedQuote.match(regexpTooGreedy));
// Expected output: Array ["[He] ha[s] to go read this novel [Alice in Wonderland]"]

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

Joshua James
github - 
