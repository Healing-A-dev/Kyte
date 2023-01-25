# Kyten
Introducing Kyten! (Pronounced Key-ten or Kitten) A programming language coded in LUA. (You can delete this file if you please)

### "Find and Replace" Parser
The Kyten parser is something I guess you can call a double parser. Not only does the parser read the code line by line, but it also reads it letter by letter. Say if you want to have a custom syntax, you would have to spell it out letter by letter (I know, I know, very inefficient) then replace said phrase with its LUA equivalent. ***NOTE: EVEN THOUGH KYTEN IS CODED IN LUA YOU MUST USE A SEMICOLON!*** Example:
```ky
putln "Hello World"; <-- CORRECT

putln "Hello World" <-- INCORRECT
```

### Comments
When commenting in Kyten, keep in mind that if you are using a single line comment you still have to use a semicolon at the end of the comment. When using a multiline comments, the comments themselves MUST be placed inbetween the comments identifier!
```ky
-# Kyten has accese to single line comments;

###
  And Multiline comments as well
###
```

### Importing Files and Libraries
To import a file, use the 'import()' function. If you are importing a LUA file (since Kyten can run LUA files aswell), add the lua tag to the file name. 

Importing a file:
```ky
import "path/to/file";
```
Importing a Lua file:
```ky
import "path/to/file<lua>";
```
### Syntax
The syntax in Kyten is a bit different from the syntax in LUA.

Varibles:
```ky
table = {}; 
-# NOTE: Kyten does support nested tables;
local number = 300;
local string = "Hello";
```

Functions:
```ky
func speak(words):{
  putln words;
end};

speak("Hello");
```
If statements:
```ky
if (Number < 10):{
  putln "Number is less than 10";
}elseif (Number == 5):{
  putln "Number is equal to 5 (obviously)";
}elseif type(Number) != "number"{
  putln "Number is not even a number :/";
}else{
  putln Number;
end};
```
For statements:
```ky
for (i in pairs(table)):{
  putln i;
end};
```
While statements:
```
while (1 <= 10):{
  putln i;
end};
```
Indexing a table (for metatables):
```ky
table:set_index = table
```
Getting user input:
```ky
Name = getln();
```

The syntax for "or" and "and" is now
```ky
|| <-- or

&& <-- and
```

To conjugate strings or variables in string you use the "%" symbol example:
```ky
local Name = "Bob";

putln "Hello "%Name;
-# outputs "Hello Bob"
```
### Built in Library
Kyten has a built in library called "taks". Short for "Table and Kolor Support"
```ky
import "taks"

or

import("taks");
```

Taks give you access to the "wait()", "table.search()", "table.split()", and "table.merge()" functions. It also give you access to colors and text styles for the console andthe "typewrite()" function.
```ky
###
  An example of using taks for console color
###

import "taks";

putln Style["Bold"]%Color["Blue"]%"Hello World"%Reset;

or

-# Typewrite function usage (NOTE: If you are conjugating strings, you must use "..");

typewrite(Style["Bold"]..Color["Blue"].."Hello World"..Reset,0.1);
```
### Small but Important Changes
Instead of using "io.read()" function to get user input, Kyten uses the "getln()".

Also, just to make life a bit easier, Kyten has a math.random has been changed to math.genrand. Now there is no need to use math.randomseed(os.time()). Kyten does it for you!

### UPDATES
```
NONE
```