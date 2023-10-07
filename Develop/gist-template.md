# Regex Tutorial for a Hex Value using Gist - Homework #17

For this homework assignment we are asked to accommplish several things. First off, is to use gist to create this homework assignment, this is in place of using a README file.  Second, the task at hand is to make this gist tutorial explaining a regex, or regular expression. So, I will look at, describe and explain a hex value, and the regex for a hex value. 

## Summary

The below paragraphs and topics will look at the pieces and parts necessary for the gist, regex and hex value.  I will then go on to describe and explain the parts of the regex.
Instead of grouping everything together in the summary, I have broken down the topics and listed them separately below.  The Gist and Regex topics will explain each of fully.  Then I will use both of them to create the regex for an hex value.


## Table of Contents

- [Gist](#gist)
- [Regex](#regex)
- [Hex Value](#hex-value)
- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Gist

The bootcamp homework assignment states: "Instead of creating a repository, you’ll publish a GitHub gist. GitHub describes a gist as a simple way to share code snippets with others. It’s also an ideal way to demonstrate a technique, teach a principle, or show off a solution. It functions just like a repository, and you’ll use Markdown to create it, just as you do with your READMEs. Gists can include code, images, links, and anything else you can include in a README."

So in this assignment I am creating this file as a gist file, and using it to explain the hex value of a color.

## Regex

A regular expression, or regex is a pattern of numbers, letters and characters that create a pattern used to represent or look for something.  Regex's can be sued for color equivalents, but are also used in artificial intelligence, data science and microcontrollers to simplify the handling and manipulation of data.  The code for a hex value is a smaller, more efficient way of writing the data needed to refer to any one of these things.

A regex can represent a specific color for a website, or the website can decode the regex to get the color - example: black can be written as #000000 or #000000 can be researched to get the meaning of black.

As quoted from freeCodeCamp: "Regular expressions provide a powerful and flexible way to define patterns and match specific strings, be it usernames, passwords, phone numbers, or even URLs."
A regular expression is also known as, and commonly referred to as a "Regex.

Stated in the bootcamp homework assignment is the following definition of a regex: "A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input." 

## Hex Value

Hex Value is based on Hexa Decem. The Greek definition of this is: hexa = 6, and decem =10.

Hex Value is a system based on 16 letters and/or number to create a numbering system.  The numbers are; 0 to 9.  The letters are; A,B,C,D,E,F.
Working with combinations of these letters and numbers creates a base of 16.  So the base of these characters used once equals 16 values.  The base of these characters used twice equals 16 * 16 or 256 values.  When looking at colors sometimes you will see the word of the color, such as "red", and sometimes you can see the value of the color: 255, 0, 0.  This represents three groups of 2 values of 16.  

The purpose of this gist is to break apart the above code and explain what each part does, hence how the expression fits together to make a hex value.

Hex values are used by developers and such for getting the value of a color.  Examples would be: Black #000000, White: #FFFFFF, and Red #ff0000

## Regex Components

A hex value in javascript looks like:    /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ 

### Anchors

Anchors are used at the beginning and the end of the string.  These anchors are: / ^ $
The string starts and ends with a forward slash (/).
Anchor: ^
The circumflex (^) starts the string.  Followed by a forward slash (/).
Anchor: $
The dollar sign ($) ends the string followed by another forward slash (/).

The hashtag (#) is optional - it is used to show the difference between a hexadecimal number and a decimal number.

Thus the anchors for the above read:  /^#
And   $/

### Quantifiers

Question marks are used as boolean qualifiers, having a value of 0 or 1. 

Curly brackets {} that contain a number are also a qualifier.  The number in the curly brackets states the number of characters the hex value will be.  Thus in the example above, the first set of curly brackets shows the number 6.  There will be 6 characters in that hex value.  Such as: 123ABC.  In the second set of curly brackets above, the number is 3, thus here there will be 3 values in the hex value.  The explaination of how to know if the answer should be 6 characters or 3 characters will be explained below when the "|" symbol is shown and explained in the Operators section.  This equates means that there will be 6 or 3 characters (between 0 and 9 and A - F) in this expression. 


### OR Operator

The "OR" operator is a straight line "|"

The or operator is a boolean value, it says that the expression is either the first (6 characters) OR the second (3 charactors).
In the case above, both the 6 and the 3 are allowed as matches in the expression.  This is used where the color is #FF0000 which is also 255, 0, 0 with a specific pattern to match.

### Character Classes

The numbers 0 through 9 and the letters a through f are the character classes used in this redex.  Only 1 out of the group offered has to match.  A hyphen (-) can be used in the expression to separate the numbers and letters from each other.  The hyphen is used as a "through" symbol - such as 0 "through" 9.

### Grouping and Capturing

The paranthesis are used for grouping.  In this way, anything placed within the paranthesis will be treated as a single unit. Then the capturing lets the group text be referred back to.
In the hex value sample used here and above: ([a-f0-9]{6}|[a-f0-9]{3})  The paranthesis are grouping the two expressions together with an OR statement in the middle.

### Bracket Expressions

Brackets, or better known as square brackets [] are used to match on any one of the characters within that list.  A hyphen (-) is usually used within the characters to separate them. In the above example the square brackets are looking to match a string that has any character between 0 and 9  and/or a - f.

### Greedy and Lazy Match

Greedy and Lazy Matches refer to the match being made on the string.  While a greedy match will look at and match  all or as many as possible of the entire string, a lazy match will look at and match as few or as little of the string as necessary.

### Boundaries

The anchor tags of ^ and $ used in the beginning and end of the expression are boundary tags.  If you want to use the ^ or the $ in the expression as actual characters, a back slash would need to be used with them.

### Back-references

When a group has been captured and it needs to be referred back to it is know as back-referencing.  So you would back-reference code that was previously captured.

### Look-ahead and Look-behind

The regex code matches from the left to the right.  Look-ahead simply means to look or refer to what's on the right, while look-behind is referring to what's on the left.

## Author

Author - Linda Vitrella  github: LindaV2023 part of the Full Stack Developers Bootcamp at UConn
 
