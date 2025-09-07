# Random.Password.generator-
import random
import string

def generate_password(length=12, use_upper=True, use_digits=True, use_special=True):
    """Generates a secure random password.

    Args:
        length (int): Length of the password.
        use_upper (bool): Include uppercase letters.
        use_digits (bool): Include digits.
        use_special (bool): Include special characters.

    Returns:
        str: Randomly generated password.
    """
    
    if length < 4:
        raise ValueError("Password length should be at least 4 characters.")

    # Base character sets
    lower = string.ascii_lowercase
    upper = string.ascii_uppercase if use_upper else ''
    digits = string.digits if use_digits else ''
    special = string.punct
