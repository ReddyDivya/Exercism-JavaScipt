## String

A string is the JavaScript data type to store text data.


## Creating a String

You create a string by wrapping the text in single quotes or double quotes. On Exercism, single quotes are used.

'Hello, World!'
"Hello, World!"

---

## Strings as Lists of Characters

A string can be treated as a list of characters where the first character has index 0. You can access an individual character of the string using square brackets and the index of the letter you want to retrieve.

'cat'[0];  // 'c'
'cat'[1];  // 'a'
'cat'[2];  // 't'
'divya'[5]  // undefined

You can determine the number of characters in a string by accessing the length property.

'cat'.length; // 3

---

### Concatenation and Methods

The simplest way to concatenate strings is to use the addition operator +.

'I like' + ' ' + 'cats.';  // "I like cats."

Strings provide a lot of helper methods, see MDN Docs on String Methods for a full list.

The following list shows some commonly used helpers.
---
1. toUpperCase - method returns the calling string value converted to uppercase (the value will be converted to a string if it isn't one).
     
     ### Syntax
      toUpperCase()

      ### Example
      Ex: const sentence = 'The quick brown fox jumps over the lazy dog.';
          console.log(sentence.toUpperCase()); // "THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG."
---      
2. toLowerCase - method returns the calling string value converted to lower case.
      
       ### Syntax
       toLowerCase()

      ### Example
      Ex: const sentence = 'The quick brown fox jumps over the lazy dog.';
          console.log(sentence.toLowerCase()); // "the quick brown fox jumps over the lazy dog."
---
2. trim - method removes whitespace from both ends of a string and returns a new string, without modifying the original string.

      ### Syntax
      trim()

      ### Example
      Ex: const greeting = '   Hello world!   ';
          console.log(greeting); // "   Hello world!   ";
          console.log(greeting.trim()); // "Hello world!";
---      
3. includes - performs a case-sensitive search to determine whether one string may be found within another string, returning true or false.
      
      ### Syntax
      includes(searchString)
      includes(searchString, position)

      ### Example
      Ex: let sentence =  'The quick brown fox jumps over the lazy dog.';
          sentence.includes("fox"); // true
          sentence.includes("Fox"); // false
          sentence.includes("The", 11); // false
          sentence.includes("The", 0); // true
---          
4. startWith - determines whether a string begins with the characters of a specified string, returning true or false as appropriate. (Case-sensitive)
      
      ### Syntax
      startsWith(searchString)
      startsWith(searchString, position)
      
      ### Example
      Ex: const str1 = 'Saturday night plans';
          console.log(str1.startsWith('Sat'));  //true
          console.log(str1.startsWith('sat'));  // false
          console.log(str1.startsWith('Sat', 3)); // false
          console.log(str1.startsWith('Sat', 0)); // true
---       
5. endsWith - determines whether a string ends with the characters of a specified string, returning true or false as appropriate.
      
      ### Syntax
      endsWith(searchString)
      endsWith(searchString, endPosition)
      
      ### Example
      Ex: const str1 = 'Cats are the best!';
          console.log(str1.endsWith('best!')); // true
          console.log(str1.endsWith('best', 17)); // true

          const str2 = 'Is this a question?';
          console.log(str2.endsWith('question'));  // false      
---
4. slice - extracts a section of a string and returns it as a new string, without modifying the original string.
       ### Syntax
      slice(indexStart)
      slice(indexStart, indexEnd)
      
      ### Example
      Ex: const str = 'The quick brown fox jumps over the lazy dog.';
          console.log(str.slice(31)); // "the lazy dog."
          console.log(str.slice(4, 19));  // "quick brown fox"
          console.log(str.slice(-4));  // "dog."
          console.log(str.slice(-9, -5)); // "lazy"
   
Strings are immutable in JavaScript. So a "modification", e.g. by some of the methods above, will always create a new string instead.

