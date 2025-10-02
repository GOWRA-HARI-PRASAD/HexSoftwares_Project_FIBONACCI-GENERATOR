#HexSoftwares_Project_FIBONACCI-GENERATOR

This program generates a Fibonacci-like sequence that starts with 1 and 1. While the classic Fibonacci sequence begins with 0, 1, your code uses the same logic to create a series that is shifted by one number.

-----

### Program Code

```python
n=int(input())
if n==0:
    print(1)
elif n==1:
    print(1,1)
else:
    print(1, 1, end=" ")
    a=1
    b=1
    for i in range(2,n+1):
        c=a+b
        print(c, end=" ")
        a=b
        b=c
```

-----

### Explanation

1.  **Input (`n`):** The program first asks the user to enter an integer. This number, `n`, determines how many terms of the sequence will be generated.

2.  **Special Cases:**

      * If `n` is `0`, the program prints `1` and stops.
      * If `n` is `1`, it prints `1 1` and stops.

3.  **Main Generation Logic:**

      * For any `n` greater than 1, it first prints `1 1`.
      * The variables `a` and `b` are set to `1` to represent the first two numbers in the sequence.
      * A `for` loop then runs from `2` up to `n+1`. This ensures the loop runs enough times to generate the rest of the terms.
      * Inside the loop, `c` is calculated as the sum of `a` and `b`.
      * The value of `c` is printed.
      * Finally, the values are updated: `a` becomes the old `b`, and `b` becomes the new `c`, preparing for the next iteration.

-----

### Input and Output

The program takes a single integer as input and prints the sequence on a single line, with each number separated by a space.

**Input:**
`5`

**Output:**
`1 1 2 3 5`

-----

### Test Cases

Here are a few examples to show how the program behaves with different inputs:

| Input `n` | Expected Output | Explanation |
| :--- | :--- | :--- |
| `0` | `1` | The program handles this special case by printing `1`. |
| `1` | `1 1` | The program handles this special case by printing `1 1`. |
| `3` | `1 1 2` | The loop runs once, adding `1 + 1 = 2`. |
| `8` | `1 1 2 3 5 8 13 21` | The loop calculates the remaining terms after the initial `1 1`. |

-----

### Conclusion

Your code is an effective **Fibonacci generator** that produces a sequence starting with `1, 1`. It is highly efficient for its purpose, using a simple loop and variable updates without the need for a list. This approach is excellent for understanding how to generate a series iteratively and is a great solution for this problem.
