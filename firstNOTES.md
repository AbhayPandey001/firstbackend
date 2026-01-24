# Basics 
in this , we are going to create a server , it means a software that serves.  
## kya karenge ? 
ek taraf computer / mobile hai jo request bhejta hai , dusri side server hai jo us req ko lekar response bana ke bhejta hai   
ham woh server hi banayege   
woh karne ke liye **Express** naam ki library use hoti hai  

sabse pehle , kisi folder ko open karke 
```
npm init
```
aisa karne se woh folder ek node ka project ban jata hai and uske baad ham various node packages install kar sakte hain like npm install express  
Isse ek **package.json** file milti hai


us package.json file me ek scripts tag hota hai . Waha jaake ham app ke running ke liye command de sakte hain 
```
"scripts": {
    "start": "node index.js"
  },
```
aisa karne se ab aage se node index.js karke file ko run nahin karna padega , directly npm run start karne se ho jayega
```
 npm install express
 ```

 it generates  node modules   
 ab expess install hogaya hai , now we go to docs (https://expressjs.com/en/starter/hello-world.html), helloworld program , copy paste....    
 we get few things the top line requires express and then uski help se ek app object banate hain   
 just like  Math object bana lene se ham math.pi , .random etc kar sakte hain , app banane se bhi ham waise hi  
  express ke sari methods ko use kar sakte hain

## requests and listening 
now the request that the computer/mobiles send are of various types , here we see the get type 
the server on the other hand cotiniously listens on a specified port , so that when someone goes to that port it serves what is needed .   
also we can set
get requests for various routes such as /hello /account /about (**NOTE** : / is called home route)

run karne pe jaise normal js files close hojati thi , ye close nahi hoti as server continiously listen karta rehta hai

## note
jaise hi server mein kch change karte hain to firse processing karni padti hai so close karke **(ctrl + c)** then firse **npm run start** karo then changes will be visible ,  

future mein kch package install karege uske liye bhi


## dotenv
is code ko production mein le jaane ke liye bas ek chiz aur lagti hai environment variables , ye protect krte hain sensitive information 
```
npm i dotenv
```
now make a file with .env (only .env)  
uske andar sensitive information such as **PORT  = 4000** dedo (in capital) and then to use it anywhere   
in top :: **require('dotenv').config()**
to use it in code :: **process.env** ke baad ek dot laga ke property ka naam such as PORT

and the code will now run at port 4000


## last m deploy to production bhi dekha tha