# Batschko's Python Notes


## Stuff


## Functions

### main
```python
if __name__ == __main__  # idiom; when called as script -> name equals main
    main()               # extra main function -> best practice
```

### slice
```python
slice(start, end, step)
a = ("0", "1", "2", "3", "4", "5")
x = slice(1, 3)
y = slice(0,5,2)
print(a[x])
print(a[y])
```
*Output:*
```
=> 12
   024
```

## Structure?

## Strings
### format string
### f-string
```python
f'a string with a {very_nice_variable} inside'
# multiline
    def __str__(self):
        return (f"remember to put "
                f"space at end of each string "
                f"missing"
                f"SPACE")
# using \ to break the line causes whitespaces
# use brackets to autmaticly join strings on new line
```
*Output:*
```
=> remember to put space at end of each string missingSPACE
```
### slice string

```python
slice(start, end, step)
a = "0123456789"
print(a[0:5]) #0..4
print(a[2:7]) #2..6
print(a[2:])  #2..n
print(a[:2])  #01
print(a[:-2]) #0..n-2
```
*Output:*
```
=> 01234
   23456
   23456789
   01
   1234567
```
## Dictionary
```python
dictionary = {'key1': 5, 'key2': 'yeah'} #create
dictionary['key2'] = 'updated'           #update
dictionary['new_key'] = 'crazy stuff'    #add
TODO functions as list ?
print(dictionary)
```
*Output:*
```
=> {'key1': 5, 'key2': 'yeah', 'new_key' = 'crazy stuff'}
```
merge two dictionaries
```python
# TODO
```

```python
'inline if' if True is True else 'no ternary operator'
```


```python
# Different ways to test multiple
# flags at once in Python
x, y, z = 0, 1, 0

if x == 1 or y == 1 or z == 1:
    print('passed')

if 1 in (x, y, z):
    print('passed')

# These only test for truthiness:
if x or y or z:
    print('passed')

if any((x, y, z)):
    print('passed')
```



```python
class RequestException(Exception):
    """Request returned diffrent status code than 200"""
    def __init__(self, status_code, url, func):
        self.status_code = status_code
        self.url = url
        self.func = func

    def __str__(self):
        return(f'Statuscode {self.status_code} for {self.url} in function {self.func}')
```