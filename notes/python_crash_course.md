# **Python learning notes**

> [!DONE] Variables and data types

> [!DONE] Introducing lists

> [!TODO] working with lists 

> [!TODO] if statements 

> [!TODO]dictionaries 

> [!TODO]user inputs and while loops 

> [!TODO]functions 

> [!TODO]classes 

> [!TODO]files and exceptions 

1. **f-strings**
    * format string => replaces the variables and format the string
        
        ```python
        first_name = "vijay"
        last_name = "jangid"
        full_name = f"{first_name} {last_name}"
        ```

    * simialar to string-interpolation in c# ($)

2. **strip white space**
    * strips the white space at the of string

        ```python
        name = "vijay "
        name.rstrip()
        ```

    * strip is the main function
        1. l => left strip
        2. r => right strip

    [Assignment](https://github.com/vjjangid/LearningPython/tree/main/PythonCrashCourse/02.Excercise) 

3. **Exponent**
    * Uses ** for exponent

        ```python
        square = 3 ** 2
        ```

4. **Datatypes**
    * Number (1,2,3) => Any number is number
    * Float (1.1, 5.3) => Any decimal number is called float
    * Integer + float in any operation => float
    * How to make number readables?
        - you can use underscore
        - universe_age = 1_00_000
        - print(universe_age)
    ```python
    x, y, z = 0, 0, 0 #Multiple assignment
    ``` 

    ```python
    MAX_CONNECTIONS = 500 #No specific keyword for const just naming convention is there
    ```

----------

## **List**
* Collection of elements

```python
names = ["ram", "mohan", "mahesh"]
print(names) #print whole list
print(names[0]) #Accessing element
```

* index starts at 0
* How to modify/add/remove?
    ```python
    names[1] = "ram"
    names.append('ducati') #at the end of list
    names.insert(0, "mahesh") #insert at index => remeber it shifts the elements to its right
    del name[0] # delete the elements in the list
    item = names.pop() # removes last occurence you can pass index too
    item = names.remove("value") #Removes first occurrence
    ```  
* sorting list
    ```python
    list.sort() #permanent sort of list
    sorted(list) # temporary sore of list
    list.reverse() # reverse the list
    list.len() # get the length of list
    ```

> [!NOTE]
> you can use the negative index -1 to get last element

* Looping through lists
    ```python
    countries = ["india", "japan", "us"]
    for country in countries:
        print(country)
    ```

> [!IMPORTANT]
> identations are very strict in python. they basically defines **bolck**

> [!IMPORTANT]
>[! Question] What if you forgot the colon after the loop (:)??
>Remeber it signifies the start of loop so you will get the error

* few more thing good to know
    1. range(1,5) => 1-4
    2. range(5) => 0-4
    3. min(list) => Minimum in list
    4. max(list) => Maximum in list
    5. sum(list) => Sum of elements in list

* List comprehension

if you see in below example here expression can be anything like what you perform on each number
iterable can be any list on each member it will perform the operation
and at the end create the list
```python
# list = [expresion for member in iterable]
squares = [ value * value for value in range(5)]

```

 > [!NOTE]
 > map returns map object
 > comprehension returns list
 
----------
## Functions

```python
def function_name(parameter):
    print(parameter)

function_name(parameter)
```

* There are two types of arguments 
    1. Positional
    2. keywords

```python
def get_fullname(first_name, last_name):
    return f"{first_name} {last+name}"

get_fullname("vijay", "jangid") #positional argument
get_fullname(first_name = "vijay", last_name="jangid") #keywords argument
get_fullname(last_name = "jangid", first_name="vijay") #keywords argumnet

```

* You can have default values took
```python
def get_fullname(first_name, last_name = "jangid"):
    return f"{first_name} {last+name}"

get_fullname("vijay") 
```
> [!IMPORTANT]
> Just like c# all default values arguments lies at the end of normal arguments

* By default passing of list is call by ref
* use slice operator to pass copy

* you can pass arbitrary amount of parameters using *args. I will just create a tuple of it.
```python
def user_details(name, *args):
    #do something

```
* you can pas dictionary to as arbitrary argument like this **keyargs. It converts the arguments in dictionary

* imports in python
    1. You can make module of by keeping functions in file like utils.py
    2. Then you have thre ways to import.
        * import utils.py => import every function
        * from utils.py => import only one function
        * from utils.py import sum as s => rename import name/alias
        * from utils.py import * => import everything

----------

