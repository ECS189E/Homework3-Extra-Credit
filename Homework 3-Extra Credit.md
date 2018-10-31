# ECS189E Homework 3 - Extra Credit

## Directly Show Wallet
Normally if an auth token can be found, the whole login and verification process should be skipped for the user. As a result, check for the auth token even before loading the first view, and show the right view according to the result.

Hint: Storyboard entry point, AppDelegate.

## Allow Account Modifications

1. Allow user to change the name of the account.  
2. Allow user to delete an account.  
3. Allow user to create a new account (with amount 0.0).
4. Should not allow user to modify the ID.
5. Should not allow user to modify the amount.

## Allow Transactions
1. Allow user to deposit to an account.
2. Allow user to withdraw from an account.
3. Allow user to make transactions between two accounts.

To be more specific, when it comes to the case of deposit and withdraw, the money is coming from "nowhere" and going to "nowhere". Like the ATM, take them as cash in and cash out. However, you need to limit the amount of money for withdraw and transfer. The account amount should not go under 0.

You are not allowed to directly change account amount on the client side. It is required to use the functions provided in Api.swift and make the changes on server side.

## Save the Accounts data to server
The function `Api.setAccounts` will allows you to save the data on server by passing the `wallet.accounts`. In the `init` of class `Wallet` in classes.swift file, if you pass `false` to `ifGenerateAccounts`, it will try to parse the account data from the `response`, and will give you a empty `[Account]` if there is no accounts data saved on server. You can save the data each time user complete any transactions, or only when user is logging out.

**You have to complete one of the "Allow Account Modifications" and "Allow Transactions" in order to receive scores from this section.**

## Great UI design, UX design, Animation
This will be graded as an overview for the whole App instead of one or two functions that was not required. I will bring out my "real" standard.

## Grading
1. Directly Show Wallet (5')
2. Allow Account Modifications (10')
3. Allow Transactions (10')
4. Save the Accounts data to server (5')
5. Great UI design, UX design, Animation (5')

## Submission
Push your files to the repository.
