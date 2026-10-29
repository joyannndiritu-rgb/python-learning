# python-learning
this repository show my progress as i learn python.it may seem that some steps are skipped and thats true beccause this is where i started tracking my work.
### 01-basics/pin_extractor.py

**What it does:** Takes a list of poems and extracts a secret PIN from each one, returning the PINs as a list.

**How it works:**
1. Each poem is split into lines, and each line is split into words.
2. Every line has an index: the first line is 0, the next is 1, then 2, and so on.
3. For each line, the program takes the word at the same index as the line. Line 0 uses word 0, line 1 uses word 1, line 2 uses word 2.
4. It then counts the number of letters in that word, and that number becomes one digit of the PIN.
5. If the line is too short to have a word at that position, a `0` is added instead.
6. The digits are joined together to form the PIN for that poem, and all the PINs are collected in a list.

**Example:**

```
Stars and the moon
shine in the sky
white and
until the end of the night
```

- Line 0: word 0 is "Stars", which has 5 letters, so the digit is **5**
- Line 1: word 1 is "in", which has 2 letters, so the digit is **2**
- Line 2: "white and" has no word at index 2, so the digit is **0**
- Line 3: word 3 is "of", which has 2 letters, so the digit is **2**

PIN: `5202`

**Output for the three test poems:** `['5202', '3346', '50000']`

**How to run:**
```
python 01-basics/pin_extractor.py
```

**What I learned:** How to split strings into lines and words, use `enumerate()` to get each line's index, build a result step by step in a loop, and handle lines that are too short with `else`. The hardest part was understanding that each digit comes from the length of one specific word, chosen by the line's index.
