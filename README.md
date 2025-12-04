⸻

Password Strength Checker

Overview

The Password Strength Checker is a C program that analyzes the strength of a password based on multiple criteria. It evaluates whether a password is strong, medium, or weak, and provides suggestions for improvement to make passwords more secure.
____

Features
	•	Checks if the password length is at least 8 characters.
	•	Detects presence of:
	•	Uppercase letters
	•	Lowercase letters
	•	Numbers (digits)
	•	Special characters (punctuation)
	•	Assigns a score out of 5 based on password complexity.
	•	Provides user-friendly suggestions to improve password strength.
	•	Allows the user to re-enter passwords and check multiple passwords in a single session.

⸻

How It Works
	1.	The program prompts the user to enter a password.
	2.	It evaluates the password based on the following criteria:
	•	Length ≥ 8 characters
	•	Contains uppercase letters
	•	Contains lowercase letters
	•	Contains numbers
	•	Contains special characters
	3.	Each satisfied criterion adds 1 point to the score (maximum score: 5).
	4.	The program then prints a detailed analysis and the overall strength:
	•	Very Strong: 5/5
	•	Medium: 3–4/5
	•	Weak: < 3
	5.	If the password is weak or medium, the user can opt to receive suggestions and enter a stronger password.
	6.	Users can check multiple passwords in one session.

⸻

Usage
	1.	Compile the program using a C compiler:

gcc password_checker.c -o password_checker


	2.	Run the program:

./password_checker


	3.	Enter the password you want to check.
	4.	Follow the prompts to see the strength and suggestions.
	5.	Optionally, enter a new password to improve its strength.

⸻

Example Output

Enter a password to check its strength: Test123
--- Password Analysis ---
Length (>=8):        No (Length = 7)
Has Uppercase:       Yes
Has Lowercase:       Yes
Has Digit:           Yes
Has Special Char:    No

Total Score: 3 / 5
Overall Strength: Medium

Do you want to make it strong? (y/n): y

Tips to make your password strong:
1. Use at least 8 characters.
2. Mix uppercase and lowercase letters.
3. Add numbers (0-9).
4. Include special characters (!@#$%^&*).

Enter a new (stronger) password: Test123!
--- Password Analysis ---
Length (>=8):        Yes (Length = 8)
Has Uppercase:       Yes
Has Lowercase:       Yes
Has Digit:           Yes
Has Special Char:    Yes

Total Score: 5 / 5
Overall Strength: Very Strong


⸻

Functions

int checkPasswordStrength(char *password)
	•	Checks password length, character types, and calculates a score.
	•	Displays detailed analysis of the password.

void suggestImprovements()
	•	Provides tips for creating stronger passwords.

⸻

Notes
	•	Maximum password length supported: 200 characters.
	•	The program handles newline characters (\n) entered by the user.
	•	Case-insensitive input is supported for prompts (y/Y or n/N).

