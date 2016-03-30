## Start Coding ##
We'll start by creating a basic workspace. First, create a folder that will act as your workspace. I made mine as ~/code. This can be done either by using your OS's gui or through terminal. In terminal, we would type `mkdir ~/code` to create the folder code in `~/`.

Now, let's write a Hello World in Java.

  1. `cd ~/code` to set your current directory to your code folder
  1. fire up Emacs
  1. `C-f` to create a new file, and enter `Hello.java` when it prompts for a destination.
  1. Now, you can start coding. For now, just copy over the sample code:
```
// Don't worry about not understanding the code for now, this is just to make sure you can run code
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```
  1. `C-x C-s` to save the code, and `C-z` to put it in the background.
  1. `javac Hello.java`: this will compile the code.
  1. `java Hello`: this will run the code.
  1. You should see this output: `Hello World!`
  1. `fg` to get back into emacs
  1. Try messing with the code to change to output to `Hello, <Your Name>!` instead of `Hello World!`.
  1. Save, compile, and run to see if you did it correctly.

You will later learn about a powerful new IDE called **Eclipse**, but learning the basics is best left to lightweight editors such as Emacs.

## Primitives ##

You will learn the different ways data is stored in a program. This includes learning about the basics of how computers work as well as how what different data types that store data and how this looks like in a physical standpoint.

### What is a Program? ###

If you look at a program and strip it down to its very basic components, a program does nothing but a bunch of data manipulation, whether it be changing the color of a pixel or recording an action, such as a key stroke; however, with this basic data manipulation, computer can do crazy cool things. All data in a computer is stored in a sequence of zeros and ones. In physical terms, a zero is when no current is running through, and a one is when current is running through. With this, programs can interpret a sequence of such zeros and ones as either a variety of things, such as a number or a character.

### What are Primitives? ###

**Primitives** are the basic means of storing data in programs. As you know, all primitives are composed of zeros and ones in a physical sense. A single zero or one is known as a bit. A bit inherently holds only 2 values: zero and one. A byte is a series of 8 bits, and can therefore hold 256 values, because 2^8 is equal to 256. Primitives in Java are a string of bytes, their sequence determining the value of the primitive.

#### Primitive Table ####

| Name | Size | Examples |
|:-----|:-----|:---------|
| boolean | 1    | true, false |
| char(character) | 1    | 'a', 'b', 'c', '1', '2', '3' |
| short(short integer) | 2    | 1, -2, 3 |
| int(integer) | 4    | 1, -2, 3 |
| long(long integer) | 8    | 1l, -2l, 3l |
| float(floating point number) | 4    | 1.0f, 2.5f, 3.1415f |
| double(double precision floating point number) | 8    | 1.0, 2.5, 3.1415926535 |

You may be wondering, what's with all these different types, and why does it seem like their are storing the same type of data some times. The different is how much each type can store. A short can only store integers in the range [-32768, 32768], whereas a long can store in the range [-9223372036854775807, 9223372036854775807]. After seeing this, you may be wondering, if a long can store that much more, why bother even considering the short or the int? The problem is that computers only have a finite amount of memory, so if we use more longs, the more memory it would take up, as the size of a long is 4 times larger than that of a short. For the most part, we will stick to the following data types:

  * boolean
    * A boolean store either true or false. This will be very useful as you will see later.
  * char
    * A char(acter) can store any ASCII value( basically anything you see on your keyboard, as well as a few special character, such as '\n" which is a new line, or '\t' which is a tab.
  * int
    * An int(eger)  can store any integer. This means the number can be both positive and negative, but has to be whole, or not have anything in the denominator.
  * double
    * A double (precision floating point numbers) can store any number (except imaginaries) in decimal format.

### Operations ###

Just like in math, you can manipulate these primitives with operators. **Operators** are fantastic little symbols that tell the computer to do something.

For instance, in math, we see the expression 2 + 5, and we automatically think 7! Now remember this. You basically substituted the whole expression (2 + 5) for a single value i.e. 7. You will see this concept come into play in many ways in programming.


#### Basic Operators ####
| Name | Symbol | Valid Primitives | What it does | Example |
|:-----|:-------|:-----------------|:-------------|:--------|
| Add  | +      | int, double, char | returns the sum of the symbol on the left side to the symbol on the right | 1 + 2 = 3 |
| Subtract | -      | int, double, char | returns the difference of the symbol on the left with the symbol on the right | 1 - 2 = -1 |
| Multiply | `*`    | int, double, char | returns the product of the symbol on the left with the symbol on the right | 1 `*` 2 = 2 |
| Divide | /      | int, double, char | There are 2 types of divisions. Integer division is used if both symbols are ints, and it returns how many of the whole symbol on the right can fit in the symbol on the right. The other is Floating Point Division, which returns the value much like how you would divide in regular math. | 1 / 2 = 0(integer division), 1.0/2.0 = 0.5(floating point division) |
| Modulus | %      | int, double, char | returns the remainder when the left symbol is divided by the right symbol | 10 % 3 = 1 |

#### Logic Operators ####
| Name | Symbol | Valid Primitives | What it does | Example |
|:-----|:-------|:-----------------|:-------------|:--------|
| Not  | !      | boolean          | returns the opposite of the the symbol on the right | !true = false |
| Or   | `|``|` | boolean          | returns whether at least one of the symbols surrounding it are true | true `|``|` false = true |
| And  | `&&`   | boolean          | return whether both symbols surrounding it are true | true `&&` false = false |
| Equals | `==`   | boolean, int, double, char | returns whether the symbol on the left has the same value as the symbol on the right | 1 `==` 2 = false |
| Less Than | `<`    | int, double, char | returns whether the symbol on the left is smaller than the symbol on the right | 1 < 2 = true |
| Greater Than | `>`    | int, double, char | returns whether the symbol on the left is greater than the symbol on the right | 1 > 2 = false |
| Less Than Equal To | `<=`   | int, double, char|return whether the symbol on the left is smaller or equal to the symbol on the right | 1 <= 2 = true |
| Greater Than Equal To | `>=`   | int, double, char | returns whether the symbol on the right is greater or equal to the symbol on the right | 1 >= 2 = false |

#### Miscellaneous ####
| Name | Symbol | Valid Primitives | What it does | Example |
|:-----|:-------|:-----------------|:-------------|:--------|
| Parenthesis | (expression) | N/A              | returns the evaluated expression inside | 1`*`(2+3) = 5 |

## Procedural Code ##

On a low level, coding is just giving the computer some instructions to fulfill, and the computer will execute those instructions one by one from top to bottom. I refer this this kind of code as procedural code, which will make up the bulk of your code.

### Variables ###

Okay, so in order to explain these concepts, I will refer to mathematics quite often. In terms of variables, variables in programs are very similar to those we use in math. They contain a name-usually in math, we use x, y, z, etc.- that acts as a replacement for actually calling the value.

So, if I did `x = 1`, I know the expression `(x+2)*2 = 6` because `(1+2)*2 = 6`.

However, there are a few differences in convention to consider when creating variables in programming. Variables in programming have to have a set data type. Additionally, the naming convention is a little different from that of math. Instead of using single characters, we use a whole words and format it with **Camel Case**.

For names, we use something called lowercase Camel Case. Here is some examples:

```
helloWorld, meaningOfLife, iLoveCamelCase
```

As you can tell, the first word is lowercase, and every word following is capitalized and appended directly after the word before it. Uppercase Camel Case is the exact same thing except the first character is capitalized.

#### Declaring Variables ####

When we say declaring a variable, it means we are saying this variable exists, or we are declaring it into existance. Just like how until, in math, we say x = 2, x does not exist to us. Same with programming, except in a **declaration**, we don't have to immediately assign a value, as you will see.

Let's say I wanted to declare a variable that stores my age. I can do this by declaring a variable.

int myAge;

Now, we can refer to myAge anytime we want after within the variables scope(a concept we will learn later). So, to give you a wholistic idea of declaration, the general syntax is this:

```
<dataType> <referenceName>;
```

So now we know how to declare a variable, we'd probably want to learn how to modify and work with it, so we will go over some basic operators.

#### Operators ####

Operators allow us to modify variables. There are quite a few of them, but you will only need to know one.

`=`   The mighty assignment operator. It takes the value of the symbol on the right and COPIES that value, plopping it into the symbol on the left. After declaring a variable, the process of assigning it a value is known as **instantiation**. Additionally, the whole expression returns the values of the symbol on the left and right(seeing how they are the same value, this is one value) so we can chain this operator. Here's an example:

```
int howMuchForAFootLong;
howMuchForAFootLong = 5;
```

So, when reading this code, we would say we declare a variable called howMuchForAFootLong. In the next line, we assign the value 5 to howMuchForAFootLong. Notice how I read the assignment from right to left, instead of the usual left to right. Now, to give you a more intricate example. Consider the following:

```
int a;
int b;
a = 2;
b = 3;
a = b;
b = 5;
```

What is the ending values of a and b? Well, people would think both would be 5 and 5, because we assigned b to a, and so, one might think that when b is assigned 5, a will be assigned 5 too. This is simple not the case. Remember, the assignment operator ALWAYS takes a copy of the value of that variable and then assigns it, so in the line `a = b;`, what's actually happening is we copy the value of b, which at the moment was 3, and assign that to a, so a is now 3. When b is assigned 5, nothing happens to a, so a = 3 and b = 5.

Oh, one more thing. You can declare and instatiate a variable in the same step. This is really easy and really intuitive:

```
int x = 5;
```

But don't go crazy with this power. Often times, especially in classes, we'd want to instantiate the variables seperately.