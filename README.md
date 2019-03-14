# Capped Crowdsale

Solidity contract for a simple capped crowd sale token

Written by **Benson Yang**

Uses :

 Truffle v4.1.15

 Solidity v0.4.25

 Web3 v0.20.7

## Getting Started

Install Truffle v4.1.15 by doing : npm install -g truffle@4.1.15

Install npm by doing : npm install

## Tutorials Used

[How To Build A Simple Capped Crowdsale Token Using OpenZeppelin Library — Part 1](https://medium.com/crowdbotics/how-to-build-a-simple-capped-crowdsale-token-using-openzeppelin-library-part-1-2789ec642308)

[How To Build A Simple Capped Crowdsale Token Using OpenZeppelin Library — Part 2](https://medium.com/crowdbotics/how-to-build-a-simple-capped-crowdsale-token-using-openzeppelin-library-part-2-cf96cb66c3d0)



### Downloads

Webstorm IDE. Download [here](https://www.jetbrains.com/webstorm/).

### Running the program

To see code, download the program and open it using Webstorm.

To run, open using terminal and go to file location.

Run these in order :
 
    1. truffle compile
    
    2. truffle develop
    
    3. migrate --reset
    
Program is now ready to run.

### Tutorial Questions

 Format is "ExampleToken.deployed(_Name,_Symbol,_Decimal).then((t) => {token = t;})"

![alt text](https://github.com/byangschool/CCC/blob/master/Images/Tut1.png)
 
  Format is "ExampleTokenCrowdsale.deployed(_rate,_wallet,_token,_cap)).then((t) => {token = t;})"
 
  ![alt text](https://github.com/byangschool/CCC/blob/master/Images/tut2.png)
  
   Format is "token.transferOwnership(sale.address)"
  
   ![alt text](https://github.com/byangschool/CCC/blob/master/Images/tut3%20owner.png)
   
  Number 1 :
    
   ![alt text](https://github.com/byangschool/CCC/blob/master/Images/tutQ1.png)
   
    Error due to the minimum contribution cap being set to 2 ether, and you are trying to buy with 1 ether
    
  Number 2 :
    
   ![alt text](https://github.com/byangschool/CCC/blob/master/Images/tutQ2.png)
     
     Successful since minimum contribution cap is 2 ether, and you are trying to buy with 2 ether
     
  Number 3 :
     
   ![alt text](https://github.com/byangschool/CCC/blob/master/Images/tutQ3.png)
      
      Successful since HardCap is equal to 50 ether, and 2 + 48 = 50 ether
      
  Number 4 : 
      
   ![alt text](https://github.com/byangschool/CCC/blob/master/Images/tutq4.png)
       
       Error due to it passing the HardCap. 50 + 1 = 51 ether.
    
### Homework Questions

Number 1 : Change the minimum contribution to 5 ether. (20points)

 ![alt text](https://github.com/byangschool/CCC/blob/master/Images/updateMin.png)

Number 2 : Add method, getTokensLeft, to report how many tockens are left. (30points)

 ![alt text](https://github.com/byangschool/CCC/blob/master/Images/hw%232.png)
 
 Number 3 : Graduate Students question : Add the needed functionality to not allow more than 1 purchase per account. (40 points)
 
 Did not attempt
 
 ### Now evaluate your contract with the following parameters :
 
 Token name : "CSC4980 Token"
 Token symbol : "GSU"
 Token decimals : 18
 Rate : 450 tokens x Ether
 Cap : 150 Ether
 
 ### Repeat steps above
 
 ![alt text](https://github.com/byangschool/CCC/blob/master/Images/assi1.png)
 
 ![alt text](https://github.com/byangschool/CCC/blob/master/Images/assi2.png)
 
 ![alt text](https://github.com/byangschool/CCC/blob/master/Images/assi3.png)
 
 Number 1 : Try to buy tokens with 2.5 ether (10 points)
 
  ![alt text](https://github.com/byangschool/CCC/blob/master/Images/assiQ1.png)
  
  Error due to us raising the minimum contribution to 5 ether, and you trying to buy with 2.5 ether.
  
 Number 2 : Buy tokens with 15 ethers (10 points)
  
   ![alt text](https://github.com/byangschool/CCC/blob/master/Images/assiQ2.png)
   
   Successful since minimum contribution is 5 ether, and you are buying with 15 ether.
   
 Number 3 : Return how many tokens are left (10 points)
   
   ![alt text](https://github.com/byangschool/CCC/blob/master/Images/assiQ3.png)
    
 Number 4 : Graduate Students : Buy tokens (again) with 25 ether (10 points)
    
   ![alt text](https://github.com/byangschool/CCC/blob/master/Images/assiQ4.png)
     
     Successful since HardCap is 50 and only 25+15 Ether has been used to buy
     
   
   
