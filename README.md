# Disguise Name & Birth Year Homework
## Conversion Process
1. Convert chars of first&last name(lowercase) to ASCII decimal value.
2. Convert each character's decimal value to hex using "Successive Division by 16"
3. Divide the ASCII value by 16 using integer division (ignore decimal)
4. Quotient becomes the hexdecimals higher nibble(left most bit/MSB)
5. Multiply the quotient by 16
6. Subtract the result from the original ASCII decimal value to get the remainder 
7. Remainder is the lower nibble (LSB/rightmost bit)
8. Combine the higher and lower nibbles to get the final hex value for the current char

EXAMPLE:<br>
e -> 101(ASCII) -> 101/16= 6(integer divison)-> 6*16 = 96 -> 101-96=5 -> hex = 65(e)

## Conversion process for birth year to binary
### Use integer division to perform successive division by 2
1. Divide the number by 2 using integer division (ignore decimals)
2. Record the remainder (1 if odd, 0 if even) -> any remainder that != 0 is counted as 1
3. Repeat with the quotient until it reaches 0
4. The binary is formed by reading the remainders from bottom to top

EXAMPLE: <br>
50/2 -> 25 R0 <br>
25/2 -> 12 R1 <br>
12/2 -> 6  R0 <br>
6/2 ->  3  R0 <br>
3/2 ->  1  R1 <br>
1/2 ->  0  R1 <br>
Result: 110010


## Challenges
This exercise was mostly straightforward, especially the hex conversion steps, since they 
followed a predictable pattern. However, one challenge I faced was keeping track of the 
nibble positions (higher vs. lower) and making sure I applied integer division correctly. 
Another challenge was maintaining accuracy when moving between ASCII, decimal, and hex 
without mixing up values. During the process, I also learned how to use successive division
by 16 to convert decimal values to hexadecimal, which gave me a much clearer understanding 
of how characters are represented in hex. Writing out each step helped reduce errors and 
reinforced my grasp of the underlying conversion logic.

## [Flowchart](images/nameInDisguised.png)
## [Hand-Written Work](images/conversions.jpg)

