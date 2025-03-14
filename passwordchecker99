
import re

def password_strength(password):
    # Criteria counters
    length_score = 0
    upper_score = 0
    lower_score = 0
    digit_score = 0
    special_score = 0
    
    # Check password length
    if len(password) >= 8:
        length_score = 1
    if len(password) >= 12:
        length_score = 2
    if len(password) >= 16:
        length_score = 3

    # Check if password has uppercase letter
    if re.search(r'[A-Z]', password):
        upper_score = 1

    # Check if password has lowercase letter
    if re.search(r'[a-z]', password):
        lower_score = 1

    # Check if password has a digit
    if re.search(r'[0-9]', password):
        digit_score = 1

    # Check if password has special characters
    if re.search(r'[!@#$%^&*(),.?":{}|<>]', password):
        special_score = 1

    # Calculate the total score
    total_score = length_score + upper_score + lower_score + digit_score + special_score
    
    # Determine the strength of the password
    if total_score == 0:
        strength = "Very Weak"
    elif total_score == 1:
        strength = "Weak"
    elif total_score == 2:
        strength = "Medium"
    elif total_score == 3:
        strength = "Strong"
    else:
        strength = "Very Strong"

    # Print results
    print(f"Password: {password}")
    print(f"Strength: {strength}")
    print(f"Total Score: {total_score}/5")
    return strength

# Example usage:
password = input("Enter your password: ")
password_strength(password)
