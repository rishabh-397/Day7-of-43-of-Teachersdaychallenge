# Day7-of-43-of-Teachersdaychallenge
💡 Codeforces Problems

1)4A. Watermelon
Problem Description: Pete and Billy want to divide a watermelon of weight w into two parts, each weighing an even number of kilos. Both parts must have positive weight. Determine if this is possible.

Key Idea/Logic:

The sum of two even numbers is always an even number. Therefore, if the total weight w is odd, it's impossible.

If w is even, say w = 2k, we need two even positive numbers p1 = 2a and p2 = 2b such that 2a + 2b = 2k, which simplifies to a + b = k.

Since p1, p2 > 0, a >= 1 and b >= 1. This implies k must be at least 2 (i.e., a+b >= 2).

Thus, w must be even and w > 2. If w = 2, the only way to divide it into two positive integer parts is 1 + 1, and 1 is not even.

Solution Condition: The answer is "YES" if w is an even number AND w is greater than 2. Otherwise, the answer is "NO".

Time Complexity: O(1) (constant time for a few arithmetic operations)

Space Complexity: O(1)

Example:
Input: 8
Output: YES (e.g., 2 and 6, or 4 and 4)

2. 7A. Way Too Long Words
Problem Description: Replace "too long" words (strictly more than 10 characters) with an abbreviation. The abbreviation consists of the first letter, the count of letters between the first and last letters, and the last letter. Words that are not too long remain unchanged.

Key Idea/Logic:

Read the number of words (n).

Loop n times, reading one word at a time.

For each word, check its length.

If length > 10:

Take the first_char = word[0].

Take the last_char = word[length - 1].

Calculate middle_count = length - 2.

Form the abbreviation: first_char + string(middle_count) + last_char.

Else (length <= 10):

Print the word as is.

Time Complexity: O(N
cdotL) where N is the number of words and L is the maximum length of a word. (Each word is processed in time proportional to its length).

Space Complexity: O(L_max) for storing the current word, or O(1) if processing character by character.


Input
The first line contains an integer n (1 ≤ n ≤ 100). Each of the following n lines contains one word. All the words consist of lowercase Latin letters and possess the lengths of from 1 to 100 characters.

Output
Print n lines. The i-th line should contain the result of replacing of the i-th word from the input data.

Examples
InputCopy
4
word
localization
internationalization
pneumonoultramicroscopicsilicovolcanoconiosis
OutputCopy
word
l10n
i18n
p43s
