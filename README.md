# Strings
####A short introduction to strings in Ruby and the [] method

## What is a string?
  A string is an object that holds a sequence of bytes. 
  
  A byte consists of eight bits, with one bit representing a single binary value, either 0 or 1:
  
                a = |0|1|1|0|0|0|0|1|                   A = |0|1|0|0|0|0|0|1|            
  
######NOTE: Most computers use the American Standard Code for Information Interchange (ASCII) to represent characters 

  A *string literal* in Ruby is code that has been marked with a single or double quotation. Alternatively, you can use the % symbol followed by a pair of any type of bracket or non-alphanumeric character:
```
string_literal = "abcdef"
string_literal = %{abcdef} 
string_literal = %?abcdef?
string_literal = %<abcdef>
string_literal = %[abcdef] 
```
The *% notation* can also be used to execute commands when paired with alphabetic characters: 
```
modified_string = %w(abc def) #=> ['abc', 'def']
modified_string = %W(abc #{def}) #=> ['abc', 'def']
```
New strings can also be created by calling the ```.new``` method:
```String.new("abcdef")
```

##Making substrings: the ```[] aka .slice``` method
  Characters within a string are numbered from 0. The ```[]``` method returns the *n*th character within a string:
  ```
  string = "abcdef"
  string[0] #=> "a"
  ```
  Providing a second number returns a substring of that length:
  ```
  string[0,3] #=> "abc"
  ```
  A range can be specified using ```a..f```(including "a" and "f"), or ```a...f```(excluding "f"). Negative numbers are also accepted, which count back from the end character of the string, but the second number must be closer to the end of the string:
  ```
  string[0..2] #=> "abc"
  string[0...3] #=> "abc"
  string[-3..-1] #=> "def"
  ```
  The ```[]=``` method lets you substitute a specified substring for another:
  ```
  string ="abcdef"
  string["def"] = "123" #=> string now equals "abc123"
  ```
  
  #####Author
  ######Tim Tang  
  
