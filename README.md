# i-rep
interactive command-line tool for deleting/replacing lines in a file.  
This tool is similar to other UNIX tools like sed, awk and tr except   
it alows the user to look at a line of text and interactivly decide whether they want to   
(r)eplace, (d)elete or (i)gnore that line, where ignore means do not modify  
I created this when I was making a [wordle](https://github.com/brianSalk/wordle-rs) game that had a word_list file  
and I wanted to remove plurals, but not all words ending in 's' are plural  
so the interactive part comes in handy.  
```diff
- WARNING: this program modifies your input file in place and does not make a backup copy!
```
# setup
after cloning this to your computer you may want to move/copy it to /usr/local/bin or some other directory in your PATH environment variable.  
# use
```i-rep file-to-modify [pattern] [starting-line-number]```
# examples
let's say you have the following file called words.txt:  
```
words
this
has
make
can
stands
```
and I want to remove all the plurals.  I could run
```
i-rep words.txt ".*[sS]$"
```
and then interactivly decide what to do with each word that ends with 's'

If I want to start somewhere in the middle of the file, say line 3, I could do:  
```
i-rep words.txt ".*[sS]$" 3
```
and it will skip the first three lines even if they match the pattern  
if I want to match everyline, I can simply omit the pattern and line number and just provide the file:  
```
i-rep words.txt
```
