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

