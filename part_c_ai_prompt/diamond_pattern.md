# Diamond Pattern using Nested Loops

## Exact Prompt Used

"Write a Python program that prints a diamond pattern of asterisks. The user inputs the number of rows for the upper half. Include proper spacing and use nested loops only (no string multiplication tricks)."

---

# AI Generated Code

```python
n = int(input("Enter number of rows: "))

for i in range(1, n+1):
    for j in range(n-i):
        print(" ", end="")
    for j in range(2*i-1):
        print("*", end="")
    print()

for i in range(n-1, 0, -1):
    for j in range(n-i):
        print(" ", end="")
    for j in range(2*i-1):
        print("*", end="")
    print()
```

---

# Critical Evaluation

## Spacing Correctness
The spacing logic correctly produces a symmetric diamond.

## Readability
Readable but could be improved with functions and clearer variable names.

## Edge Cases
- n = 0 → program prints nothing; better to show an error message.
- n = 1 → prints a single star, which is acceptable.

## Nested Loops vs String Tricks
Uses nested loops only, satisfying the requirement.

## Time Complexity
Pattern printing takes roughly O(n²) operations.

---

# Improved Version

```python
def print_diamond(n):

    if n <= 0:
        print("Invalid input")
        return

    for i in range(1, n + 1):

        for space in range(n - i):
            print(" ", end="")

        for star in range(2 * i - 1):
            print("*", end="")

        print()

    for i in range(n - 1, 0, -1):

        for space in range(n - i):
            print(" ", end="")

        for star in range(2 * i - 1):
            print("*", end="")

        print()


rows = int(input("Enter number of rows: "))
print_diamond(rows)
```