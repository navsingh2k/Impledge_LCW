
# Longest Compound Word(Impledge)

## Problem Statement
Write a program that:
1. Reads provided files (Input_01.txt and Input_02.txt) containing alphabetically sorted words list (one
word per line, no spaces, all lower case)
2. Identifies & display below given data in logs/console/output file
o longest compounded word
o second longest compounded word
o time taken to process the input file
<br> **Note: A compounded word is one that can be constructed by combining (concatenating) shorter words
also found in the same file.**

## Steps to execute code
Just clone this repo and run the Longest_Compound_Word.cpp in any IDE for C/C++.
<br>Note : change the file name accordingly to switch input files.

## Approach
To find the longest and second longest compound word i used TRIE data structure. 
In TRIE store all the word from list and also maintains queue of pair of string which contains the current word and suffix.
After creating TRIE and QUEUE , QUEUE is processes by popping out pair from it.We check whether the suffix is a valid or compound word. 
If it’s a valid word and the original word is the longest up to now, we store the result

### Optimisation
For the program to return results quickly even for very large lists (100,000+ items), i used TRIE with Map(so that there will no wastage of space).
**Space used here with every node here is proportional to number of children which is much better than proportional to alphabet size, especially if alphabet is large.**
