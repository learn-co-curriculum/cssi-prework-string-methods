
#Python String Methods
Let's explore how to use some string methods in Python to modify or gain information about strings.

#Objectives:
+ Understand the syntax of strings in Python
+ How to get data from the user
+ How to concatenate strings
+ How to interpolate with str.format()
+ Understand style guide and escape characters


##Printing Strings
The `print()` method will display a string in your command prompt. This is great for testing small parts of code at a time.

```python
>>>print 'hello, world!'
hello, world
```

#User Input
In Python, if you want to get text from a user, you can use the raw_input()/input() function, depending on your Python version.
To check your version, just type `python --version` into the command line. You will get something like 'Python 3.X.X or Python 2.X.X'
* input() is for Python version 3 and higher
* raw_input is for Python versions lower than 3
Let's try it out!
```python
>>> name = input('Who are you? ')
Who are you? Joseph
>>> name
'Joseph'
```


#String Concatenation
Concatenation (joining strings together) is one of those things that might seem intuitive to a human but needs to be spelled out explicitly for the computer. For instance, when I run the code below, I will get `onetwo`.

```python
new_str = 'one' + 'two'
print new_str
```
Python doesn't add anything extra - if you want a space between your words, you need to put it there!

When you try to concatenate a string with a datatype other than another string you will get an error.
```
TypeError: cannot concatenate 'str' and 'int' objects
```


#Substrings
A substring is a part of a string.  To get a substring from a string, use square brackets and specify the range of characters that you want from the string. Just like in Javascript, string characters are indexed starting at 0.

Grabbing a specific character:
```python
>>> old_str = 'superfly'
>>> print old_str[0]
s
```

Grabbing a substring of a range of characters:
```python
>>> old_str = 'superfly'
>>> print old_str[0:4]
su
```
As you might be able to guess, the selection works like this:
```python
<string>[<first character position>: <last character position +1>]
```
Here are a couple handy shortcuts for selecting particular parts of strings:
```python
>>> print old_str[3:] # character position 3 to the end
erfluous
>>> print old_str[:5] # From the beginning to character position 4
super
```
#String Length

Python gives us the len() function to determine a string's length.
```python
>>> short_string = "o"
>>> long_string = "(pumba) When I was a young warthog… (timon) When he was a young waaarthoooooooooooooog!"
>>> len(short_string)
1
>>> len(long_string)
89
```

#Replace Function
To replace one string with anohter, use the `replace()` method. `str.replace` takes two `parameters`. The first one is the word you want to replace, and the second one is the word you want to replace it with.
```python
>>> old_str = 'superfly'
>>> new_str = old_str.replace('super', 'SUPA')
>>> print new_str
SUPAfly
```

# Lower and Upper Function
lower() and upper() make strings lowercase and uppercase respectively.
```python
>>> old_str = 'Seattle Seahawks'
>>> print  old_str.lower()
seattle seahawks
>>> print old_str.upper() + '!!!'
SEATTLE SEAHAWKS!!!
```

#Strip Function
The strip() function removes leading and trailing white space.
```python
>>>print '     spaces everywhere     '.strip()
spaces everywhere
```

#String Formatting and Interpolation
String interpolation lets us pass different data into a string, which is faster and more convenient than keeping track of different pieces of string and concatenating them ourselves. There are two ways to do string interpolation. With the .format method and with the %s. Let's take a look at the difference.

## Interpolation with ***.format***
This is the newer version of using variables within string in Python. The method `.format()` is chained to the end of a string. The arguments of `.format()` are substituted into the placeholders of the string. The placeholders start and end with curly brackets. The placeholders can contain a named variable, a number, or nothing at all.

###Keyword Variables
For readability, keyword variables generally make the most sense in interpolation placeholders. In the example below, the string has one keyword argument, 'reading_materials', which is assigned to a global variable, 'magazine'.
```python
>>>magazine = "The Atlantic"
>>>print "I am always behind on {reading_material}".format(reading_material=magazine)
I am always behind on The Atlantic
```
The hobby example uses two keyword arguments: 'name' and 'hobby', which are assigned to strings within .format()
```python
>>>print "{name} is the best at {hobby}".format(name='Charlie', hobby='playing piano')
Charlie is the best at playing piano
```
###Positional Variables
There is also an option to use positional arguments. The advantage is that this is  a bit shorter to type, but harder for others to interpret.
```python
>>>print "There are {0} students at CSSI in {1}!".format(30, "New York")
There are 30 students at CSSI in New York!
```

You could also not include any value in the placeholder and achieve the same effect.
```python
>>>print "There are {} students at CSSI in {}!".format(28, "Cambridge")
There are 28 students at CSSI in Cambridge!
```

##String Interpolation with ***%s***
The older way to use variables in strings and uses the % operator.

Again the whole string is in quotes. The placeholder for the variable is a percent sign and the first letter of the datatype. (%d int, %s string, %f/%g float). The entire string is followed by a percent sign and the name of the variable

```python
>>>print "The %s have %d %s championships in %d years" %("Chicago",3, "NHL", 3)
The Chicago have 3 NHL championships in 3 years
```

# Conclusion
There are a lot of string methods that we can access in Python. Whenever you don't remember if one exists, or the syntax, you can always look up the documentation.

# References
[Python String Interpolation Guide] (https://mkaz.com/2012/10/10/python-string-format/)
