# **Python learning notes**

* [-] Variables and data types
* [-] Introducing lists
* [-] working with lists 
* [-] if statements 
* [-] dictionaries 
* [-] user inputs and while loops 
* [-] functions 
* [-] classes 
* [-] files and exceptions 
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

    











































