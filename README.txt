README
James Kuch

-ciphers.hs
The main program, tested in GHCi with (all files in ~\Haskell Platform\2014.2.0.0\winghci)
:l ciphers.hs

-ciphers.hs
The main program, contains a series of simple cipher related functions including:
-A couple Caeser ciphers (aka a shift cipher) and solvers for both.
 -One version considers all ASCII characters and the other only considers letters)
 
-A frequency based substitution cipher solver that takes each character's frequency
 and assumes a solution based on a preset alphanumeric order

-A brute force based substitution cipher solver that uses a few tricks to find out
 some of the more common letters, then tries combinations for all the other letters
 until it finds a word- it then takes the letters of that word and adds them to a list
 of known letters, thereby severely reducing the number of brute-force combinations to check.
 This process repeats until all 26 letters are found, or the file passes a spellcheck of at least 50% accuracy
 (Results are usually still error prone, but usually to the point physical inspection can reveal the solution)

-A spellchecker used to check the solutions of the above ciphers for accuracy
 -dictionary for the spellchecker provided below
 
-main, consists of several commented out benchmarks tests- they all work though.
 The last cipher is uncommented for use.

for details of helper functions, please see comments.
 
-wordsEn.txt
An extensive list of words used as a makeshift dictionary for the brute force algorithms. Source & stats below.
http://www-01.sil.org/linguistics/wordlists/english/
-109582 words, -935172 characters