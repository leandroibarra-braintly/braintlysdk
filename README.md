![Braintly Logo](./resources/assets/docs/logo.png)

---

# PHP SDK for OAuth 2.0 API

## Introduction

Client to access generic APIs with OAuth 2.0. It can be distibuted for platforms to make API requests in PHP.
 
### Requirements

* PHP >= 5.4

### Usage

```
require_once __DIR__ . "/src/Braintly/SDK.php";

$SDK = new Braintly\SDK([
	'url' => 'http://example.com/api', // base API URL
	'apiKey' => 'ABCDE-FGHIJ-KLMNO-PQRST',
]);

// Consuming service examples
$getOrders = $SDK->get('/orders');
$getOrder = $SDK->get('/orders/12');
$postOrder = $SDK->post('/orders', ['total' => 12345]);
$putOrder = $SDK->put('/orders', ['total' => 12345]);
$deleteOrder = $SDK->delete('/orders', 12);

echo json_encode($getOrders);
echo json_encode($getOrder);
echo json_encode($postOrder);
echo json_encode($putOrder);
echo json_encode($deleteOrder);
```
