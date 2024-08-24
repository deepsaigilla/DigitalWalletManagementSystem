###### This README provides a comprehensive overview of the Digital Wallet Management System project. If there are any specific details or sections you would like to add or modify, please let me know!

# Digital Wallet Management System
A Digital Wallet Management System is a software platform that allows users to manage their financial transactions digitally. It enables transferring and receiving funds, and viewing account balances. This system ensures secure, fast, and convenient transactions, streamlining financial management for users.

## Overview
This repository contains a C++ implementation of a Digital Wallet Management System. The system is designed to handle financial transactions between users, validate the transactions, and then sort and display users based on their remaining balances.

## Problem Description
The Digital Wallet Management System allows users to manage their finances by facilitating transactions between them. The system:

1. Maintains a list of users with their initial balances.
2. Processes a series of transactions.
3. Provides feedback on whether each transaction was successful or failed due to insufficient funds.
4. Sorts and displays users by their remaining balances.

## Input Format
* The first line contains an integer 'n', the number of users.
* The next 'n' lines each contain two integers: 'userID' and 'balance'.
* The next line contains an integer 'q', the number of transactions.
* The next 'q' lines each contain three integers: 'from_userID', 'to_userID', and 'amount'.

## Constraints
* 1 ≤ N ≤ 10<sup>2</sup>
* 1 ≤ userID ≤ 10<sup>2</sup>
* 0 ≤ balance ≤ 10<sup>4</sup>
* 1 ≤ T ≤ 10<sup>3</sup>
* 0 ≤ amount ≤ 10<sup>4</sup>
  
## Output Format
For each transaction, the program prints "Success" if the transaction is completed or "Failure" if it fails.
After all transactions are processed, the program prints the user IDs and their balances, sorted by balance in ascending order.

## Sample Input
4

1 9000

2 3000

3 7500

4 2000

5

1 2 1000

3 4 3000

2 3 500

4 1 7500

1 4 1500

## Sample Output
Success

Success

Success

Failure

Success

&nbsp;

2 3500

3 5000

1 6500

4 6500


## Solution Explanation
The solution is implemented in C++ using a 'map' to store and manage the balances of users and a 'multimap' to sort users based on their remaining balances after all transactions are processed.
#### Note:
A multimap is similar to a map, but it allows to store multiple values with the same key.

### Key Components
* **Balance Management**: The 'map<int, int>' balance stores the user ID and balance pairs. This allows for efficient lookups and updates during transactions.
* **Transaction Processing**: The system checks whether the 'from_userID' has sufficient funds to complete the transaction. If successful, the balances are updated, and "Success" is printed; otherwise, "Failure" is printed.
* **Sorting**: The 'multimap<int, int>' sorted is used to automatically sort users by their balances. This data structure allows for easy insertion and automatic sorting based on the key (balance).
* **Output**: Finally, the program outputs the sorted list of users with their remaining balances.

## Conclusion
This code offers an efficient and easy-to-understand solution for managing digital wallet transactions, ensuring that all transactions are validated and that users are presented in a sorted manner based on their remaining balances. The use of 'map' and 'multimap' makes the implementation both clear and efficient, adhering to the problem constraints.
