# Password generator
import random # Different types of element random gaa generator avuthayii
lower="bhargav"
upper="BHARGAV"
numbers="0123456789"
symbols="@#"
all=lower+upper+numbers+symbols
lenght=7
for i in range(6):    
    password=" ".join(random.sample(all,lenght))
    print(password)
# Model-2
# Password generator
import string
import random
def generate_password(min_length, numbers=True, special_characters=True):
    letters = string.ascii_letters
    digits = string.digits
    special = string.punctuation

    characters = letters
    if numbers:
        characters += digits
    if special_characters:
        characters += special

    while True:
        pwd = ''.join(random.choice(characters) for i in range(min_length))
        if (numbers and any(c.isdigit() for c in pwd) and
            special_characters and any(c in special for c in pwd)):
            return pwd

min_length = int(input("Enter password length: "))
has_number = input("Do you want numbers (yes/no)? ").lower() == "yes"
has_special = input("Do you want to have special characters (yes/no)? ").lower() == "yes"  # Complete the input line
lenght=6
for i in range (6):
    print(password)
    password = generate_password(min_length, has_number, has_special)
    print("Your generated password is:", password)  # Print the password

    
