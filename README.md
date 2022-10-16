# binary-decimal-converter
#This program allows a user to enter any binary number and it returns its decimal equivalent. In case the user enters a number that is not binary, it prints out an error message. Written in Python code.
def binaryToDecimal(binary):


    decimal, i, n = 0, 0, 0
    while(binary != 0):
        dec = binary % 10
        decimal = decimal + dec * pow(2, i)
        binary = binary//10
        i += 1
    print(f'the decimal equivalent is: {decimal}')

binary_number = (input('Enter binarynumber: '))
final_number = int(binary_number)

#to check if the number entered is a binary number before converting it to decimal
b = {'0', '1'}
t = set(binary_number)

if b == t or t == {'0'} or t == {'1'}:
    print(f'{binary_number} is a binary number')
else:
    print(f'{binary_number} is not a binary number')
    exit()
binaryToDecimal(final_number)
