# OpenAPI\Client\WebhookApi

All URIs are relative to *https://paella.test10.ozean12.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**webhooksPost**](WebhookApi.md#webhooksPost) | **POST** /webhooks | 


# **webhooksPost**
> object webhooksPost($callback_url)



Subscribes to order notifications

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new OpenAPI\Client\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$callback_url = https://billies-server.com; // string | Url where webhook data will be sent

try {
    $result = $apiInstance->webhooksPost($callback_url);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->webhooksPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **callback_url** | **string**| Url where webhook data will be sent |

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

