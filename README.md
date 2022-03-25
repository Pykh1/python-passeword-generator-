# python-passeword-generator-
By : Ada Lovelace
// Day 10
// Instruction 
  the project of today is to build this password generator.
creating a random password for the user based on the number of letters,symbols, 
  and numbers that they want...
  So it's going to ask us how many letters, how many symbols, how many numbers,
  password in a completely random order.

So instead of having it being, letter symbol number,
it should be maybe letter and then a symbol and then a number,
then a letter, then a symbol and then a number.
But notice how this is completely random and unpredictable. 
And every single time I generate a new password

// solution 
import random

print("welcome to python passeword generator")
ask_for_letters=int(input("How many letters would you like /in you passeword :"))
ask_for_symbols=int(input("How many symbols would you like in you passeword :"))
ask_for_numbers=int(input("How many Numbers would you like in you passeword :"))
letters=['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q','r', 's', 't', 'u', 'v', 'w', 'x', 'y', ' z','A', 'B', 'C', 'D', 'E', 'F', 'G', 'H','I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y','Z']
symbols=['{','}','(',')','[',']','.',',',':',';','+','-','*','/','&','|','<','>','=','~','$']
numbers= ['0','1','2','3','4','5','6','7','8','9']

passeword = []
for char in range(1,ask_for_letters+1):
     passeword +=random.choice(letters)
     
     
for char in range(1,ask_for_symbols+1):
     passeword +=random.choice(symbols)
     
     
for char in range(1,ask_for_numbers+1):
     passeword +=random.choice(numbers)
     
random.shuffle(passeword)


"""back shuffle list into string"""
final_passeword=""
for char in passeword:
    final_passeword+= char
print(f"the passeword is : {final_passeword}")


