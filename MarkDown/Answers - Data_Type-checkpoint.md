
# Answers - Data_Type
-----

**Q** : What will be the output of the following code snippets?


```python
a=[1,2,3,4,5,6,7,8,9]
print(a[::2])
```

    [1, 3, 5, 7, 9]
    


```python
a=[1,2,3,4,5,6,7,8,9]
a[::2]=10,20,30,40,50,60 # a[0], a[2],... = 10,20,30
print(a)
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-9-01f0e79fed52> in <module>()
          1 a=[1,2,3,4,5,6,7,8,9]
    ----> 2 a[::2]=10,20,30,40,50,60
          3 print(a)
    

    ValueError: attempt to assign sequence of size 6 to extended slice of size 5



```python
a=[1,2,3,4,5,6,7,8,9]
a[::2]=10,20,30,40,50
print(a)
```

    [10, 2, 20, 4, 30, 6, 40, 8, 50]
    


```python

```


```python
a=[1,2,3,4,5]
a[3:1:-1]
```




    [4, 3]




```python
a=[1,2,3,4,5]
print(a[3:0:-1])
```

    [4, 3, 2]
    


```python
arr = [[1, 2, 3, 4],
       [4, 5, 6, 7],
       [8, 9, 10, 11],
       [12, 13, 14, 15]]
for i in range(0, 4):
    print(arr[i].pop())
```

    4
    7
    11
    15
    


```python
arr = [1, 2, 3, 4, 5, 6]
for i in range(1, 6):
    arr[i - 1] = arr[i]
for i in range(0, 6): 
    print(arr[i], end = " ")
```

    2 3 4 5 6 6 


```python
nums = set([1,1,2,3,3,3,4])
print(len(nums))
```

    4
    


```python
numbers = [1, 2, 3, 4]
numbers.append([5,6,7,8])
print (len(numbers))
```

    5
    


```python
numbers = [1, 2, 3, 4]
for a in [5,6,7,8]:
    numbers.append(a)
print (len(numbers))
```

    8
    


```python
numbers = [1, 2, 3, 4]
for a in range(5,9):
    numbers.append(a)
print (len(numbers))
```

    8
    


```python
names1 = ['Amir', 'Barry', 'Chales', 'Dao']
names2 = names1
names3 = names1[:]

names2[0] = 'Alice'
names3[1] = 'Bob'

sum = 0
for ls in (names1, names2, names3):
    if ls[0] == 'Alice':
        sum += 1
    if ls[1] == 'Bob':
        sum += 10

print(sum)
```

    12
    


```python
names1 = ['Amir', 'Barry', 'Chales', 'Dao']
loc = names1.index("Edward")
print (loc)
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    <ipython-input-31-42e02283ae8d> in <module>()
          1 names1 = ['Amir', 'Barry', 'Chales', 'Dao']
    ----> 2 loc = names1.index("Edward")
          3 print (loc)
    

    ValueError: 'Edward' is not in list



```python
list1 = [1, 2, 3, 4]
list2 = [5, 6, 7, 8]

print (len(list1 + list2))
```

    8
    


```python

list1 = [1, 2, 3, 8, 4]
list2 = [5, 6, 7, 8, 2]

print(len(set(list1 + list2)))
```

    8
    

**Q: Write a Python script to add key to a dictionary.**

e.g. Sample Dictionary : {0: 10, 1: 20} Expected Result : {0: 10, 1: 20, 2: 30}


```python
a = {0: 10, 1: 20}
a[2] = 30
print(a)
```

    {0: 10, 1: 20, 2: 30}
    

**Q: Write a Python script to concatenate following dictionaries to create a new one.**

e.g:

**Sample Dictionary** : dic1={1:10, 2:20} dic2={3:30, 4:40} dic3={5:50,6:60}

**Expected Result** : {1: 10, 2: 20, 3: 30, 4: 40, 5: 50, 6: 60}



```python
names1={1:10, 2:20} 
names2={3:30, 4:40}
names3={5:50,6:60}
# names1.update(names2)
new_dict = {}
for ls in (names1, names2, names3):
    new_dict.update(ls)
print(new_dict)
```

    {1: 10, 2: 20, 3: 30, 4: 40, 5: 50, 6: 60}
    


```python
d1={1:2,3:4}
d2={5:6,7:9}
d3={10:8,13:22}
d4 = dict(d1)
d4.update(d2)
d4.update(d3)
print(d4)
```

    {1: 2, 3: 4, 5: 6, 7: 9, 10: 8, 13: 22}
    

**Q: Write a Python script to check if a given key already exists in a dictionary.**


```python
dict = {1: 2, 3: 4, 5: 6, 7: 9, 10: 8, 13: 22}

found = True
for key in dict:
    if(key == 11):
        print("key found")
        break;
else:
    print("key not found")
    found = False
```

    key not found
    

**Q: Write a Python program to iterate over dictionaries using for loops.**
ans: please look above examples

**Q: Write a Python script to generate and print a dictionary that contains number (between 1 and n) in the form (x, x*x).**

Sample Dictionary ( n = 5) : Expected Output : {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}

and 

    Write a Python script to print a dictionary where the keys are numbers between 1 and 15 (both included) and the values are square of keys. Sample Dictionary {1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64, 9: 81, 10: 100, 11: 121, 12: 144, 13: 169, 14: 196, 15: 225}


```python
a = { b : b*b for b in range(1,10) } 
print(a)
```

    {1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64, 9: 81}
    

**Q: Write a Python script to sort (ascending and descending) a dictionary by value. **


```python
e = {1:39,8:110, 4:34, 3:87, 7:110, 2:87}
sortE = sorted(e.items(), key=lambda value: value[1])
print(sortE)
```

    [(4, 34), (1, 39), (3, 87), (2, 87), (8, 110), (7, 110)]
    


```python
e = {1:39,8:110, 4:34, 3:87, 7:110, 2:87}
sortE = sorted(e.items(), key=lambda value: value[1], reverse=True)
print(sortE)
```

    [(8, 110), (7, 110), (3, 87), (2, 87), (1, 39), (4, 34)]
    

**Q: Write a Python script to merge two Python dictionaries.**
use `update`

**Q: Write a Python program to sum all the items in a dictionary.**


```python
e = {1:39,8:110, 4:34, 3:87, 7:110, 2:87}
```

    Write a Python program to multiply all the items in a dictionary.
    Write a Python program to remove a key from a dictionary.
    Write a Python program to map two lists into a dictionary.
    Write a Python program to sort a dictionary by key.
    Write a Python program to get the maximum and minimum value in a dictionary.
    Write a Python program to get a dictionary from an object's fields.
    Write a Python program to remove duplicates from Dictionary.
    Write a Python program to check a dictionary is empty or not.
    Write a Python script to sort (ascending and descending) a dictionary by value.
