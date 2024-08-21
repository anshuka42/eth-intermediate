# eth-intermediate
Etherium intermediate project
## Description
Here we have a contract error that demonstrates different ways to handle errors and validate conditions in Ethereum smart contracts. It includes examples of using require, revert, and assert statements, as well as custom error definitions.
## Getting Started
### Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., etherium_project.sol). 
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile" button.
Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar.
## TestRequire Function
The function checks if the input value _i is greater than 10.
If the condition is not met (i.e., _i is less than or equal to 10), the transaction is reverted, and an error message "Input must be greater than 10" is returned.
The require statement is commonly used to validate conditions such as function inputs, state conditions before execution, and return values from external function calls.
## TestRevert Function
Similar to testRequire, it checks if _i is greater than 10.
If _i is less than or equal to 10, the revert statement is called, which reverts the transaction and returns the error message "Input must be greater than 10".
revert is useful for complex error-checking conditions, allowing for more granular control over error handling.
## TestAssert Function
The assert statement is used to check for conditions that should never occur, indicating an internal error or an invariant violation.
In this case, the function asserts that the state variable num is always equal to 0.
If num is not 0, the transaction is reverted, and the error is flagged as a serious issue in the contract logic.
## Custom Error: InsufficientBalance
Custom errors allow for more efficient error handling, as they use less gas than require or revert statements with strings.
This custom error accepts two parameters: balance (the current balance) and withdrawAmount (the amount to be withdrawn).
## TestCustomError Function
The function retrieves the contract's current balance using address(this).balance.
It then checks if the balance is less than the withdrawal amount _withdrawAmount.
If the balance is insufficient, the function reverts the transaction using the custom error InsufficientBalance, passing the current balance and the withdrawal amount as parameters.
## Authors
Anshuka
github profile link:-https://github.com/anshuka42
## License

This project is licensed under the MIT License - see the Create LICENSE file for details
