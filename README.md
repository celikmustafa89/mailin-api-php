# SendinBlue Php Library

This is the SendinBlue Php library. It implements the various exposed APIs that you can read more about on https://developers.sendinblue.com/docs.

SendinBlue API's use HTTP Authentication through an api key. You can create your api key from [API Console](https://my.sendinblue.com/advanced/apikey), after you sign up for an account with SendinBlue. You must use latest version 2.0, access key, for accessing APIs.

This library 
## Installation & Configuration
1. ```composer require celikmustafa89/sendinblue-api-php```
2. following field must be added to .env file.
```
# you can get sendinblue api-key from: https://account.sendinblue.com/advanced/api
# you can get sendinblue mail-list-id from: https://my.sendinblue.com/lists
SENDINBLUE_URL=https://api.sendinblue.com/v3/
SENDINBLUE_APIKEY=XXXXXXXX<your-api-key>XXXXXXXXXX
SENDINBLUE_MAIL_LIST_ID=2
```
## Quickstart Guide

Learn how to send email campaigns from your application using SendinBlue API.

You must sign up for SendinBlue account for using APIs. All our APIs require HTTP authentication using access key, which are accessible from your [API Console](https://my.sendinblue.com/advanced/apikey).

The following guides give you a start and understanding of how to use our API.

 * [Get all your campaigns](https://apidocs.sendinblue.com/how-to-get-all-you-campaigns/)
 * [Send transactional emails](https://apidocs.sendinblue.com/tutorial-sending-transactional-email/)
 * [Setup your webhooks](https://apidocs.sendinblue.com/how-to-setup-webhooks/)


## Support and Feedback

Be sure to visit the SendinBlue official [documentation website](https://apidocs.sendinblue.com) for additional information about our API.

We also support [Composer](https://packagist.org/packages/mailin-api/mailin-api-php).

If you find a bug, please submit the issue in [Github directly](https://github.com/mailin-api/mailin-api-php/issues). 

As always, if you need additional assistance, drop us a note [here](https://apidocs.sendinblue.com/support/).
