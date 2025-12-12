# MyToken (MTK)

## Overview
MyToken is a simple ERC-20 token built on Ethereum for learning purposes.  
This project demonstrates how to deploy a token, transfer it, approve allowances, and use `transferFrom` on Remix IDE.

---

## Token Details
- **Name:** MyToken  
- **Symbol:** MTK  
- **Decimals:** 18  
- **Total Supply:** 1,000,000 MTK  

---

## Features
- Transfer tokens between accounts  
- Approve a spender to spend tokens  
- `transferFrom` functionality  
- Balance tracking  
- Event emission (`Transfer` and `Approval`)  

---

## How to Deploy
1. Open [Remix IDE](https://remix.ethereum.org/)  
2. Create a new file `MyToken.sol` in the `contracts/` folder  
3. Paste your ERC-20 contract code  
4. Compile using Solidity 0.8.x  
5. Deploy with an initial supply of `1000000 * 10^18` (considering 18 decimals)  

**Deployment Screenshot:**  
![Contract Deployment](screenshots/deploy.png)

---

## How to Use

### 1. Check Balance
- Function: `balanceOf(address)`  
- Returns token balance of any address.

### 2. Transfer Tokens
- Function: `transfer(address _to, uint256 _value)`  
- Example: Account 1 → Account 2, `1000000000000000000` (1 MTK)  

**Transfer Screenshot:**  
![Transfer](screenshots/transfer.png)

### 3. Approve a Spender
- Function: `approve(address _spender, uint256 _value)`  
- Example: Account 1 approves Account 3 for `5000000000000000000` (5 MTK)  

**Approve Screenshot:**  
![Approve](screenshots/approve.png)

### 4. TransferFrom by Spender
- Switch to the spender account (Account 3) in Remix  
- Function: `transferFrom(address _from, address _to, uint256 _value)`  
- Example: Account 3 moves `5000000000000000000` (5 MTK) from Account 1 → Account 2  

**TransferFrom Screenshot:**  
![TransferFrom](screenshots/transferFrom.png)

### 5. Check Remaining Allowance
- Function: `allowance(address owner, address spender)`  
- Example: `allowance(Account 1, Account 3)`  
- Should return remaining allowance (0 after transfer)  

**Allowance Screenshot:**  
![Allowance](screenshots/allowance.png)

---

## Notes / Edge Cases
- **Do not** transfer to zero address  
- **Do not** transfer more than your balance  
- `transferFrom` fails without sufficient allowance  

---

## Folder Structure Suggestion
