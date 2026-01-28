# password-generator
# 🔐 Password Generator (Python)

This is a simple **menu-driven password generator** program written in Python.  
It allows users to generate different types of passwords based on their choice and desired length.

---

## ✨ Features

- Generate passwords using:
  - Lowercase letters only
  - Uppercase + lowercase letters
  - Numbers only
  - Symbols only
  - Strong passwords (letters + numbers + symbols)
- Uses Python’s built-in `random` module
- Easy-to-use command-line menu

---

## 📋 Program Menu
1. Lowercase password
2. Letters (Upper + Lower)
3. Numbers only
4. Symbols only
5. Strong password
6. Exit

## 🧠 Source Code

      
       import random

---------- FUNCTION ----------

def generate_password(length, choice):

    # Nested List
    char_groups = [
        list("abcdefghijklmnopqrstuvwxyz"),
        list("ABCDEFGHIJKLMNOPQRSTUVWXYZ"),
        list("0123456789"),
        list("!@#$%^&*")
    ]

    # Dictionary
    char_dict = {
        1: char_groups[0],                         # lowercase
        2: [*char_groups[0], *char_groups[1]],     # letters
        3: [*char_groups[2]],                      # numbers
        4: [*char_groups[3]],                      # symbols
        5: [*char_groups[0], *char_groups[1],
            *char_groups[2], *char_groups[3]]      # strong
    }

    # List Comprehension
    password_list = [random.choice(char_dict[choice]) for _ in range(length)]

    # Loop
    password = ""
    for ch in password_list:
        password += ch

    return password


# ---------- MAIN PROGRAM ----------


 
while True:
    print("\n🔐 PASSWORD GENERATOR MENU 🔐")
    print("1. Lowercase password")
    print("2. Letters (Upper + Lower)")
    print("3. Numbers only")
    print("4. Symbols only")
    print("5. Strong password")
    print("6. Exit")

    choice = int(input("Enter your choice: "))

    if choice == 6:
        print("Thank you! Program ended.")
        break

    length = int(input("Enter password length: "))

    password = generate_password(length, choice)
    print("Generated Password:", password)

## 🧪 Sample Output


🔐 PASSWORD GENERATOR MENU 🔐

Enter your choice: 5

Enter password length: 10

Generated Password: A9@kP2!fQ#
