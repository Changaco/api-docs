**The Card Direct PayIn Object lets you pay with a registered Card (token)**. Here are the steps to follow:

1. Complete the CardRegistration steps (From 1. to 9. in the diagram)
2. Create a Direct `PayIn` object with the `CardId` received through the `CardRegistration` (10. in the diagram)
3. You need to do your tests in sandbox mode only with the testing cards

[alert type="info"]There is a KYC limit on Pay-Ins in order to fight fraud, money laundering and financing of terrorism. You have to send some documents through the API. [Please check the rules to go over the limits](/guide/kyc)[/alert]

# Payment Flow
Here is the CardRegistration flow (tokenization) then the Direct PayIn:
![alt](/uploads/medias/Scheme Card Registration.png)

[alert type="info"]**It is imperative to inform your users if you are registering their cards.**[/alert]

[alert type="info"]You can find more information about the difference between Payin through WEB interface and Direct payin [here](https://mangopay.desk.com/customer/portal/articles/1630150-what-is-the-difference-between-payin-direct-and-payin-through-web-interface-)

You can check here the [Fees rules](/guide/collecting-platform-fees)[/alert]