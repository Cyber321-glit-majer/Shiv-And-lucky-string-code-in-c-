# Shiv-And-lucky-string-code-in-python


Problem statement:

Shiv is your new boss and be likes lucky strings very much. A string is called lucky if and only if each character from first half of the string can be paired to each character from second half of the string, AND:

1. In each pair, a character from the first half is strictly greater than a character from the second half OR

2. In each pair, a character from the first half is strictly lesser than a character from the second half OR

3. In each pair, a character from the first half is equal to character from the second half.




Each character should be used exactly once in pairing

Your are given a string 5. You want to change the minimum number of characters to make this string lucky

so that you can gift it to your boss

Note that each character in lucky string should be in lower case alphabet ('a-2)

Input format:

The fig line consists of an integer N. The second line consists of N lower case characters.

Output formati

Print minimum number of changes required to make given string lucky


CODE: Python
n=int(input())
a=input()
arr=[]
less=0
more=0
equal=0
cap=0
for i in a:
 if i.isupper():
  cap+=1
  break
a=a.lower()
for i in range(len(a)//2):
 if(a[i]<a[i+len(a)//2]):
  less+=1
 elif(a[i]==a[len(a)-i-1]):
  equal+=1
 else:
  more+=1
 
print(n//2-max([less,more,equal])+cap)
