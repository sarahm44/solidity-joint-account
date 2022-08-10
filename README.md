# Solidity Smart Contract - Joint Savings Account

![](Images/20-5-challenge-image.png)

## Overview
I created a Solidity smart contract that accepts two user addresses, to automate the creation of joint savings accounts. These two addresses will be able to control a joint savings account. 

The smart contract uses ether management functions to implement a financial institution’s requirements for providing the features of the joint savings account. These features will consist of the ability to deposit and withdraw funds from the account.

See the file [joint_savings.sol](joint_savings.sol) containing the smart contract.

The folder ['execution_results'](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results) contains images confirming the deposit and withdrawal transactions designed to test the `JointSavings` functionality in the Remix VM (London) worked as expected.

## Steps Completed

The steps I completed are as follows:

1. Created a joint savings account contract in Solidity
2. Compiled and deployed the contract in the Remix VM (London) 
3. Interacted with the deployed smart contract

## Step 1: Create a Joint Savings Account Contract in Solidity

I created the smart contract for a joint savings account in Solidity. See part of the contract in the image below:

![](https://github.com/sarahm44/solidity-joint-account/tree/main/images/contract.png)

## Step 2: Compile and Deploy Contract in the JavaScript VM

I compiled the smart contract as shown below:

![](https://github.com/sarahm44/solidity-joint-account/tree/main/images/compile_and_run.png)

I then deployed the contract, as shown below:

![](https://github.com/sarahm44/solidity-joint-account/tree/main/images/compile_and_run.png)

## Step 3: Interact with Deployed Smart Contract

Once the contract was deployed, I tested its functionality.

### Use 'setAccounts' Function

I used the `setAccounts` function to define the authorized Ethereum addresses that will be able to withdraw funds from the contract:

![](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results/set_accounts.png)

See the transaction record below:

![](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results/set_accounts2.png)

### Test Deposit Functionality

I tested the deposit functionality of the smart contract by sending the following amounts of ether. After each transaction, I used the `contractBalance` function to verify that the funds were added to the contract.

#### Transaction 1: Send 1 ether as wei.

![](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results/1_ether.png)

![](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results/1_ether_balance.png)

#### Transaction 2: Send 10 ether as wei.

![](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results/10_ether.png)

![](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results/10_ether_balance.png)

#### Transaction 3: Send 5 ether.

![](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results/5_ether.png)

![](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results/5_ether_balance.png)

I used the website [Ethereum Unit Converter](https://eth-converter.com/) to assist doing the conversions of ether to wei.

### Test Withdrawal Functionality

Once I'd successfully deposited funds into the contract, I tested the contract’s withdrawal functionality. 

#### Withdraw 5 ether into `accountOne`

![](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results/5_ether_withdraw.png)

![](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results/5_ether_withdraw_bal.png)

#### Withdraw 10 ether into `accountTwo`

![](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results/10_ether_withdraw.png)

![](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results/5_ether_withdraw_bal.png)

#### Use the `lastToWithdraw` and `lastWithdrawAmount` functions to verify that the address and amount were correct.

![](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results/last_to_withdraw.png)

![](https://github.com/sarahm44/solidity-joint-account/tree/main/execution_results/last_withdraw_amount.png)
