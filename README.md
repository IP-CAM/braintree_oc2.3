# Braintree payments for Opencart 2.3.x
TLT Braintree for Opencart 2.x

Braintree library version 3.23.0

---------
IMPORTANT
---------

If you get connection error like 'Cannot connect to the bank. Please try again later or use PayPal.' switch the debug mode to on, try to pay and check Opencart error log.

Message like 'Debug Info: #0 /path_to_opencart/system/braintree/lib/Braintree/Http.php(47): Braintree\Util::throwStatusCodeException(403)' means, that the Merchant Account ID value is not valid.

Open the Braintree settings and enter value from your Braintree credentials. Merchant account ID and Merchant ID are two different values with distinct purposes.

More information about it you can get from Braintree support article.
https://articles.braintreepayments.com/control-panel/important-gateway-credentials#merchant-account-id-vs.-merchant-id

Please also note, that Braintree credentials for sandbox and production are different. Don't mismatch it!

TLS 1.2 support

If your server isn't configured to use TLS 1.2 encryption by default you can enable TLS 1.2 in TLT Braintree settings. You need Braintree ver. 3.21.0 or more. Please note that in this case another parts of your shop can use less secure encryption, so is better to configure your server properly.

-------
INSTALL
-------

1. Upload all files from /upload folder to the root of your opencart installation. No files will be overwritten, if you install the extension first time.

2. The Braintree library is preinstalled, but to be sure you can always install the fresh instance:

2.1 Delete all files from system/braintree folder of your opencart installation 

2.2 Download Braintree library from https://developers.braintreepayments.com/start/hello-server/php

2.3 Unarchive the library and upload the /lib folder to the system/braintree folder of your opencart installation

2. Set up parameters, which you get from Braintree payment gateway.

3. Double check that the default merchant account currency matches to your store default currency. 

4. Check the credit cards logos, which you accept. Visa / Master / Discover are preinstalled. To change this list you should change the file image/logos/Cards.jpg.

5. Check the front-end messages for your customers. To change it edit the file catalog/language/en-gb/payment/braintree_tlt.php. 

-----
NOTES
-----

If your store is multi-currency you should get from Braintree Merchant Account ID for each currency used in your store. Otherwise a customer will be charged in your default currency. In this case you MUST notify your customer about it.

If the extension doesn't work please contact me.
