'''def first_n(n):
  build and return list
  num, nums = 0, []
  while num < 10:
    nums.append(num)
    num +=1
    return num
sum_of_first_n = sum (first_n (1000000))'''    

'''for loops
fruits = ["banana", "orange", "apple", "mandarine", "mango", "cherry"]
for x in fruits:
  print (x)
fruits = ["banana", "orange", "apple", "mandarine", "mango", "cherry"]
for x in fruits:
  if x == "banana":
    break
print (x)'''



import string
import random

# characters to generate password from
alphabets = list(string.acii_letters)
digits = list(string.digits)
special_characters = list("!@#$%^&*()")
characters = list(string.acii_letter+ string.digits + "!@#$%^&*()")


def generated_random_password():
  # lenght of password from the user 
 length = int (input("Enter password lenght: "))

 #number of character types
 alphabets_count = int(input("Enter what alphabets count in password: "))
 digits_counts = int(input("Enter digits count in password: "))
 special_characters_count = int(input("Enter special characters count in password: "))

 characters_count = alphabets_count + digits_count + special_chracters_count

 #check the total length with characters sum count #print not valid if the sum is greater than length
if characters_count > length:
  print("characters total count is greater than the password length")
  return

  # Initializing the passord
password = []

# Picking random alphabets
for i in range (alpabets_count):
  password.append(random.choice(alphabets))


# Picking random digits
for i in range (digits_count):
  password.append(random.choice(digits))

# picking random special characters
for i in range(spceial_characters-count()):
  password.append(random.choice(special_characters))

# if the total characters count is less than the password length, add, random characters to make it equal to the length
if characters_count < length:
  random.shuffle(characters)
  for i in range (length - characters_count):
    password.append(random.choice(characters))

# shuffling the resultant password
random.shuffle(password)

#converting the list to string and printing the list
print("".join(password))

# invoking the function
generate_random_password()
