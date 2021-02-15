# ipaytotal-directAPI

## How to integrate iPayTotal Payment API

<div data-label="Tutorial Detail" class="df-example demo-table">
<p>We have provided an easy payment API integration, you can use this to integrate with any platform. Please follow the simple steps to integrate our payment API in PHP platform.</p>

<h3>Direct Payment API</h3>

<h4>Request Parameter</h4>

<table cellspacing="0" class="table table-hover table-light" style="background-color: rgba(255, 255, 255, 0.14); border-collapse: collapse; box-sizing: border-box; font-family: Roboto, sans-serif; font-size: 15px; font-style: normal; font-variant-caps: normal; font-variant-ligatures: normal; font-weight: 400; letter-spacing: 1px; margin-bottom: 0px; orphans: 2; text-align: left; text-decoration-color: initial; text-decoration-style: initial; text-indent: 0px; text-transform: none; white-space: normal; widows: 2; width: 1026px; word-spacing: 0px;">
	<thead>
		<tr>
			<th style="text-align: inherit; vertical-align: bottom; white-space: nowrap;">PARAMTERS</th>
			<th style="text-align: inherit; vertical-align: bottom; white-space: nowrap;">REQUIRED</th>
			<th style="text-align: inherit; vertical-align: bottom; white-space: nowrap;">DATA TYPE</th>
			<th style="text-align: inherit; vertical-align: bottom; white-space: nowrap;">DESCRIPTION</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">api_key</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">API key from iPaytotal account</td>
		</tr>
		<tr>
			<td style="vertical-align:top; white-space:nowrap">method</td>
			<td style="vertical-align:top; white-space:nowrap">N</td>
			<td style="vertical-align:top; white-space:nowrap">String</td>
			<td style="vertical-align:top; white-space:nowrap">pass here your payment method.<br />
			possible value is = (unipay, visa-mc, crypto)<br />
			unipay (for unionpay card),<br />
			visa-mc (for visa, master, amex, jcb, discover),<br />
			crypto (for crypto currency)</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">first_name</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">First Name of user</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">last_name</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">Last Name of user</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">address</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">Address of user</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">country</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">2 letter Country, eg US</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">state</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">State Name, 2 letter for US states, eg CA</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">city</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">City name</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">zip</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">Zip Code</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">ip_address</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">IP address of user device, eg 94.104.7.296</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">birth_date</td>
			<td style="vertical-align: top; white-space: nowrap;">N</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">Birth date of user</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">email</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">Valid Email address of user</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">phone_no</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">Phone number (Note : Must be added with the country code , e.g +447777777777 ; Space not allowed.)</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">card_type</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">Integer</td>
			<td style="vertical-align: top; white-space: nowrap;">Valid Following Card Type.<br>
			1 - For Amex&nbsp;<br>
			2 - For Visa&nbsp;<br>
			3 - For Mastercard&nbsp;<br>
			4 - For Discover</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">amount</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">Decimal</td>
			<td style="vertical-align: top; white-space: nowrap;">Amount Value</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">currency</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">3 Digit format, eg USD</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">response_url</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">Merchant site GET URL where we redirect if &nbsp;from 3DS complete</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">sulte_apt_no</td>
			<td style="vertical-align: top; white-space: nowrap;">N</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">Order number of Merchant Transaction</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">card_no</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">Integer</td>
			<td style="vertical-align: top; white-space: nowrap;">Credit Card number</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">ccExpiryMonth</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">Integer</td>
			<td style="vertical-align: top; white-space: nowrap;">Credit card 2 digit expiry month, E.g. 04</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">ccExpiryYear</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">Integer</td>
			<td style="vertical-align: top; white-space: nowrap;">Credit card 4 digit expiry Year, E.g. 2022</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">cvvNumber</td>
			<td style="vertical-align: top; white-space: nowrap;">Y</td>
			<td style="vertical-align: top; white-space: nowrap;">Integer</td>
			<td style="vertical-align: top; white-space: nowrap;">Credit card CVV number</td>
		</tr>
		<tr>
			<td style="vertical-align: top; white-space: nowrap;">webhook_url</td>
			<td style="vertical-align: top; white-space: nowrap;">N</td>
			<td style="vertical-align: top; white-space: nowrap;">String</td>
			<td style="vertical-align: top; white-space: nowrap;">Merchant site POST URL where we send webhook notification</td>
		</tr>
	</tbody>
</table>

<p>&nbsp;</p>

<p><span style="font-size: 16px;"><strong>Request URL:</strong> <span style="color: rgb(117, 105, 179);">https://ipaytotal.solutions/api/transaction</span></span></p>

<p><span style="font-size: 16px;"><strong>Request type:</strong> POST</span></p>

<p>&nbsp;</p>

<p><span style="font-size: 16px;"><strong>Test transaction&nbsp;URL:</strong> <span style="color: rgb(117, 105, 179);">https://ipaytotal.solutions/api/test/transaction</span></span></p>

<p><span style="font-size: 16px;"><strong>Direct API Testing card data:</strong></span></p>

<pre>card_no : 4242 4242 4242 4242
ccExpiryMonth : 00
ccExpiryYear : 2021
cvvNumber : 123</pre>

<p><span style="font-size: 16px;"><strong>Direct API 3D secure Testing card data:</strong></span></p>

<pre>card_no : 4000 0000 0000 0077
ccExpiryMonth : 02
ccExpiryYear : 2021
cvvNumber : 123
</pre>

<h4>API Call Example</h4>

<pre><span style="color: rgb(251, 165, 64);">// You can call our API following curl post example
$url = "https://ipaytotal.solutions/api/transaction";
$key = "Your API Key";
// Fill with real customer info
$data = [
    'api_key' =&gt; $key,
    'first_name' =&gt; 'First Name',
    'last_name' =&gt; 'Last Name',
    'address' =&gt; 'Address',
    'sulte_apt_no' =&gt; 'ORDER-78544646461235',
    'country' =&gt; 'US',
    'state' =&gt; 'NY', // if your country US then use only 2 letter state code.
    'city' =&gt; 'New York',
    'zip' =&gt; '38564',
    'ip_address' =&gt; '192.168.168.4',
    'birth_date' =&gt; '06/12/1990',
    'email' =&gt; 'test@gmail.com',
    'phone_no' =&gt; '+91999999999',
    'card_type' =&gt; '2', // See your card type in list
    'amount' =&gt; '10.00',
    'currency' =&gt; 'USD',
    'card_no' =&gt; '4242424242424242',
    'ccExpiryMonth' =&gt; '02',
    'ccExpiryYear' =&gt; '2020',
    'cvvNumber' =&gt; '123',
    'shipping_first_name' =&gt; 'First Name',
    'shipping_last_name' =&gt; 'Last Name',
    'shipping_address' =&gt; 'Address',
    'shipping_country' =&gt; 'US',
    'shipping_state' =&gt; 'NY',
    'shipping_city' =&gt; 'New York',
    'shipping_zip' =&gt; '35656',
    'shipping_email' =&gt; 'test@gmail.com',
    'shipping_phone_no' =&gt; '+91999999999',</span>
    <span style="color: rgb(243, 156, 18);">'response_url' =&gt; 'https://yourdomain.com/callback.php',</span>
<span style="color: rgb(243, 156, 18);">    'webhook_url' =&gt; 'https://yourdomain.com/notification.php',
</span><span style="color: rgb(251, 165, 64);">];

$curl = curl_init();
curl_setopt($curl, CURLOPT_URL, $url);
curl_setopt($curl, CURLOPT_POST, 1);
curl_setopt($curl, CURLOPT_POSTFIELDS, json_encode($data));
curl_setopt($curl, CURLOPT_RETURNTRANSFER, 1);
curl_setopt($curl, CURLOPT_HTTPHEADER,[
    'Content-Type: application/json'
]);
$response = curl_exec($curl);
curl_close($curl);

$responseData = json_decode($response);

print_r($responseData);

</span></pre>

<h3>Response</h3>

<p>After a successful CURL request, the response will be sent in JSON format.</p>

<h4>Validation Errors</h4>

<p>If in case of validation errors in request, response will be like:</p>

<pre><span style="color: rgb(245, 54, 92);">{
    "status": "fail",
&nbsp;   "message": "Some parameteres are missing or invalid request data.",
    "errors": {
        "first_name": [
            "The first name field is required."
        ]
        .......
        // Other validation error
    }
}  </span> 
</pre>

<h5>Mainly there are 3 types of response with the following Parameter:</h5>

<ol>
	<li>
	<h5>“status”:"fail” : &nbsp;Transaction is declined.</h5>
	</li>
	<li>
	<h5>“status”:"success” : Transaction is success.</h5>
	</li>
	<li>
	<h5>“status”:"3d_redirect” : 3D secure redirection is required to complete the transaction</h5>
	</li>
</ol>

<h4>&nbsp;</h4>

<h4>Success or Declined</h4>

<p>If response contains &nbsp;“status”:"fail” or &nbsp; “status”:"success” it means transaction is complete and it doesn’t need to redirect to 3DS URL.</p>

<h5>This is successful transaction response</h5>

<pre><span style="color: rgb(2, 186, 90);">{
    "status": "success",
    "message": "Your Transaction was processed successfully!!",
    "order_id" : "Unique order no."
} </span>       
</pre>

<h5>This is the declined transaction response</h5>

<pre><span style="color: rgb(231, 76, 60);">{
    "status": "failed",
    "message": "Card provided has expired",
    "order_id" : "Unique order no."
}</span></pre>

<h3>WEBHOOKS</h3>

<p>Webhooks events are transaction callbacks that sends notifications of transaction to the merchant server. If you want to receive webhooks, then send "webhook_url" parameter with initial request(See above request example).</p>

<h3>WEBHOOK EXAMPLE</h3>

<p>Here are the example of webhook notification request:</p>

<pre style="text-align: left;"><span style="color: rgb(243, 156, 18);">{
    "order_id": "2020119869065794026",
    "sulte_apt_no": "ODR465456",
    "transaction_status": "success",
    "reason": "Your transaction processed successfully",
    "currency": "USD",
    "amount": "10",
    "email": "testemail@gmail.com",
    "test": true,
    "transaction_date": "2020-06-10 10:21:55"
}</span></pre>

<p style="text-align: left;">Here are the simple explanation of each parameter:</p>

<ol>
	<li>order_id : Transaction reference number of ipaytotal system.</li>
	<li>sulte_apt_no: Merchant transaction reference.</li>
	<li>transaction_status: "success" / "fail".</li>
	<li>reason: Response from the bank about transaction status.</li>
	<li>currency: Currency of the transaction.</li>
	<li>amount: Amount of the transaction.</li>
	<li>email: Email of the transaction.</li>
	<li>test: true / false. If transaction done in test mode, then value will be true.</li>
	<li>transaction_date: Date of the transaction.</li>
</ol>

<h4 style="text-align: left;">3D secure Redirect</h4>

<p>If the response returns “status”:"3d_redirect” need to redirect the &nbsp;“redirect_3ds_url”</p>

<h5>3D secure Json Response type :</h5>

<pre><span style="color: rgb(245, 54, 92);">{
    "status": "3d_redirect",
    “redirect_3ds_url”: "https://ipaytotal.solutions/redirect?hash=gVRC9OjvYehEbiTAS7RXoxC7L1566046455”,
&nbsp; &nbsp; "api_key": "sugQdpk3gwNi9x63MRAFLgkMJ4nyil88ZYMyjqTSE3FIo8Lghfi",
&nbsp; &nbsp; "sulte_apt_no": null
}</span>  
</pre>

<p>&nbsp;</p>

<h3>Response After 3DS</h3>

<h5>After 3D secure is completed, the user will be redirected to merchant website.</h5>

<p>If transaction will be successful, the user will redirect to ”response_url” with response in query string similar to the one below:</p>

<p><span style="color: rgb(155, 89, 182);">https://ipaytotal.solutions/response?&nbsp; &nbsp; status=success&amp;message=Your%20transaction%20was%20success&amp;order_id=20190000458521&amp;sulte_apt_no=456789521365</span></p>

<p><br>
If the transaction fails, the user will be redirected to &nbsp;“response_url” with response in query string as follows:</p>

<p><span style="color: rgb(155, 89, 182);">https://ipaytotal.solutions/response?status=fail&amp;message=Activity%20limit%20exceeded.&amp;order_id=20190000458521&amp;sulte_apt_no=456789521365</span></p>

<h3><span style="color: rgb(0, 0, 0);">NOTE:</span></h3>

<p><span style="color: rgb(0, 0, 0);">After successful redirect back, create new CURL request and get transaction status:</span></p>

<p><span style="color: rgb(155, 89, 182);">https://ipaytotal.solutions/tutorials/ipaytotal-get-transaction-details-api</span></p>
</div>

#### © Copyright 2020 iPayTotal Ltd.  

