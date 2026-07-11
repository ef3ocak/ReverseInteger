# Reverse Integer

A Python solution for the **Reverse Integer** problem.

## Description

This solution converts the integer to a string, reverses its digits, and preserves the sign for negative numbers. After reversing, it checks whether the result is within the 32-bit signed integer range. If the value is out of range, it returns `0`.

## How It Works

- Convert the integer to a string.
- Check if the number is negative.
- Reverse the digits.
- Restore the negative sign if needed.
- Convert the result back to an integer.
- Return `0` if the reversed value is outside the 32-bit signed integer range.

## Code

```python
class Solution:
    def reverse(self, x: int) -> int:

        x = str(x)
        
        if "-" in x:

            x = x.replace("-", "")
            x = x[::-1]
            x = "-" + x

        else:
            x = x[::-1]
        
        x = int(x)

        if x > 2147483647 or x < -2147483647:
            return 0

        return x
```
