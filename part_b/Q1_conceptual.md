# Break vs Continue and Loop Else Clause

## Difference between break and continue

break:
Stops the loop completely and exits it.

Example:
```python
for i in range(5):
    if i == 3:
        break
    print(i)
```

Output:
0
1
2

continue:
Skips the current iteration and moves to the next iteration.

Example:
```python
for i in range(5):
    if i == 3:
        continue
    print(i)
```

Output:
0
1
2
4

## else clause in loops

The else clause in a loop executes when the loop finishes normally without hitting a break.

Example:
```python
for i in range(3):
    print(i)
else:
    print("Loop completed")
```

## Practical Use Case (Search Pattern)

```python
numbers = [2,4,6,8]

for n in numbers:
    if n == 5:
        print("Found")
        break
else:
    print("Not Found")
```