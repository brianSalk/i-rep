# i-rep
interactive command-line tool for deleting/replacing lines in a file.  
This tool is similar to other UNIX tools like sed, awk and tr except   
it alows the user to look at a line of text and interactivly decide whether they want to   
(r)eplace, (d)elete or (i)gnore that line, where ignore means do not modify  
I created this when I was making a wordle game that had a word_list file  
and I wanted to remove plurals, but not all words ending in 's' are plural  
so the interactive part comes in handy.  
# setup
after cloning this to your computer you may want to move/copy it to /usr/local/bin or some other directory in your PATH environment variable.  
# use
```i-rep file-to-modify [pattern] [starting-line-number]```

