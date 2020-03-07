# Writing Files in Python

If you have been following along, you can probably guess what the file-mode flag is for writing files: “w” and “wb” for write-mode and write-binary-mode. Let’s take a look at a simple example, shall we?

*CAUTION*: When using “w” or “wb” modes, if the file already exists, it will be overwritten with no warning! You can check if a file exists before you open it by using Python’s os module.

```python
handle = open("test.txt", "w")
handle.write("This is a test!")
handle.close()

# Now let's read the file that we just wrote
handle = open("test.txt", "r")
for line in handle:
    print(line)
handle.close()
```

**output**
```
This is a test!
```
