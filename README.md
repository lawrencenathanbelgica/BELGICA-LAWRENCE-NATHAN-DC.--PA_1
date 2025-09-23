# BELGICA-LAWRENCE-NATHAN-DC.--PA_1

# Programming Assignment (PA#1)

The purpose of this assignment is to practice basic Python concepts such as string manipulation, dictionaries, list unpacking, and user input. This README serves as a guide to explain what each program does, the logic behind the solutions, and how to run them.  

This repository contains my submission for **Programming Assignment #1** in  
**ECE 2112: Advanced Computer Programming and Algorithms**.  



### About the Files

- **alphabet_soup.py** → Solves the Alphabet Soup Problem.
- **emoticon.py** → Solves the Emoticon Problem.
- **unpacking_list.py** → Solves the Unpacking List Problem.
- **README.md** → Documentation explaining the logic, code, and usage.
  
## 1. Alphabet Soup Problem  
**Goal:** Arrange the letters of a given word in alphabetical order.  

**Process:**  
1. Ask the user to input a word.  
2. Use Python’s built-in `sorted()` function to arrange the letters.  
3. Join the sorted letters back into a string using `"".join()`.  
4. Print the result.  

**Code Snippet:**  
```python
word = input("Enter a word: ")
sorted_word = ''.join(sorted(word))
print(" ", sorted_word)
```

Explanation of Code

- input() → asks the user for a word.
- sorted(word) → sorts the letters alphabetically.
- "".join() → joins the letters back into one string.
- print() → displays the result.
  
**Example Run:**  
```
Input: thequickbrownfoxjumpsoverthelazydog
Output:  abcdeeefghhijklmnoooopqrrsttuuvwxyz
```


## 2. Emoticon Problem  
**Goal:** Replace specific words in a sentence with their corresponding emoticons.  

**Process:**  
1. Create a dictionary where keys are words (`"smile"`, `"grin"`, `"sad"`, `"mad"`) and values are the emoticons (`":)"`, `":D"`, `":(("`, `">:("`).  
2. Ask the user to enter a sentence.  
3. Loop through the dictionary and replace each matching word with the emoticon.  
4. Print the converted sentence.  

**Code Snippet:**  
```python
def emotify(phrase):
    emoticons = {"smile": ":)", "grin": ":D", "sad": ":((", "mad": ">:("}
    for word, symbol in emoticons.items():
        phrase = phrase.replace(word, symbol)
    return phrase

phrase = input("Enter a phrase or sentence: ")
print(emotify(phrase))
```

**Example Run:**  
```
Input: Last night I was feeling mad, but this morning I got really sad.
Output: Last night I was feeling >:(, but this morning I got really :((
```


## 3. Unpacking List Problem  
**Goal:** Take a list of numbers and unpack them into three variables: `first`, `middle`, and `last`.  

**Process:**  
1. Ask the user to input numbers.  
2. If the input contains spaces, split it normally.
3. If not, split each digit separately.  
4. Convert the input into a list of integers.  
5. Assign the first element to `first`, the last element to `last`, and everything in between to `middle`.  
6. Print the results.  

**Code Snippet:**  
```python
user_input = input("Enter numbers: ")

if " " in user_input:
    lst = list(map(int, user_input.split()))
else:
    lst = list(map(int, user_input))

first, middle, last = lst[0], lst[1:-1], lst[-1]

print("first:", first)
print("middle:", middle)
print("last:", last)
```

**Example Run:**  
```
Input: 97458125
Output:
first: 9
middle: [7, 4, 5, 8, 1, 2]
last: 5
```

## How to Run the Programs  
1. Clone this repository or download the Python file.  
2. Run it using:  
   ```bash
   python filename.py
   ```
   (Replace filename.py with the actual file name.)
3. Follow the prompts to test each problem. 
