# Ali_Khatami_ChainlinkVRF(learning from the video of Stephen Fluin)

###  Introduction

With Chainlink VRF version 2 we are gonna fund subscription which is basically an account that allows to fund and maintain balance <br>
for multiple consumer contracts <br>

![l27](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/32e10b00-37c2-4913-801c-c81eb57beb1f)


We will go to the above link https://docs.chain.link/getting-started/intermediates-tutorial
and click the get random number shown with black arrow and click Subscriptions manager shown <br>
with blue arrow <br>

![l28](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/b9f8e78c-f4a9-4206-8677-7d240a55736b)

Then we will connnect wallet button here <br>

![l29](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/7af0e328-fbbc-42cd-a9c6-5f175c8f9a4b)

Then we will ckick Create subscription button <br>

![l30](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/1ac48ec7-0557-4d02-a21b-73b2bcb5d769)
here I will use my address as a subscription address <br>

![l31](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/c2fc488b-e05f-48ea-b73f-ae0694123d32)

here we will click the Sign button <br>

![l32](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/109feb6d-06a7-450f-9505-a1b01b1f2722)

Here we will click the Confirm button <br>

![l33](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/2a166f6d-dada-47b6-af21-73c04181e03a)

Thus the Subscriptio is successfully created <br>

Now ew have subscription where we gonna fund it <br>

And we can use that account for all of our random request <br>


![l34](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/0739311e-20d5-49d8-a19f-b6059c3620a0)

We gonna put 10 links you can put whatever you want <br>


![l35](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/ef015b96-b2a1-4190-9dcb-80f73c070d04)

Then we will click the Confirm button <br>

![l36](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/57160cac-b685-4082-8d52-c1a2931176cf)


Thus the fund is added and we will now add consumer <br>

The price and link of evry random number you passed will be based on current gas rates on a given chain as well as gas you choose <br>

![l37](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/8e98cd5e-3518-4fa0-8b26-30ea7e081767)

we have no consumer address <br>

![l38](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/0a058ea3-17e5-4b35-8322-ba4d75852851)

For that we have to link the link below and a contract will be open at REMIX IDE <br>


![l39](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/594b336f-a40e-4983-ac2a-ac02f102fc6d)


This is the contract that opened at REMIX IDE <br>


![l40](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/ecebac4b-28df-4267-82d4-189af6c020ff)

Here at the top we have two important imports <br>


![l41](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/b3e1dcfe-7d00-49bb-9fa8-3912beb84ece)

The key hash option is a way that we specify the gas line was specified in the documentation <br>


So depending on the key hash we choose for the given chain we are on the gas limit will be set differently <br>
for our random number request <br>


![l42](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/5dfe1038-ee47-460e-be0b-83da6889ca97)

here above ```uint32 callbackGasLimit = 40000;```  that we are in charge of <br>

So depending on how much gas we want to spend to fulfill a random number we must set this value appropriately <br>

![l43](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/c9af3499-982a-4693-8774-3e527a930908)

Another most important and useful features that gives a lot more flexibility and control of our VRF <br>

is the number of random numbers we want for that the above white arrow marked variable we use 

![l44](https://github.com/C191068/Ali_Khatami_ChainlinkVRF/assets/89090776/782a4918-ad63-4b5a-8ff7-c6131b2a03a7)

In the above constructor we can see address to the coordinator and the subscription that will be created as <br>
we deploy the contract <br>












