# ScrabbleSolver

## Description
This Scrabble solver takes 7 letters from the user, as one would draw in a game of Scrabble, and returns the 10 highest scoring words. The resulting words can be any length from 2 to 7 letters. Word scores are calculated based on the base letter points and does not include properties of the board such as double letter or double word tiles.

## Implementation
All code is written in Java. The main function is called ScrabbleSolver.java. This function first reads a text file containing the Scrabble letter points<sup>1</sup> and then one which contains a dictionary<sup>2</sup>. Next, user input is acquired by asking the user to enter in the 7 letters one at a time. Once the 7 letters are gathered, the program calculates all possible permutations, narrows down to just the ones which are valid words (checks the dictionary), then calculates the number of points each word receives based on the letter scores. Permutations were calculated using modified permutations and combinations algorithms found online<sup>3,4</sup>. The words are then sorted based on their point values, and the top 10 words are returned to the user.

## Optimizations
   - Using a HashSet for words to efficiently check if word in dictionary and prevent duplicate entries
   - Using a HashMap for mapping the letters to points

## Sources
1. https://en.wikipedia.org/wiki/Scrabble_letter_distributions
2. https://github.com/dwyl/english-words/blob/master/words_alpha.txt
3. https://www.geeksforgeeks.org/java-program-to-print-all-permutations-of-a-given-string/
4. https://www.geeksforgeeks.org/print-all-possible-combinations-of-r-elements-in-a-given-array-of-size-n/
