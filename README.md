# copy-file
## AIM:
To write a python program for copying the contents from one file to another file.
## EQUIPEMENT'S REQUIRED: 
PC
Anaconda - Python 3.7
## ALGORITHM: 
### Step 1:
First we want create 2 text files.
### Step 2: 
Then We want to create a python file. 
### Step 3: 
In That python file we want to import the copy file.
### Step 4:  
Then we want to use what we want to display in the command lines.
### Step 5: 
Then we want to add the expansion handling.
### Step 6: 
Then we want to write the revalent code.
## PROGRAM:
### To write a python program for copying the contents from one file to another file.
```python
#Developed by : YUVARAJ.S
#Register Number : 22008589
from shutil import copyfile
from sys import exit

source = input("Enter source file with full path: ")
target = input("Enter target file with full path: ")

# adding exception handling
try:
    copyfile(source, target)
except IOError as e:
    print("Unable to copy file. %s" % e)
    exit(1)
except:
    print("Unexpected error:", sys.exc_info())
    exit(1)

print("\nFile copy done!\n")

while True:
    print("Do you like to print the file ? (y/n): ")
    check = input()
    if check == 'n':
        break
    elif check == 'y':
        file = open(target, "r")
        print("\nHere follows the file content:\n")
        print(file.read())
        file.close()
        print()
        break
    else:
        continue
```
### OUTPUT:
![output](./53%201.jpeg)
![output](./53%202.jpeg)


## RESULT:
Thus the program is written to copy the contents from one file to another file.