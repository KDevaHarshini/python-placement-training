# python-placement-training
my_set={1,2,3}            #set with curly braces
print(my_set)
another_set=set([3,4,5])          #set using set() constructor
print(another_set)
set2={1,2,3}
set2.add(4)               #adds 4 to set
print(set2)

#remove element from set
set2.remove(2)
print(set2)
set2.discard(2)
print(set2)
set2.remove(3)       #throws error if ele is not present
print(set2)
set2.discard(10)      #do not throw error if ele is not present and prints the same set
print(set2)
set3={6,7,8}
set4={6,9,3}
union=set3|set4
print(union)
intersection=set3&set4
print(intersection)
difference=set3-set4
print(difference)

#
stu_score=int(input("Enter student score:"))
if stu_score>=90:
  print("A")
elif stu_score>=80 and stu_score<=89:
  print("B")
elif stu_score>=70 and stu_score<=79:
  print("C")
else:
  print("D")

  
#Dictionaries:
dict1={"name":"Alia","age":20,"address":"banglore"}
print(dict1)
#access
address=dict1["address"]  #banglore
print(address)
age=dict1["age"]          #20
print(age)
dict1={"name":"alia","age":20}
new_data={"address":"banglore","gender":"female"}
dict1.update(new_data)  #merges new_data into my_dict
print(dict1)

#
#year=int(input("Enter year:"))
#if year%4==0 and year%100!=0 or year%400==0:
  #print("Leap year")
#else:
  #print("not leap year")


   #program that takes a password as input and checks if it is strong or weak.a strong password has atleast 8 characters,incudes both upper and lowercase letters,and contain atleast one digit
   METHOD 1:
length,u,d=0,0,0
char=input("Enter Password:")
if(len(char)>=8):
  for i in char:
    length+=1
    if(i.isupper()):
      u+=1
    if(i.islower()):
        d+=1
if(length>=1 and u>=1 and d>=1):
  print("valid password")
else:
  print("invaid password")

  METHOD 2:
  password=input("Enter a password:")
length=len(password)>=8
uppercase=any(char.isupper() for char in password)
lowercase=any(char.islower() for char in password)
digit=any(char.isdigit() for char in password)
if length and uppercase and lowercase and digit:
  print("Strong password")
else:
  print("Weak password")

  #create a game where the computer generates a random number between 1 and 100 and the player has to guess the number.Provide hints like "too high" or "too low" after each guess.
import random
target=random.randint(1,100)
while True:
  guess=int(input("Guess the number:"))
  if guess<target:
    print("Too low")
  elif guess>target:
    print("Too high")
  else:
    print("Congrats")
    break

    #Iterating through dictionaries:
colors={"color1":"Black","color2":"Red","color3":"Blue","color4":"Green"}
for i in colors:
  print(i,colors[i])

  #functions
#def function_name(parameters): 
  # Code to be executed
  #....
def greet(name):
  print(f"Hello, {name}!")
greet("Akash")  

#default parameters
def power(base,expo=3):
  return base**expo
print(power(3,6))
print(power(3))

#args(to pass different variables into the function)
def average(*args):
  return sum(args) / len(args)
print(average(5,10,15))  

#kwargs(key arguments)
def person_info(name,age):
  print(f"Name: {name},Age: {age}")
person_info(age=25,name="Bob")  
#class Definitiom
class Student:
   #Special method called constuctors
  def __init__(self):
    self.name="Ram"
    self.age=21
    self.marks=75.90
  #This is an instance method
  def putdata(self):
    print("Name:",self.name)
    print("Age:",self.age)
    print("Marks:",self.marks)
#create an instance to the student class
s=Student()
#call the method using an object
s.putdata()

class BankAccount:
  def __init__(self,name,balance):
    self.name=name
    self.balance=balance
  def deposit(self,amount):
    if amount > 0:
      self.balance+=amount
      print(f"Deposited ${amount}. Newbalance: ${self.balance}")
    else:
      print("Invalid amount. Please deposit a positive amount.")
  def withdraw(self,amount):
        if amount<=0:
           print("Invalid amount. Please withdraw a positive amount.")
        elif amount>self.balance:
           print("Insufficient balance.")
        else:
          self.balance-=amount
          print(f"Withdrew ${amount}. New balance: ${self.balance}")
account1=BankAccount("Alice", 1000)
account1.deposit(500)
        
        


