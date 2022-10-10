
# Longest Compound Word(Impledge)
## Steps to execute code
Just clone this repo and run the Longest_Compound_Word.cpp in any IDE for C/C++.
<br>**Note : change the file name accordingly to switch input files.**
## Approach
To find the longest and second longest compound word i used TRIE data structure. 
In **TRIE** store all the word from list and also maintains queue of pair of string which contains the current word and suffix.
After creating **TRIE** and **QUEUE** , **QUEUE** is processes by popping out pair from it.We check whether the suffix is a valid or compound word. 
If it’s a valid word and the original word is the longest up to now, we store the result.
The suffix may be compound word so we again apply the same procedure search its prefixes in trie if exists than add new word to queue and the new suffix.

## Optimisation
For the program to return results quickly even for very large lists (100,000+ items), i used TRIE with Map(so that there will no wastage of space).
**Space used here with every node here is proportional to number of children which is much better than proportional to alphabet size.**
## Time Complexity(time taken to process the input file)

The complexity of this algorithm is **O(kN)** where **N is the number of words in the input list, and k the maximum number of words in a compound word**. 
