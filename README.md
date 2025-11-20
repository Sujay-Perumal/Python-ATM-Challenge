# 🏧 ATM Transaction Validation Challenge

[![Language](https://img.shields.io/badge/Language-Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Platform](https://img.shields.io/badge/Platform-Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com/)
[![Status](https://img.shields.io/badge/Status-Completed-2AA854?style=for-the-badge)](https://github.com/Sujay-Perumal/ATM-Challenge-Python)

***

## Project Overview

This project implements a **Python program to simulate and validate core ATM withdrawal transactions**. The focus is on the logical flow, robust error handling, and state management necessary to process a user's withdrawal request successfully and safely.

The program simulates the critical checks an ATM performs, making it a robust exercise in fundamental programming logic and conditional execution.

### Key Objectives
* **Transaction Logic:** Successfully processing a withdrawal by correctly updating the account balance if all necessary conditions are met.
* **Input Validation:** Ensuring the requested amount is syntactically and logically valid (e.g., positive, integer, within ATM limits).
* **Balance Checking:** Preventing overdrafts by confirming the available balance is sufficient for the transaction.
* **Error Reporting:** Providing clear, specific messages for various transaction failures (e.g., "Insufficient funds," "Invalid amount").

***

## Skills Demonstrated

This challenge highlights strong competencies in **Python fundamentals, logical control flow, and exception handling**:

| Skill Focus | Description |
| :--- | :--- |
| **Python Fundamentals** | Strong command of functions, variables, basic data types (integers/floats), and conditional logic. |
| **Input Validation** | Implementing checks to ensure user input conforms to required formats (e.g., checking for positive numbers, integer values, and adherence to minimum denominations). |
| **Conditional Logic & Control Flow** | Utilizing comprehensive `if/elif/else` structures to manage different transaction states and failure modes accurately. |
| **State Management** | Tracking and updating the **`account_balance`** variable correctly after a successful withdrawal to reflect the new state of the system. |
| **Functional Design** | Structuring the solution into clear, distinct functions that handle specific responsibilities (e.g., checking validity, executing the transaction). |

***

## Access and Execution

This project is fully contained and executable directly via a Google Colab notebook, ensuring easy review and interaction without requiring local setup.

### 💻 Open the Notebook
**[Access the ATM Challenge Notebook (Google Colab)](https://colab.research.google.com/github/Sujay-Perumal/ATM-Challenge-Python/blob/main/ATM_challenge_Sujay.ipynb)**


## Example Logic Snippet

The core logic of the program involves checking a series of sequential conditions before executing the final balance update.

```python
# Pseudo-Code of the core validation logic

def withdraw(requested_amount, account_balance):
    if not isinstance(requested_amount, int) or requested_amount <= 0:
        return "Error: Invalid withdrawal amount. Must be a positive integer."
    
    # Assuming the ATM only dispenses multiples of 10
    if requested_amount % 10 != 0:
        return "Error: Withdrawal amount must be a multiple of 10."

    if requested_amount > account_balance:
        return "Error: Insufficient funds."
    else:
        # Transaction approved
        new_balance = account_balance - requested_amount
        return f"Success! New balance is: ${new_balance}"

# Example of a successful run
# print(withdraw(150, 500))  # Output: Success! New balance is: $350
