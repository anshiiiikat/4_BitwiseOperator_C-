
# Aim
To:Understand how bitwise operators work in C++

Learn how to set (turn ON) and reset (turn OFF) specific bits in a number

# Objectives
 Use basic bitwise operators like &, |, ^, ~, <<, >>

 Learn how to change just one bit in a number

 Understand how shifting bits left or right changes the whole value

# Theory:
What Are Bitwise Operators?
Every number is made of bits (0s and 1s).

Useful when we want to control specific bits — like in LEDs, sensors, switches, flags, etc.
|Operator|Symbol| Description|
|--------|------|------------|
| AND    | &     |  Sets bit to 1 only if both bits are 1|
| OR     |  \|    | Sets bit to 1 if at least one bit is 1|
| XOR    |  ^    |Sets bit to 1 if only one of the bits is 1|
| NOT    |  ~    |Inverts all bits (0 becomes 1, 1 becomes 0)|
|Left Shift| <<  |Shifts bits to the left, multiplying by 2|
|Right Shift| >> |Shifts bits to the right, dividing by 2|

# Set and Reset a Bit
Sometimes, we don’t want to change the whole number — just one single bit. It is very useful in electronics, where you control just one light or switch.

#### To Set a Bit (Make a bit = 1)
```num | (1 << 3)```

This keeps all other bits the same, and turns bit at position 3 to 1

#### To Reset a Bit (Make a bit = 0)
```num & (~(1 << 4))```

This makes the bit at position 4 = 0, and keeps the rest unchanged.

# Program Description
Bitwise Operations
Take two numbers (say a = 5 and b = 3)

Apply each bitwise operator and show the result

a & b → AND

a | b → OR

a ^ b → XOR

~a → NOT

a << 1 → Left shift by 1

a >> 1 → Right shift by 1

#### Set & Reset Specific Bits
Let’s say we want to set bit 2 of number a → use a | (1 << 2)

To resetF bit 1 of number a → use a & (~(1 << 1))

We can see that before and after values has changed just one bit.

#### Concepts Used
Bitwise Operators: &, |, ^, ~, <<, >>

Set a bit: num | (1 << position)

Reset a bit: num & (~(1 << position))
# Sample output
### Bitwise Operator and set and reset 

```AND: 0
OR: 14
XOR: 14
NOT: -13
LEFT_SHIFT: 48
RIGHT_SHIFT: 14

Enter bit to set: 3
Enter bit to reset: 4
SET OUTPUT: 88
RESET OUTPUT: 64
