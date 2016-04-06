
#Python String Methods
Let's explore how to use some string methods in Python to modify or gain information about strings.

#Objectives:
+ Describe the syntax of strings in Python
+ Get data from the user
+ Concatenate strings
+ Interpolate with str.format()
+ Explain style guide and escape characters


##Printing Strings
The `print()` method will display a string in your command prompt. This is great for testing small parts of code at a time.

```python
>>>print 'hello, world!'
hello, world
```

##User Input
In Python, if you want to get text from a user, you can use the raw_input() or input() function, depending on your Python version.
To check your version, just type `python --version` into the command line. You will get something like 'Python 3.X.X or Python 2.X.X'
* input() is for Python version 3 and higher
* raw_input() is for Python versions lower than 3
Let's try it out!
For python 3+:

```python
>>> name = input('Who are you? ')
Who are you? Sergey
>>> name
'Sergey'
```

Python 2+:
```python
>>> name = raw_input('What is your name?')
What is your name? Larry
>>> name
'Larry'
```

Mini Challenge: See if you can write a short Python script that prompts a user for their name, their age, and their favorite food, and then returns a string combining this information.

##String Concatenation
Concatenation (joining strings together) is one of those things that might seem intuitive to a human but needs to be spelled out explicitly for the computer. For instance, when we run the code below, we will get `onetwo`.

```python
new_str = 'one' + 'two'
print new_str
=> onetwo
```
Python doesn't add anything extra - if you want a space between your words, you need to put it there!

When you try to concatenate a string with a datatype other than another string you will get an error.
```
TypeError: cannot concatenate 'str' and 'int' objects
```

##Substrings
A substring is a part of a string.  To get a substring from a string, use square brackets and specify the range of characters that you want from the string. Just like in Javascript, string characters are indexed starting at 0.

Grabbing a specific character:
```python
>>> old_str = 'superfly'
>>> old_str[0]
"s"
>>> print old_str[3]
"e"
```

Grabbing a substring of a range of characters:
```python
>>> old_str = 'superfly'
>>> print old_str[0:4]
'supe'
```
As you might be able to guess, the selection works like this:
```python
<string>[<first character position>: <last character position +1>]
```
Here are a couple handy shortcuts for selecting particular parts of strings:

```python
new_str = "superfluous"
>>> new_str[3:] # character position 3 to the end
'erfluous'
>>> new_str[:5] # From the beginning to character position 4
'super'
```
##String Length

Python gives us the len() function to determine a string's length. The `len()` function will count the number of characters in the string, including spaces and newline characters"

```python
>>> short_string = "o"
>>> long_string = "(pumba) When I was a young warthog… (timon) When he was a young waaarthoooooooooooooog!"
>>> len(short_string)
1
>>> len(long_string)
89
```
## Split
The split function, `split()` divides a string into smaller parts. The method's default is to divide on whitespace, but other separators can be included as an argument. 
```python
>>> words="This is a sentence".split() #since there is no argument, we are splitting on whitespace.
>>> words
['This', 'is', 'a', 'sentence']

>>> ingredients="jelly, peanut butter, bread".split(',') # we are using a comma as the divider here.
>>> ingredients
['jelly', ' peanut butter', ' bread']
```

##Replace Function
The `replace()` method is a handy Python tool that allows you to substitute a word or letter for another word or letter within a string. That means *every time the word or letter appears in the string, it will be substituted out.* 

This method takes two `parameters`. The first one is the word you want to replace, and the second one is the word you want to replace it with.


```python
>>> pygmalion = 'the rayn in Spayn stays maynly in the playn'
>>> new_pygmalion = pygmalion.replace('ayn', 'ain')
>>> new_pygmalion
'the rain in Spain stays mainly in the plain'
```


## Lower and Upper Function
lower() and upper() make strings lowercase and uppercase respectively.

```python
>>> old_str = 'Seattle Seahawks'
>>> print  old_str.lower()
seattle seahawks
>>> print old_str.upper() + '!!!'
SEATTLE SEAHAWKS!!!
```

## Strip Function
The strip() function removes leading and trailing white space.
```python
>>>'     spaces everywhere     '.strip()
'spaces everywhere'
```


# Conclusion
There are a lot of string methods that we can access in Python. Whenever you don't remember if one exists, or the syntax, you can always look up the documentation.
