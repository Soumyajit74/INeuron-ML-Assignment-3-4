# INeuron-ML-Assignment-3-4
#Assignment 3

#1.1 Creatng my own myreduce function
def myreduce(func, lst):
    x=lst[0]
    for i in range(1,len(lst)):
        x = func(x, lst[i])
        print(x)
    return(x)
#testing
myreduce(lambda a,b: a+b, [1,2,3,4,5,6,7,8,9])

#1.2 Write a Python program to implement your own myfilter() function which works exactly
#like Python's built-in function filter()
#Creating myfilter
def myfilter(func, lst):
    lst1=[]
  
    for i in (lst):
        if  func(i):
            lst1.append(i)
    return(lst1)
list(myfilter(lambda x: x%2==0, [1,23,43,54,66,75,99,34,12,100,42,70]))


#2. Implement List comprehensions to produce the following lists.
#Write List comprehensions to produce the following Lists
#['x', 'xx', 'xxx', 'xxxx', 'y', 'yy', 'yyy', 'yyyy', 'z', 'zz', 'zzz', 'zzzz']

lst1=['x', 'y', 'z']
lst2=[]
for i in range(len(lst1)):
    for j in range(1,5):
        lst2.append(lst1[i]*j)

print(lst2)

#Creating ['x', 'y', 'z', 'xx', 'yy', 'zz', 'xxx', 'yyy', 'zzz', 'xxxx', 'yyyy', 'zzzz']
lst1=['x', 'y', 'z']
lst2=[]

for i in range(1,5):
     for j in lst1:
        lst2.append(i*j)
lst2

#creating[[2], [3], [4], [3], [4], [5], [4], [5], [6]] [[2, 3, 4, 5], [3, 4, 5, 6],[4, 5, 6, 7], [5, 6, 7, 8]]

lst1=[2, 3, 4]
lst2=[]
lst3=[2, 3, 4, 5]
lst4=[]
for i in lst1:
    for j in range(0,3):
        lst2.append([i+j])


lst4.append([ [x+y for x in lst3] for y in range(0,4)  ])

print(lst2, lst4)

#creating[(1, 1), (2, 1), (3, 1), (1, 2), (2, 2), (3, 2), (1, 3), (2, 3), (3, 3)]
lst1=[1,2,3]
lst2=[]
for i in lst1:
    for j in lst1:
        lst2.append((j,i))
lst2






#Assignment 4
#Defining class polygon
#1.1
class polygon:
    def __inti__(self, a, b, c):
        self.a= float(a)
        self.b= float(b)
        self.c= float(c)
a= int(input("a="))
b= int(input("b="))
c= int(input("c="))

#Defining class triangle
class triangle(polygon):
    
    def __int__(self, a, b, c):
        polygon.__init__(self, a, b, c)
            
    
    def get_area(self):
        s = (a + b + c) / 2
        return (s*(s-a)*(s-b)*(s-c)) ** 0.5 

t = triangle()
print("area : {}".format(t.get_area()))


#1.2 Write a function filter_long_words() that takes a list of words and an integer n and returns
the list of words that are longer than n.
#1.2
def long_filter_longwords(str, num):
    words=[]
    for i in range(len(str)):
        
        if len(str[i])>num:
            words.append(str[i])
        
    return words
str=["wolf", "elephant", "zebra", "hyena", "dog", "leaopard", "human", "chicken"]
num=5
long_filter_longwords(str, num)



#2.1 Write a Python program using function concept that maps list of words into a list of integers
representing the lengths of the corresponding words.

def letter_counter(str):
    word_num=[]
    for i in range(len(str)):
        word_num.append(len(str[i]))
    
    return word_num
str= ["ab","cde","erty"]  
letter_counter(str)



#2.2 Write a Python function which takes a character (i.e. a string of length 1) and returns True if
it is a vowel, False otherwise.

def vowel_detector(char):
    if char in ('a', 'e','i','o','u'):
        return True
    else:
        return False
    
char = input("Enter character of choice:")
vowel_detector(char)


