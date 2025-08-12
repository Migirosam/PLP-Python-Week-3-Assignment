# Discount Calculator

## Overview

This repository contains two Python programs that work together to calculate the final price of an item after applying a discount. The programs allow users to input the original price and the discount percentage, providing a clear output based on the discount criteria.

## Program 1: `calculate_discount`

The first program defines a function named `calculate_discount` that takes two parameters:

- `price`: The original price of the item.
- `discount_percent`: The percentage of discount to be applied.

### Functionality

- If the discount percentage is 20% or higher, the function calculates the final price after applying the discount.
- If the discount percentage is less than 20%, the function returns the original price.

### Code

```python
def calculate_discount(price, discount_percent):
    """Calculate the final price after applying a discount."""
    if discount_percent >= 20:
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
        return final_price
    else:
        return price
Program 2: User Interaction
The second program prompts the user to enter the original price and discount percentage, then uses the calculate_discount function to determine and print the final price.

Code
python

Run

Copy
if __name__ == "__main__":
    # Prompt user for input
    original_price = float(input("Enter the original price of the item: "))
    discount_percent = float(input("Enter the discount percentage: "))

    # Calculate final price
    final_price = calculate_discount(original_price, discount_percent)

    # Print the final price
    if final_price < original_price:
        print(f"The final price after applying the discount is: ${final_price:.2f}")
    else:
        print(f"No discount applied. The original price is: ${final_price:.2f}")
How to Use
Clone the repository to your local machine:

bash

Copy
git clone https://github.com/yourusername/discount-calculator.git
Navigate to the repository directory:

bash

Copy
cd discount-calculator
Run the Python script:

bash

Copy
python script_name.py
Replace script_name.py with the name of your Python file.

Follow the prompts to enter the original price and discount percentage.
