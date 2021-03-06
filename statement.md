# C# Tutorial - Part 3: Data Types

In the last tutorial, we defined what a variable was, and harnessed its power to solve mathematical problems in C#, and in the process, we learned how the computer stores memory. If you haven't read it yet, see Part 2! Many think they're too good to know how the computer works with memory under the hood, but trust me, it's worth it!
Today, I'm going to explain the different data types in C#, and why knowing the difference is so important. You wouldn't want to divide a jack o' lantern emoji by the letter 'b', would you?

## Data Types: Variables with a Mission

You're going to notice two lines from the last tutorial that would make some programmers very angry:
```
var d = 12;
var t = 0.25;
```
Is it because the names of the variables are "d" and "t" and have absolutely no description? Well, that's not what I was going for, but in many cases, programmers do like more descriptive names.
Actually, the issue is "var". In the last tutorial, I said "var" told the computer that it needed a piece of memory to put a variable inside. But what kind of variable? You see, in math, we're used to all variables being some kind of number, but that is not the only type of data that can be held by a computer. All data on a computer is represented by a series of 1s and 0s, but the way the computer reads and processes the data is different for every type. Making sure the computer knows what kind of data it's dealing with can be crucial!
"var" is perfectly fine to use! But it just causes some annoyance for some programmers. More on that later!

Here are all of these illusive "data types" that C# currently handles:

```
//Logic
bool (true/false)

//Whole numbers
byte -  (0 to 255)
sbyte - (-128 to 127)
short - (-32,768 to 32,767)
ushort - (0 to 65,535)
int - (-2,147,483,648 to 2,147,483,647)
uint - (0 to 4,294,967,295)
long - (-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807)
ulong - (0 to 18,446,744,073,709,551,615)

//Fractions
float - (-3.4 x 10^38 to 3.4 x 10^38)
double - (-2.2 x 10^308 to 2.2 x 10^308)
decimal - (-2.2 x 10^308 to 2.2 x 10^308)

//Text
char - (U+0000 to U+FFFF)
string - (infinite possibilities)
```
Whew, that is a LOT! But the four categories are all that is important here. You can store letters and numbers in the computer, and C# will know how to handle them when you want to change the value or use it in some way. With a "bool" You can also store the truth or lies in a computer... Well not really. You can do that without true/false, but a "bool" will let you store logic that is used to make your program work! It's an important topic that will be covered with Loops and If statements in the next tutorial. It's too complex for now, so stay tuned!

In our last example, "d" and "t" were numbers. When the computer saw them, it knew what it had to do:
```
//What you see
var d = 12;
var t = 0.25;

o<*POOF*>o

//What the computer sees
int d = 12;
double t = 0.25;
```
For "d", it saw a number and thought "No decimal place. The programmer probably wants to store a whole number. I'll make it an integer!". 
For "t", it saw the point and thought "Huh. The numbers after that decimal place must be important! I'll make it a fraction". Fractions, known as "floating point numbers" in computer science, are very useful for scientific measurements and certain mathematics. 

For numbers, all forms of basic math can be used:
* Addition (+)
* Subtraction (-)
* Multiplication (*)
* Division (/)
* Modulus (%)

As long as you give each of these numbers and the answer exists it will spit out an answer you can use in your code! Sometimes the answer does not exist, so be careful (I'm looking at you, division! You and zero don't get along sometimes).