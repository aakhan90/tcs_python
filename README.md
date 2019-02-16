# tcs_python
code snippets for tcs python excersises functions and oops                               

Q.1)Convert the entire string zenPython into a list of words. Capture the words in the list - words

import re

from collections import Counter 

zenPython = '''
The Zen of Python, by Tim Peters
Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
'''
words=zenPython.split()   
print(words)                             

Q.2)Now, remove the flanking characters (such as , . - * ! and space) from each of the word, present in list words.Store the obtained result again in the list words  
-------- add below code in above code   
words=[re.sub('[^a-zA-Z0-9]+', '', _)  for _ in words]   
print(words)   

Q.3)Convert all the words of list words to lower case.Store the obtained result again in the list words  
-------- add below code in above code   
words=[s.lower() for s in words]   
print(words)  

Q.4)Determine the unique set of words from the list words.Store obtained unique words in the list unique_words.  
-------- add below code in above code  
unique_words = set(words)  
print(unique_words)  

Q.5)Calculate the frequency of each identified unique word in the list - words and store the result in the dictionary word_frequency.  
-------- add below code in above code   
word_frequency=Counter(words)  
print(word_frequency)  

Q.6)Create the dictionary frequent_words, which filter words having frequency greater than five from word_frequency.Finally print the dictionary frequent_words.  
-------- add below code in above code   
frequent_words=[x[0] for x in word_frequency.items() if x[1]>=5]  
print(frequent_words)  

