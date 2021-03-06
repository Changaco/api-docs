You need to register a card in order to process a [textdirect PayIn](https://docs.mangopay.com/api-references/payins/payindirectcard/). **Card registration enables you to tokenize a Card**. These are the steps to follow:
1. Create a « CardRegistration » Object (1. 2. & 3. in the diagram)
2. Get a « PreRegistrationData » key (4. in the diagram)
3. The user posts « PreRegistrationData », « AccessKey » and card details through a form ([PHP](https://github.com/MangoPay/mangopay2-php-sdk/tree/master/demos/paymentDirect) & [JS](https://github.com/MangoPay/mangopay2-php-sdk/tree/master/demos/paymentDirect/js) samples) to the « CardRegistrationURL » (5. in the diagram)
4. Get a « RegistrationData » back (6. in the diagram)
5. Edit the « CardRegistration » Object (POST method) with the « RegistrationData » just received (7.8. in the diagram)
6. Get the CardID ready to use into the « [Direct PayIn](https://docs.mangopay.com/api-references/payins/payindirectcard/) » Object (9. in the diagram)

* If you don’t want to save the card you must change the field ACTIVE in the card object to false as shown in the document [Consult a card Object](https://docs.mangopay.com/api-references/card/)
* **You need to do your tests in sandbox mode only with the [testing cards](https://docs.mangopay.com/api-references/test-payment/)**
* **From 24/02/2015, some out-dated browsers will not support payin webs nor card registrations – [more info](https://docs.mangopay.com/payment-security-enhancement-browser-obsolescence/)**
* **IMPORTANT**: card details must never pass via your server – therefore you must use the card registration process given below and not implement a different system where the card details may touch your server and then you use cURL etc to create the card – (this approach or anything similar) is strictly not allowed

**Registration Flow**
[alert type="info"]The card registration method lets you customise your payment page. This page can be hosted on your own.[/alert]

Here is the registration flow (the last step correponds to the [Direct PayIn](https://docs.mangopay.com/api-references/payins/payindirectcard/)):
http://demo.dev-app.net/uploads/medias/SchemeCardRegistration.png

[alert type="info"]N.B.: 
* It is imperative to inform your users if you are registering their cards
* The validity of a registered card (CardId) before a payment or a pre-authorisation is 30min maximum. Once one of these operations is made, the card « validity » field change to « VALID ». Then, it is available up to the expiry date
* TIP : You can download our graphic [KIT](http://docs.mangopay.com/files/2013/09/KIT.zip)
* The validity of a registered card (CardId) before a payment or a pre-authorisation is  30min maximum. Once one of these operations is made, the card « validity » field change to « VALID ». Then,it is available up to the expiry date.
[/alert]