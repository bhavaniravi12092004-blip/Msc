1(a). PROGRAM USING LIST

Aim:
        To write a python program using list
Procedure : 
Program:

print("List Method")
first=[1,2,3]
second=["one","two","three"]
print(first)
print(second)
print("Append:",first.append(4))
print(first)
print("Extend:",first.extend(second))
print(first)
print("Insert:",first.insert(0,0))
print(first)
print("Pop:",second.pop())
print(second)
print("Searching a list")
a=[10,20,30]
target=25
if target in a:
    print(a.index(target))
 
else:
    print("The value is not present")
print("Sort a list")
c=[20,10,30]
print(c)
c.sort()
print()


















Output:

List Method
[1, 2, 3]
['one', 'two', 'three']
Append: None
[1, 2, 3, 4]
Extend: None
[1, 2, 3, 4, 'one', 'two', 'three']
Insert: None
[0, 1, 2, 3, 4, 'one', 'two', 'three']
Pop: three
['one', 'two']
Searching a list
The value is not present
Sort a list
[20, 10, 30]




Result:
          The above program using list was executed and run successfully.

1(b). PROGRAM USING TUPLE

Aim:
        To write a python program using tuple
Procedure : 
Program:

print("Tuple Method")
first=[1,2,3,4]
second=("one","two","three")
print(first)
print(second)
print("Searching a tuple:")
a=(10,20,30)
target=20
if target in a:
	print(a.index(target))
else:
    print("The value is not present")
print(“Counting the duplicate elements in the Tuple:”)
c=(20,10,10,30)
print(c)
print(c.count(30))
print("Length of the first tuple:",len(first))
print("Length of the second tuple:",len(second))



 
Output:

Tuple Method
(1, 2, 3, 4)
('one', 'two', 'three')
Searching a tuple:
The value is not present
Sort the Tuple:
(20, 10, 30)

Length of the first tuple: 4
Length of the second tuple: 3









Result:
          The above program using tuple was executed and run successfully.


1(c). PROGRAM USING DICTIONARY

Aim:
        To write a python program using dictionary
Procedure :



















Program:


print("Dictionary")
book={"name":"python","cost":300,"edition":"first"}
print(book)
print("Length of dictionary:",len(book))
dict1={1:"python",2:"java",3:"c programming",4:"RDBMS"}
print("Copy method:")
dict2=dict1.copy()
(dict2)
print("Clear method:")
dict1.clear()
print("Get method:")
print(dict2.get(2))
print("Pop method:")
dict2.pop(4)
print(dict2)
print("Update method:")
dict2.update({3:"RDBMS"})
print(dict2)
 
print("Print the keys:")
print(list(dict2.keys()))
print("Print the values:")
print(list(dict2.values()))
print("Print the items:")
print(list(dict2.items()))



















Output:
Dictionary
{'name': 'python', 'cost': 300, 'edition': 'first'}
Length of dictionary: 3
Copy method:
Clear method:
Get method:
java
Pop method:
{1: 'python', 2: 'java', 3: 'c programming'}
Update method:
{1: 'python', 2: 'java', 3: 'RDBMS'}
Print the keys:
[1, 2, 3]
Print the values:
['python', 'java', 'RDBMS']
Print the items:
[(1, 'python'), (2, 'java'), (3, 'RDBMS')]


Result:
          The above program using dictionary was executed and run successfully.


2. CONDITIONAL BRANCHES

Aim:
        To write a program using conditional branch in python
Procedure : 
Program:
regno=int(input("Enter your register number :"))
name=(input("Enter your name :"))
tamil=int(input("Enter the Tamil mark :"))
english=int(input("Enter  the English mark :"))
maths=int(input("Enter the Maths mark :"))
science=int(input("Enter the science mark :"))
socialscience=int(input("Enter the Social Science mark :"))
print(".................................................................")
print("Your name : ",name)
print("Your register number : ",regno)
total=tamil+english+maths+science+socialscience
print("Total = ",total)
avg=total/5
print("Average : ",avg)
if avg>80:
    grade="A"
    print("Result = Pass")
elif avg>60:
    grade="B"
    print("Grade : ",grade)
    print("Result = Pass")
elif avg>40:
    grade="C"
   
 print("Grade : ",grade)
    print("Result = Pass")
elif avg>30:
    grade="D"
    print("Grade : ",grade)
    print("Result = Pass")
else:
    print("No grade")
    print("Result = Fail")
    print(".................................................................")















Output:

Enter your register number : 12026016
Enter your name : Guru
Enter the Tamil mark : 99
Enter the English mark : 87
Enter the Maths mark : 89
Enter the Science mark : 90
Enter the Social Science mark : 91
......................................................................
Your name: Guru
Your register number: 12026016
Total = 456
Average = 91.2
Grade: A
Result = pass
......................................................................

Result:
          The above program using conditional branches was executed and run successfully.




3. PROGRAM USING LOOPS

Aim:
       To write a program using loops in python
Procedure :
 
Program:

print("1. Factorial")
print("2. Fibonacci series")
print("3. Perfect number")
ch=int(input("Enter your choice:"))
if ch==1:
    print("Factorial")
    n=int(input("Enter the number:"))
    f=1
    i=1
    while(n>=i):
        f=f*i
        i=i+1
    print("The Factorial of",n,"is",f)
elif ch==2:
    print("Fibonacci series")
    n=int(input("Enter the number:"))
    n1=0
    n2=1
    print(n1)
    print(n2)



    for i in range(2,n):
        n3=n1+n2
        n1=n2
        n2=n3
        print(n3)
else:
    ch==3
    print("Perfect number")
    n=int(input("Enter the number:"))
    sum=0
    for i in range(1,n):
        if(n%i==0):
            sum=sum+i
    if(sum==n):
        print(n," is a Perfect number")
    else:
        print(n," is not a Perfect number")









Output:

1. Factorial
2. Fibonacci series
3. Perfect number

Enter your choice: 2
Fibonacci series

Enter the number: 2
0
1






Result:
          The above program using loops was executed and run successfully.

         
4. PROGRAM USING FUNCTION

Aim:
        To write python program using string function
Procedure :
 
Program:

print("Function without arguments")
print('----------------------------------')
def function1():
    print('Printing letters one by one')
    for i in 'Programming':
         print(i)                    
print('Function with argument')
def function2(a):
    print('Finding the square and cube of a')
    print('Finding the square of a')
    sq=a**2
    print('Square of',a,'is:',sq)   
    print('Finding the cube of a')
    cb=a**3
    print('Cube of',a,'is:',cb)           
function1()  
function2(3)




 
Output:
Function without arguments
------------------------------------------
Function with argument
Printing letters one by one
P
r
o
g
r
a
m
m
i
n
g
Finding the square and cube of a
Finding the square of a
Square of 3 is: 9
Finding the cube of a
Cube of 3 is: 27

Result:
          The above program using function was executed and run successfully.

5. PROGRAM USING EXCEPTION                         HANDLING

Aim:
      To write a python program using exception handling
Procedure :
 
Program:


#zero division exception
def fun(x,y):
    try:
        z=((x+y)/(x-y))
    except ZeroDivisionError:
        print("a/b divide by zero")
    else:
        print(z)
a=int(input(‘Enter the a value:’))
b=int(input(‘Enter the b value:’))
fun(a,b)
#element out of bound exception
str=["python", "exception","try and except"]
try:
    for i in range(4):
        print("The index and element from list:",i,str[i])
except:
    print("Index out of bound range")





 
Output:

Enter the a value : 5
Enter the b value : 2
2.3333333333333335
The index and element from list: 0 python
The index and element from list: 1 exception
The index and element from list: 2 try and except
Index out of bound range












Result:
          The above program using exception handling was executed and run successfully.

6. PROGRAM USING INHERITANCE

Aim:
        To write python program using inheritance
Procedure :
 
Program:


class person:
    def __init__(self,name,idno):
        self.name=name;
        self.idno=idno;
    def display(self):
        print("................................")
        print("Name:",self.name,"\n Id no:",self.idno)
class emp(person):
    def __init__(self,name,idno,salary,job):
        self.name=name
        self.idno=idno
        self.salary=salary
        self.job=job
    def printed(self):
        print("Salary : ",self.salary,"\n  Job :",self.job)
        print("................................")
n=input("Enter the name:")
i=int(input("Enter the idno:"))
s=int(input("Enter the salary:"))
j=input("Enter your job:")
lic=(s*5/100)
pf=(s*10/100)
m=(s*1/100)
hr=(s*2/100)
daily=(s*2/100)
print("Your LIC is : ",lic)
print("Your PF is : ",pf)
print("Your medical allowance is : ",m)
print("Your HR is : ",hr)
print("Your Daily allowance is : ",daily)
s=s-(lic+pf)+(hr+m+daily)
emp1=emp(n,i,s,j)
emp1.display()
emp1.printed()





 
Output:

Enter the name : Guru
Enter the Id no : 12026016
Enter the salary:35000
Enter your job : IT
Your LIC is : 1750.0
Your PF is: 3500.0
Your medical allowance is: 350.0
Your HR is: 700.0
Your Daily allowance is: 700.0
................................
Name : Guru 
Id no: 12026016
Salary: 31500.0 
Job: IT
................................        


Result:
          The above program using inheritance was executed and run successfully.


7. PROGRAMS USING POLYMORPHISM

Aim:
         To write a python program using polymorphism
Procedure :
 
Program:


class vehicle:
    def __init__(self,brand,model,price):
        self.brand=brand
        self.model=model
        self.price=price
    def show(self):
        print('details:',self.brand,self.model,'price:',self.price)
    def max_speed(self):
        print('vehicle max speed is 160')
    def gear_system(self):
        print('vehicle has 6 shifter gearbox')
class car(vehicle):
    def max_speed(self):
        print('car max speed is 260')
    def gear_system(self):
        print('car has automatic transmission')
car=car('audi','r8',9000000)
car.show()
car.max_speed()
car.gear_system
 
print()
vehicle=vehicle('nissan','magnite',550000)
vehicle.show()
vehicle.max_speed()
vehicle.gear_system()

















 
Output:

details: audi r8 price: 9000000
car max speed is 260
details: nissan magnite price: 550000
vehicle max speed is 160
vehicle has 6 shifter gearbox














Result:
          The above program using polymorphism was executed and run successfully.
                   
8. PROGRAM USING FILE OPERATIONS

Aim:
        To write a python program to implement a file operations.
Procedure : 
Program:


# File name to use
file_name = "sample_file.txt"

# 1. Create and write to a file
def create_and_write_file():
    with open(file_name, "w") as file:
        file.write("Hello, this is a file operation example.\n")
        file.write("We are writing some sample text.\n")
    print("✅ File created and written successfully.")

# 2. Read from a file
def read_file():
    if os.path.exists(file_name):
        with open(file_name, "r") as file:
            print("📖 File contents:")
            print(file.read())
    else:
        print("⚠️ File does not exist.")



# 3. Append to a file
def append_to_file():
    if os.path.exists(file_name):
        with open(file_name, "a") as file:
            file.write("This line is appended to the file.\n")
        print("✅ Text appended to the file.")
    else:
        print("⚠️ File does not exist.")

# 4. Delete a file
def delete_file():
    if os.path.exists(file_name):
        os.remove(file_name)
        print("🗑️ File deleted successfully.")
    else:
        print("⚠️ File does not exist.")

# Menu to demonstrate operations
def main():
    while True:
        print("\nFile Operations Menu:")
        print("1. Create and write to file")
        print("2. Read file")
        print("3. Append to file")
        print("4. Delete file")
        print("5. Exit")
        choice = input("Enter your choice (1-5): ")

        if choice == '1':
            create_and_write_file()
        elif choice == '2':
            read_file()
        elif choice == '3':
            append_to_file()
        elif choice == '4':
            delete_file()
        elif choice == '5':
            print("👋 Exiting program.")
            break
        else:
            print("❌ Invalid choice. Please try again.")

# Run the program
if __name__ == "__main__":
    main()




OUTPUT :

File Operations Menu:
1. Create and write to file
2. Read file
3. Append to file
4. Delete file
5. Exit

Enter your choice (1-5): 1
✅ File created and written successfully.

File Operations Menu:
1. Create and write to file
2. Read file
3. Append to file
4. Delete file
5. Exit

Enter your choice (1-5): 2
📖 File contents:
Hello, this is a file operation example.
We are writing some sample text.


File Operations Menu:
1. Create and write to file
2. Read file
3. Append to file
4. Delete file
5. Exit

Enter your choice (1-5): 3
✅ Text appended to the file.

File Operations Menu:
1. Create and write to file
2. Read file
3. Append to file
4. Delete file
5. Exit

Enter your choice (1-5): 4
🗑️ File deleted successfully.

File Operations Menu:
1. Create and write to file
2. Read file
3. Append to file
4. Delete file
5. Exit

Enter your choice (1-5): 5
👋 Exiting program. 














Result:
          The above program to implement file operations was executed and run successfully.
 

9. PROGRAM USING MODULE

Aim:
        To write a python program using module
Procedure :
 
Program:


def addition(n1,n2):
    return n1+n2
def subtraction(n1,n2):
    return n1-n2
def multiplication(n1,n2):
    return n1*n2
def division(n1,n2):
    return n1/n2
def floordivision(n1,n2):
    return n1//n2
def modules(n1,n2):
    return n1%n2
def exponent(n1,n2):
    return n1**n2
n1=int(input("Enter the first value"))
n2=int(input("Enter the second value"))
print("The addition of n1 and n2=",addition(n1,n2))
print("The subtraction of n1 and n2=",subtraction(n1,n2))
print("The multiplication of n1 and n2=",multiplication(n1,n2))
 
print("The division of n1 and n2=",division(n1,n2))
print("The floor division of n1 and n2=",floordivision(n1,n2))
print("The modules of n1 and n2=",modules(n1,n2))
print("The exponent of n1 and n2=",exponent(n1,n2))





















Output:

Enter the first value 5
Enter the second value 6
The addition of n1 and n2= 11
The subtraction of n1 and n2= -1
The multiplication of n1 and n2= 30
The division of n1 and n2= 0.8333333333333334
The floor division of n1 and n2= 0
The modules of n1 and n2= 5
The exponent of n1 and n2= 15625








Result:
          The above program using module was executed and run successfully.


10. PROGRAMS FOR CREATING DYNAMIC AND INTERACTIVE WEB PAGES USING FORMS.

Aim:
        To write python program create Dynamic and Interactive Web pages using Djanco Tools.
Procedure : 
Programs:

from django import forms

# creating a form 
class InputForm(forms.Form):

	first_name = forms.CharField(max_length = 200)
	last_name = forms.CharField(max_length = 200)
	roll_number = forms.IntegerField(
					help_text = "Enter 6 digit roll number"
					)
	password = forms.CharField(widget = forms.PasswordInput())


from django.shortcuts import render
from .forms import InputForm

# Create your views here.
def home_view(request):
	context ={}
	context['form']= InputForm()
	return render(request, "home.html", context)
<form action = "" method = "post">
	{% csrf_token %}
	{{form.as_p }}
	<input type="submit" value=Submit">
</form>












 
Output:



















Result:
          The above programs for creating dynamic and interactive web pages using forms was executed and run successfully.
 

11. PROGRAMS USING CLASSES AND OBJECTS

Aim:
        To write python program using classes and object
Procedure :
 
Program:

class bank_account:
    def __init__(self):
        self.balance=0
        print("hello!!!welcome to the deposit & withdrawal machine")
        self.name=input("Enter your name:")
        self.acc_no=int(input("Enter your account number:"))
    def deposit(self):
        amount=float(input("Enter amount to be deposited:"))
        self.balance+=amount
        print("\n Amount deposited:",amount)
    def withdraw(self):
        amount=float(input("Enter amount to be withdrawn:"))
        if self.balance>=amount: 
            self.balance-=amount
            print("\n Your withdraw:",amount)
        else:
            print("\n Insufficient balance")
   
 
 def display(self):
        print("\n Not avilable balance=",self.balance)
s=bank_account()
s.deposit()
s.withdraw()
s.display()
















 
Output:

Enter your name : Guru
Enter your account number :74651982375
Enter amount to be deposited :2000
Amount deposited : 2000.0
Enter amount to be withdrawn : 1500
Your withdraw : 1500.0
Not available balance = 500.0









Result:
          The above program using classes and objects was executed and run successfully.

