# args and kwargs
You can also set up functions to accept any number of arguments or keyword arguments by using a special syntax. To get infinite arguments, use *args and for infinite keyword arguments, use **kwargs. The "args" and “kwargs” words are not important. That’s just convention. You could have called them *bill and **ted and it would work the same way. The key here is in the number of asterisks.

*Note: in addition to the convention of *args and **kwargs, you will also see a andkw from time to time.

Let’s take a look at a quick example
```python
def many(*args, **kwargs):
    print(args)
    print(kwargs)

many(1, 2, 3, name="Mike", job="programmer")

# (1, 2, 3)
# {'job': 'programmer', 'name': 'Mike'}
```
**output**
```
(1, 2, 3)
{'name': 'Mike', 'job': 'programmer'}
```
First we create our function using the new syntax and then we call it with three regular arguments and two keyword arguments. The function itself will print out both types of arguments. As you can see, the **args** parameter turns into a tuple and **kwargs** turns into a dictionary. You will see this type of coding used in the Python source and in many 3rd party Python packages.

