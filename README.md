# password-generator
# 🔐 Password Generator (Python)

A simple **command-line password generator** written in Python.  
It allows users to generate different types of passwords based on their choice and desired length.

---

## 📌 Features

- Generate passwords using:
  - Lowercase letters
  - Uppercase + lowercase letters
  - Numbers only
  - Symbols only
  - Strong passwords (letters + numbers + symbols)
- User-friendly menu
- Random and secure password generation

---

## 🛠 Requirements

- Python 3.x  
- No external libraries needed (uses Python's built-in `random` module)

---

## ▶️ How to Run

1. Clone or download the repository
2. Open a terminal in the project folder
3. Run the program:

```bash
python password_generator.py
📋 Menu Options
markdown
Copy code
1. Lowercase password
2. Letters (Upper + Lower)
3. Numbers only
4. Symbols only
5. Strong password
6. Exit
🧠 How It Works
Characters are grouped into lists:

Lowercase letters

Uppercase letters

Numbers

Symbols

A dictionary maps user choices to the appropriate character set

A random password is generated using list comprehension

🧪 Example Output
pgsql
Copy code
🔐 PASSWORD GENERATOR MENU 🔐
Enter your choice: 5
Enter password length: 12
Generated Password: A9@fQ2!kZ#1m
