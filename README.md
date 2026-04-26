# github-final-project
final project from IBM full stack Certificate- git and github course
# Simple Interest Calculator

## Overview
The **Simple Interest Calculator** is a straightforward tool designed to compute the interest accrued on a principal amount over a specific period at a fixed interest rate. Unlike compound interest, simple interest is calculated only on the initial principal amount.

## Purpose
This calculator is useful for quick financial estimations, educational purposes, and basic loan or investment tracking. It helps users understand how much interest they will pay or earn without the complexity of compounding periods.

## How It Works
The calculator uses the standard simple interest formula:

**`I = P * r * t`**

Where:
* **`I`** = Total Interest Amount
* **`P`** = Principal Amount (the initial sum of money)
* **`r`** = Annual Interest Rate (in decimal form, e.g., 5% = 0.05)
* **`t`** = Time (in years)

To find the total accumulated amount (Principal + Interest), the formula is:

**`A = P(1 + rt)`**

## Code Snippet
Below is a simple implementation of the Simple Interest Calculator in Python:

```python
def calculate_simple_interest(principal, rate, time):
    """
    Calculates the simple interest and total amount.
    
    :param principal: The initial amount of money (float)
    :param rate: The annual interest rate as a percentage (float)
    :param time: The time the money is invested or borrowed for, in years (float)
    :return: A tuple containing the interest and the total amount
    """
    # Convert percentage to decimal
    decimal_rate = rate / 100
    
    # Calculate interest
    interest = principal * decimal_rate * time
    
    # Calculate total amount
    total_amount = principal + interest
    
    return interest, total_amount

# --- Example Usage ---
P = 1000.00  # $1,000 principal
R = 5.0      # 5% annual interest rate
T = 3        # 3 years

interest_earned, final_balance = calculate_simple_interest(P, R, T)

print(f"Principal: ${P:,.2f}")
print(f"Interest Earned: ${interest_earned:,.2f}")
print(f"Total Amount: ${final_balance:,.2f}")
