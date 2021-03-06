# OpenAPIClient-php
API Specification for Paella API

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 1.0
- Build package: org.openapitools.codegen.languages.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: api_key
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKey('X-Api-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Api-Key', 'Bearer');

$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_id = 'order_id_example'; // string | Order id
$merchant_payment_request = new \OpenAPI\Client\Model\MerchantPaymentRequest(); // \OpenAPI\Client\Model\MerchantPaymentRequest | 

try {
    $apiInstance->merchantPayment($order_id, $merchant_payment_request);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->merchantPayment: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://paella.test10.ozean12.com/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*OrderApi* | [**merchantPayment**](docs/Api/OrderApi.md#merchantpayment) | **POST** /order/{order_id}/confirm-payment | Merchant payment confirmation
*OrderApi* | [**orderFullCancellation**](docs/Api/OrderApi.md#orderfullcancellation) | **POST** /order/{order_id}/cancel | Order full cancellation
*OrderApi* | [**orderPost**](docs/Api/OrderApi.md#orderpost) | **POST** /order | Create new order
*OrderApi* | [**orderShip**](docs/Api/OrderApi.md#ordership) | **POST** /order/{order_id}/ship | Ship order
*OrderApi* | [**patchOrder**](docs/Api/OrderApi.md#patchorder) | **PATCH** /order/{order_id} | Update order amount / duration
*OrderApi* | [**retrieveOrder**](docs/Api/OrderApi.md#retrieveorder) | **GET** /order/{order_id} | Retrieve order
*WebhookApi* | [**webhooksPost**](docs/Api/WebhookApi.md#webhookspost) | **POST** /webhooks | 


## Documentation For Models

 - [Amount](docs/Model/Amount.md)
 - [BankAccount](docs/Model/BankAccount.md)
 - [CreateNewOrderApi](docs/Model/CreateNewOrderApi.md)
 - [DebtorCompany](docs/Model/DebtorCompany.md)
 - [DebtorCompanyOnOrderCreatedResponse](docs/Model/DebtorCompanyOnOrderCreatedResponse.md)
 - [DebtorPerson](docs/Model/DebtorPerson.md)
 - [DeliveryAddress](docs/Model/DeliveryAddress.md)
 - [ErrorBadRequest](docs/Model/ErrorBadRequest.md)
 - [ErrorBadRequestErrors](docs/Model/ErrorBadRequestErrors.md)
 - [ErrorBlock](docs/Model/ErrorBlock.md)
 - [ErrorUnauthorized](docs/Model/ErrorUnauthorized.md)
 - [Invoice](docs/Model/Invoice.md)
 - [MerchantPaymentRequest](docs/Model/MerchantPaymentRequest.md)
 - [Order](docs/Model/Order.md)
 - [PatchOrder](docs/Model/PatchOrder.md)
 - [ShipOrder](docs/Model/ShipOrder.md)
 - [Webhook](docs/Model/Webhook.md)


## Documentation For Authorization


## api_key

- **Type**: API key
- **API key parameter name**: X-Api-Key
- **Location**: HTTP header


## Author

engineering@billie.io


