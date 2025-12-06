<!-- <p align="center">
<img width="200" height="230" alt="image" src="https://github.com/xmm16/xmm16.github.io/blob/main/timeworm.png?raw=true" /></p> -->
<h3 align="center"><b >Timeworm</b></h3>

A compiler that knows your code on an initialization-variable-name basis to time-travel which results in a type-based butterfly effect!

#### What that actually means
Say we have a string that you add and remove a ton of other strings and characters to
```cpp
string example = "hello!";
example = example[0, -1]; // example = "hello"
example += ' ';
example += "world!";
```
Eventually, we may decide to ask for the length of this string
```cpp
string example = "hello!";
example = example[0, -1];
example += ' ';
example += "world!"; // example = "hello world!"
print(example.length);
```
Most languages will keep track of the length and return it, which is extremely optimized, but we've decided to do something different. 
```cpp
s̶t̶r̶i̶n̶g̶ string_with_counter example = "hello!";
example = example[0, -1]; // every operator is now overloaded to track length updates
example += ' ';
example += "world!"; // example = "hello world!"
print(example.length);
```
If the compiler never sees you request the length of a string (or an alias/slice of a string, because the compiler knows your code on an initialization-name-basis), it just won't keep track. However, if it does, it'll go back (or time travel) and change the type (leading to a type-based butterfly effect).
