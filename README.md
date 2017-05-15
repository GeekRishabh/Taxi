# TaxiApp - Documentation 



### Payment Gateway

 

PostInstall   
Run script  that ask for the payment gateway  that owner wants to configure . Get token/credentials from owner for different type of payment gateway like 

* Stripe
* Paypal
* Amazon

Getting token for all is optional . But add at least one  payment gateway . default is stripe .



Depending on the gateway configured create a JSON file eg\( paymentMode.JSON\) that will contain the details for the various payment gateway .

PaymentMode.JSON will look like

```

{
  strip :{
    authId:
    Key: 
  },
  paypal :{
    authId:
    Key: 
   },
  amazon :{
   authId:
   Key: 
  }
}
```

####   In FrontEnd 

  
The app will be configured based on the above file . Like if only one payment gatewaye is opted by owner then

the end user won't be prompted for the payment modes with other option other then \(credit card & cash \) .  
If the owner has configured more then one gateway . the the end user will get option like with payment gateway he will like to go with .   
  
Depending on the selected gateway the selected Class and functions will be executed in FrontEnd the the record will be saved in the backend along with the type of payment gateway the customer has opted . 

####   In Backend  

We can save the payment details . The modal can be someThing of this sort   
  


```
userEmail:
userId:
userType: DEFAULT Rider/Customer
paymentGateway: DEFAULT stripe
walletBalance : 
amountPaid: 
Depending on paymentGateway save the result i.e response data received from the server .
response : Type object 
```



