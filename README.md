Introduction
============

Merchant e-Solutions APIs implemented in a PHP SDK.

###Requirements
This library requires the cURL extension for PHP.

###Basic Usage
```php
include('mes_sdk.php');
$host = 'https://cert.merchante-solutions.com/mes-api/tridentApi';

$tran = new TpgSale('9410000xxxxx000000xx', 'xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx');
$tran->setAvsRequest('123 Main Street', '55555');
$tran->setRequestField('cvv2', '123');
$tran->setRequestField('invoice_number','123456');
$tran->setTransactionData('4012888812348882', '1212', '1.00');
$tran->setHost($host);
$tran->execute();
```