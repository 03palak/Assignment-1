**class 1**

print("hello world")# when we want to print string as it is then we use double or single inverted commas "",''


#creating a variable used to store data
a="hello everyone"  #string
print(a)
print(type(a))

num1=3387 #integer
num2=3376
sum=num1 + num2
print(sum)

num1=2234
num2=22.34
print(num1-num2)

**Class 2**

#boolean
print(10<9)
add=False
print(type(add))
name="jerry"
no=3
#Concatinating (adding up two string or combining the data)
print("Hello"+name,no)

#collection datatypes in python
#list,tuple,set ,dictionary
#list: ordered collection of datatypes,[],mutable(data is changeable in list)
 
mylist=["data","details","access"]#homogenous list(having same data type)
print(mylist)
mylist1=[366,True,"data"] 
print (mylist1)
print(mylist1+mylist)#concatenation

#update (mutable)
mylist1[1]=False
print(mylist1)

#Append(add data to end of the list)
mylist1.append("data1")
print(mylist1)

#insert (adding data at any position)
mylist.insert(0,300)
print(mylist)

#Delete
del mylist1[1]
print(mylist1)

mylist1.remove("data")
print(mylist1)

mylist.extend(mylist1)
print(mylist)

#Indexing (indexd no. alsways starts with zero)
mylist1+[366, 476.0,True,"data"]
print(mylist1[1])#+ve indexing
print(mylist1[-1])#-ve indexing


**Class 3**

#tuple: ordered collection of datatype,()are used, it is immutable(its like list)#it means once you access the data then no one can modify or update it.
_tuple_=("dell","asus","hp",27,387,87)
print(_tuple_)
 
 #tuple does not support append ,update, insertion ,deletion.(we cannot delete one element but we can delete the whole tuple) 
 #we get to know that the function is immutable or unchangable if it use normal bracket()........else if it have{},[] it is changable.



#Dictionary : it consists of key and values,mutable 
#we will not use add as well as append

Dict={
    "Username":["Admin","Admin1"],
    "password":"pass",
    "os":"windows",
    "Ram":"128GB"

}
print(Dict["Username"])

#Update
Dict["password"]=12234
print([Dict])

del Dict["os"]
print(Dict)

#index number: prints individual elements.
#slicing: printing the sequence of elements.

a="ramdomness"
print(a[0:100])
print(a[3:])
print(a[:3])
print(a[-9:-1])
print(a[-10:])

#step indexing

b="python"
print(b[::-2])

**class 4**

#set: unordered collection of datatypes ,{},mutable,index value will not work and it does not show data multiple times,we can't delete specific data in set.
myset={"A","B","C","A",3241}
print(myset) #output will not get in same order.
print(len(myset))


#here append will not work but add will work
myset.add(True)
print(myset)

#Frozenset

#empty set ;we just use()
var=set()
print(var)
var.add("add")
print(var)

#union and intersection
set1={0,True,"Data"}
set2={"Data","tasl","status"}
set3=set1.union(set2)
set4=set1|(set2)
print(set3)
print(set4)


set3=set1.intersection(set2)
set4=set1&(set2)
print(set3)
print(set4)
set1.clear()

set1=()


set1=128
set2=200
print(set1!=set2)
print(set1>=set2)
print(set1==set2)
print(type(set1))

**class 5**

#function: a set in which code is executed whenever it is called
print("hello")
print("hello")
print("hello")


def func():
  for x in range(5):
    print("task is done")
    print("work is completed")
func()    

list1=[2,3,5,7,9,"data",0]
print(list1[0])
print(list1[2])
print(list1[3])
print(list1[5])


for values in list1:
  print(values)


#iteration:way to print data one by one
list1=["a","b","c","d"]
myiterartion=iter(list1) 
print(next(myiterartion))

myiterartion=iter(list1) 
print(next(myiterartion))

class 6


#keyword arguments

def key(name,marks,subject):
 print("hii my name is",name,"and i scored",marks,"in",subject)
key(marks="100 marks",subject="maths",name="Tom")

#default arguments
def awesome(name="palak",city="rath",describe="distict hamirpur"):
  print("hey i am",name,"from",describe,city)
awesome()

def awesome(name,city="rath",describe="distict hamirpur"):
  print("hey i am",name,"from",describe,city)
awesome(honey,noida,glbajaj)




def func(teacher,*a):
  print("The teacher name is",teacher)
  for rollno in a:
   print("The students are",rollno)
func("Tom","RHTF",1,2,3,4,5,6,7,8)    

def func(teacher,*a,**skdj):
  print("The teacher name is",teacher)
  for rollno in a:
   print("The students are",rollno)
  for subject in skdj:
    print(subject,skdj[subject])
    print(subject) 
func("Tom",1,2,3,4,5,6,7,8,science=10,maths=20)    

#sequence
list=["A","R","D"]
print("A" in list)
print("E" in list)
list1=[1,2,4,6,8]
print(2 in list1)
print(3 not in list1)
print(len(list1))

seq="hellol"
print(seq.index("l"))#this show pos of l which shown first
print(seq.index("l",3))#pos after or in 3
print(seq.index("l",4))#pos after or in 4

b=[1,2,3,4,8,6,8,9,8,20,356]
print(b.index(8,5,10))

#files: to store data
#read mode (r):you can only read data you can't add anything.
#write mode(w):  you can write but the previous data gets deleted
#append mode(a): you can add data in the previous one


myfile=open("file.txt","r")
print(myfile.read())

myfile.close()

myfile=open("file.txt","w")
myfile.write("developind a game\n")

myfile=open("file.txt","r")
print(myfile.read())

myfile=open("file.txt","a")
myfile.write("palak")

myfile=open("file.txt","r")
print(myfile.read())

#context manager
with open("file.txt") as file1:
  print(file1.read())
  print(myfile.read())

mylines=["tast is been scheduled\n","status of the task\n","good to go"]
with open("file.txt","a") as file1:
  file1.writelines(mylines)
file1=open("file.txt","r") #or with open("file.txt","r") as file1: 
print(file1.read())  

#modules: it is a predefined function
#built in function
import math 
print(math.sin(1))
print(math.pi)

import datetime
x=datetime.datetime.now()

print(x)
print(x.strftime("%d"))
print(x.strftime("%m"))
print(x.strftime("%y"))
print(x.strftime("%u"))
print(x.strftime("%w"))
print(x.strftime("%a"))

class 7
