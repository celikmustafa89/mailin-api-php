# SendinBlue Php Library

This is the SendinBlue Php library. It implements the various exposed APIs that you can read more about on https://apidocs.sendinblue.com.


## Example Codes
You can use below sample script to get started.

```PHP
<?php
/**
 * Created by PhpStorm.
 * User: mustafa çelik
 * Email: celikmustafa89@gmail.com
 * Date: 30.04.2018
 * Time: 17:51
 */


require('Mailin.php');
/*
 * This will initiate the API with the endpoint and your access key.
 *
 */
$mailin = new Mailin('https://api.sendinblue.com/v3/','Your access key');

/*
 * This will send a transactional email
 *
 */
/** Prepare variables for easy use **/

$data = array( "to" => array("to@example.net"=>"to whom!"),
    "cc" => array("cc@example.net"=>"cc whom!"),
    "bcc" =>array("bcc@example.net"=>"bcc whom!"),
    "from" => array("from@email.com","from email!"),
    "replyto" => array("replyto@email.com","reply to!"),
    "subject" => "My subject",
    "text" => "This is the text",
    "html" => "This is the <h1>HTML</h1><br/>
					   This is inline image 1.<br/>
					   <img src=\"{myinlineimage1.png}\" alt=\"image1\" border=\"0\"><br/>
					   Some text<br/>
					   This is inline image 2.<br/>
					   <img src=\"{myinlineimage2.jpg}\" alt=\"image2\" border=\"0\"><br/>
					   Some more text<br/>
					   Re-used inline image 1.<br/>
					   <img src=\"{myinlineimage1.png}\" alt=\"image3\" border=\"0\">",
    "attachment" => array(),
    "headers" => array("Content-Type"=> "text/html; charset=iso-8859-1","X-param1"=> "value1", "X-param2"=> "value2","X-Mailin-custom"=>"my custom value", "X-Mailin-IP"=> "102.102.1.2", "X-Mailin-Tag" => "My tag"),
    "inline_image" => array('myinlineimage1.png' => "your_png_files_base64_encoded_chunk_data",'myinlineimage2.jpg' => "your_jpg_files_base64_encoded_chunk_data")
);

var_dump($mailin->send_email($data));

//            var_dump($mailin->get_account());
//            var_dump($mailin->get_smtp_details());

//            $data = array("limit" => 10, "offset" => 0);
//            var_dump($mailin->get_folders($data));

//            $data = array("name" => "test_folder");
//            var_dump($mailin->create_folder($data));

//            $data = array("folderId" => "5");
//            var_dump($mailin->get_folder($data));

//            $data = array("folderId" => "4", "name" => "test_folder_rename1");
//            var_dump($mailin->update_folder($data));

//            $data = array("folderId" => "4");
//            var_dump($mailin->delete_folder($data));

//            $data = array("limit" => "410", "offset" => "0");
//            var_dump($mailin->get_folder($data));

//            $data = array("folderId" => 1, "limit" => "410", "offset" => "0");
//            var_dump($mailin->get_folder($data));

//            $data = array("folderId" => 1, "name" => "deneme_list");
//            var_dump($mailin->create_list($data));

//            $data = array("folderId" => 1, "name" => "deneme_list");
//            var_dump($mailin->create_list($data));

//            $data = array("listId" => 9);
//            var_dump($mailin->get_list($data));

//            $data = array("listId" => 9, "name" => "list_update_test");
//            var_dump($mailin->update_list($data));

//            $data = array("listId" => 9, "folderId" => 8);
//            var_dump($mailin->update_list($data));

//            $data = array("listId" => 9);
//            var_dump($mailin->delete_list($data));

//            // TODO: something wrong with datetime object
//            $date = new \DateTime("1999-12-12 12:00:00.0001");
//            $data = array("listId" => 2, "modifiedSince" => date("1999-12-12 12:00:00.0001"), "limit" => 50, "offset" => 1);
//            var_dump( $date, $mailin->get_list_contacts($data));

//            $data = array("listId" => 6, "emails" => array('mustafa.celik@epigra.com', 'celikmustafa89@gmail.com'));
//            var_dump($mailin->add_contacts_list($data));

//            $data = array("listId" => 6,  "all" => true);
//            var_dump($mailin->delete_contacts_list($data));

//            $data = array("limit" => 50, "offset" => 0, "modifiedSince" => date("1999-12-12 12:00:00.0001"));
//            var_dump($mailin->get_all_contacts($data));

//            $data = array("email" => "caneraa.asa@epigra.com",
//                "attributes" => array("firstname" => "caner", "lastname" => "asa", "sms" => "5064445566"),
//                "emailBlacklisted" => false,
//                "smsBlacklisted" => false,
//                "listIds" => array(2, 6),
//                "updateEnabled" => false);
//            var_dump($mailin->create_contact($data));

//            $data = array("email" => "caner.asa@epigra.com");
//            var_dump($mailin->retrieve_contact_information($data));

//            $data = array("email" => "caner.asa@epigra.com");
//            var_dump($mailin->delete_contact($data));

//            $data = array("email" => "mustafa.celik@epigra.com");
//            var_dump($mailin->get_campaigns_statistics_of_contact($data));

//            $data = array("email" => "caner.asa@epigra.com",
//                "emailBlacklisted" => false,
//                "smsBlacklisted" => false,
//                "listIds" => array(2),
//                "unlinkListIds" => array(6));
//            var_dump($mailin->update_contact($data));

?>
```

 * To explore more, you should visit the [SendinBlue v3 API documentation](https://developers.sendinblue.com/docs).

## API Functions

 * [sms_api](https://developers.sendinblue.com/v3.0/reference#transactional-sms) - SMS functions
 * [contacts_api](https://developers.sendinblue.com/v3.0/reference#contacts-6) - Contact functions
 * [web_hooks_api](https://developers.sendinblue.com/v3.0/reference#webhooks-6) - Webhook functions
 * [smtp_api](https://developers.sendinblue.com/v3.0/reference#smtp) - SMTP functions
 * [email_campaings_api](https://developers.sendinblue.com/v3.0/reference#email-campaigns) - Email Campaign functions 
 * [process_api](https://developers.sendinblue.com/v3.0/reference#process) - Process functions
 * [senders_api](https://developers.sendinblue.com/v3.0/reference#senders-6) - Senders functions 
 * [resellers_api](https://developers.sendinblue.com/v3.0/reference#reseller) - Resellers functions 
 * [account_api](https://developers.sendinblue.com/v3.0/reference#account-6) - Account functions 

####Recommendation:

If you face any error like "Curl error: SSL certificate problem, verify that the CA cert is OK. Details: error:14090086:SSL routines:func(144):reason(134)\n", with our library then by adding the below line of code just before curl_exec() ( line no. 48 ) in mailin.php file, you may no longer face this issue.
```PHP
curl_setopt($ch, CURLOPT_CAINFO, "PATH_TO/cacert.pem");
```
The content of the file is available here: http://curl.haxx.se/ca/cacert.pem
