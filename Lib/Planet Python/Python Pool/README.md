Python Pool

3 Proven Ways to Convert ASCII to String in Python


Introduction

In python, we have discussed many concepts and conversions. But sometimes, we come to a situation where we need to convert ASCII into string in python. In this tutorial, we will be discussing how to convert ASCII into strings in python. As the conversion of elements has been a handy utility as it offers it in a much simpler way than other languages.

What are ASCII Values?
ASCII stands for American Standard Code for Information Interchange. It is a character encoding that uses numeric codes to represent characters from 0 to 127. These include upper and lowercase English letters, numbers, and punctuation symbols. For example, the ASCII code for character A is 65, and Z is 90.

Ways to convert ASCII into string in python
Here, we will be discussing all the different ways through which we can convert ASCII into string in python:

1. Using chr() function to convert ASCII into string
In this example, we will be using the chr() function with ASCII value as a parameter to function. We will be taking an input list with some integer values. After that, we will be using the chr() function, which will convert the ASCII values into integers. At last, we will print the resultant string. Let us look at the example for understanding the concept in detail.

# Input list
lst = [80, 121, 116, 104, 111, 110,
		80, 111, 111, 108]

# Printing initial list
print ("Input list", lst)

# Using chr() Method
res = ""
for i in lst:
	res = res + chr(i)

print ("String : ", str(res))
Output:

chr() function to convert ASCII into string
Explanation:

Firstly, we will be taking an input list with some ASCII values.
Then, we will be printing the input list.
Then, we will be taking an empty string res.
After that, we will apply for loop till the length of string, and inside it, we will be using the chr() function to convert ASCII value into character value.
At last, we will print the Final string.
Hence, you can see the ASCII values get converted into a string.
2. Using join and list comprehension to convert ASCII into string
In this example, we will be using join and list comprehension with the help of the chr() function to convert each ASCII value to its corresponding character. join(iterable) method with str as "" to concatenate each character in iterable into a single string. At last, we will print the final string. Let us look at the example for understanding the concept in detail.

# Input list
lst = [80, 121, 116, 104, 111, 110,
		80, 111, 111, 108]

# Printing input list
print ("Initial list : ", lst)

# Using list comprehension and join
res = ''.join(chr(i) for i in lst)

print ("Final string : ", str(res))
Output:

join and list comprehension
Explanation:

Firstly, we will be taking an input list with some ASCII values.
Then, we will be printing the input list.
After that, we will be taking a variable ‘res’ to apply the join() method.
Inside the join() method, We have used list comprehension, which will convert the ASCII into the string.
At last, we will print the Final string.
Hence, you can see the ASCII values get converted into strings.
3. Using map() function to convert ASCII into string
In this example, we will be using the map() function and join() method to convert each ASCII value to its corresponding character. join(iterable) method with str as " " to concatenate each character in iterable into a single string. At last, we will print the final string. Let us look at the example for understanding the concept in detail.

# Input list
lst = [80, 121, 116, 104, 111, 110,
		80, 111, 111, 108]

# Printing input list
print ("Initial list : ", lst)

# Using map and join
res = ''.join(map(chr, lst))

print ("Final string : ", str(res))
Output:

map() function to convert ASCII into string
Explanation:

Firstly, we will be taking an input list with some ASCII values.
Then, we will be printing the input list.
After that, we will be taking a variable ‘res’ to apply the join() method.
Inside the join() method, we have used the map() function through which ASCII values get converted into strings.
At last, we will print the Final string.
Hence, you can see the ASCII values get converted into strings.
Conclusion
In this tutorial, we have learned about the concept of conversion of ASCII into string in python. We have also discussed what ASCII values are? Then, we have discussed all the different ways with the help of an example through which we can convert ASCII values into strings in python. All the ways are explained in detail with the help of examples. You can use any of the functions according to your choice and your requirement in the program.

However, if you have any doubts or questions, do let me know in the comment section below. I will try to help you as soon as possible.

FAQs
1. How to check if a string in Python is in ASCII?
We can check if the string in python is ASCII or not with the help of the following code:

def is_ascii(s):
    return all(ord(c) < 128 for c in s)
In this, s is the string through which you can check if the python string is ASCII or not. You can write any of the strings and run the program. It will give you the output in True or False.

2. Are python strings ASCII?
Python strings have no property corresponding to ‘ASCII’ or any other encoding. The input of your string (whether you read it from a file, input from a keyboard, etc.) may have encoded a Unicode string in ASCII to produce your string. In case you want to remove all the Unicode characters from the string in python. You can read our in-depth article from here.

3. What does chr() do in Python?
The chr() function in python inputs as an integer, a Unicode code point, and converts that into a string representing a character. This function is used to return a string with length 1, representing the character whose Unicode code point value is passed in the chr() function.

The post 3 Proven Ways to Convert ASCII to String in Python appeared first on Python Pool.

April 26, 2021 02:37 PM UTC
