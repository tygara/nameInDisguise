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

