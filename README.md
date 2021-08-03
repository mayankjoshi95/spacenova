# spacenova

Find out the 6th letter of s from starting and 6th letter from end and store in ans2 and ans3 respectively
s = "Spaceonova where limit tends to infinity"
store=[]
for i in range(6):
    store.append(s[i])
ans2=store
num=[]
for i in range(len(s)-6,len(s),1):
    num.append(s[i])
ans3=num




You are given two lists x and y. Sort x in ascending order and sort y in descending order. Then store the concatenation in ans5
x=[3,5,1,9,7,4]
y=['limit','tends','to','infinity']
z=sorted(x)
b=sorted(y,reverse=True)
ans5=z+b





You are given a list p.
Change 3rd element in p to rock.
Add boss in the end of list.
Add another element don't after you
And store the result in ans6 as a string by adding '#' between every element
#ans6=None
p=['you','definitely','too','inside','of me']
p[2]='rock'
p.append('boss')
p.insert(1,"don't")
for i in range(1,2*len(p)-1,2):
    p.insert(i,'#')
    
print(len(p))
p





Given a number n, and a function f1(), you must complete the function to return a list from [1,n]

+1
def f1(n):
    l=[]
    for i in range(1,n+1):
       l.append(i)
    return l
    # YOUR CODE HERE
    
#Tests
assert f1(2)==[1,2]
assert f1(3)==[1,2,3]





Write a function f2(), which checks whether a number n is prime or not, it must return True if prime, else False if not a prime.
Note: 1 is considered to be Non-Prime

import math
def f2(n):
    if n%2==0 and n>2:
      return False
    for i in range(3,int(math.sqrt(n))+1,2):
        if n%i==0:
            return False
    return True    
#Tests
assert f2(2)==True
assert f2(4)==False





Ex1: if the list is ['abc','pkonh','aqwetmkoi'], then the middle char of each element is 'b','o','t' repectively hence the original string is "bot"

def f3(l):
  g=[]
  
  for j in range (len(l)):
    i=0
    for i in range(len(l[j])):
        if i==(len(l[j])-1)/2:
         g.append(l[j][i])
         
            
  return ''.join(g) 
p=f3(['abc','pkonh','aqwetmkoi'])
p







This is an interesting question, you are given a string s all in lower case
Make a dictionary storing the frequency of each letter in the string
Complete f4() and return the dictionary
Eg:
If s="abc",
d={'a':1,'b':1,'c':1}
And so on

def f4(s):
    d={}
    r=s.split()
    t=s.split()
    
    
    for i in range(len(r[0])):
      count=0        
  
      for j in range(len(r[0])):
            
            if r[0][i]== t[0][j]:
             count+=1
            d[r[0][i]]=count
    return d
    
    
    
    
    
    
    
    
    Now, let us come to the real question

HackTheBox really loves strings a lot but they likes palindromic strings more. Today, they took two strings X and Y, each consisting of lower case alphabets.

Now they took a substring from X which is not empty let us say x and they took another substring from Y (which is again non empty) which is let us say y and then they did the concatenation of x and y and called it z Now they want to know whether this z is pallindrome or not

You will be given two string X and Y and return True if it possible to choose such string z else False

-- 3 points
def f5(x,y):
    z=x+y
    if z==z[::-1]:
        return True
    else:
        return False
    
v=f5('abc','abc') 
v







HackTheBox can not get enough of strings. They took a string s and did this and gave you encoded

l=list(s)
for i in range(len(l)):
    l[i]=chr(ord(l[i])+i)
encoded="".join(l)

Can you return the original string through f7(encoded)?
Read about ord() From here
Read about chr() From here

def f7(encoded):
    l=list(encoded)
    for i in range(len(l)):
      l[i]=chr(ord(l[i])-i)
    z="".join(l)
    return z
s=f7("def")
s
