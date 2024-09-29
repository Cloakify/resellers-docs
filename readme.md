# Introduction

These REST APIs are provided for resellers who are registered in cloakify.

## Use Cases

You can get all plans , get your customers and request new subscriptions.

## Authorization

To authenticate an API request, you should provide your API key in the `resellerApiKey` header.


| Parameter | Type | Description                |
| :--- | :--- |:---------------------------|
| `resellerApiKey` | `string` | **Required**. Your API key |


### Endpoints

Base ulrs are :
`https://p1.silkroadway.cloud/api/v1` and `https://panel.silkways.online/api/v1`

| Method   | URL                                                               | Description                                                                                 |
| -------- |-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| `GET`    | `/reseller/plans`                                                 | Retrieve all available plans.                                                               |
| `POST`   | `/reseller/order`                                                 | Create a new subscription.                                                                  |
| `GET`    | `/reseller/links`                                                 | Retrieve all active subscriptions.                                                          |

## Responses

Many API endpoints return the JSON representation of the resources created or edited. However, if an invalid request is
submitted, or some other error occurs, It returns a JSON response in the following format:

```javascript
{
    "data": array
    "message": string, 
}
```

The `message` attribute contains a message commonly used to indicate errors or,
success that the resource was properly stored.

The `data` attribute contains any other metadata associated with the response. This will be an array containing
JSON data.

## Status Codes

Cloakify returns the following status codes in its API:

| Status Code | Description |
| :--- | :--- |
| 200 | `OK` |
| 400 | `BAD REQUEST` |
| 404 | `NOT FOUND` |
| 500 | `INTERNAL SERVER ERROR` |

## Payment System and Subscription Policy

Payments are processed on a weekly basis. You can subscribe to this API with no limits on the number of subscriptions you obtain.
<br><br>
At the end of each week, a settlement notice will be sent to the sales representative. If payment is not made within 3 days of receiving this notice, the links created under this account will be locked. If the settlement remains unpaid for 7 days, the account will be permanently suspended.
<br><br>
Price is calculated based on the traffic you consume, for example if you get 3x 20GB subscription you'll have to pay for 60GB of traffic usage.
<br><br>
Current Price For Each GB: 0.033$
<br><br>
Payment Method : TRX
<br><br>
Wallet Address: TPebfsG6zM4FodyCbgiEiXrZ2diVHWmLFt

## Postman Collection

You can find the postman collection in this repository by the name `Cloakify-resellers.postman_collection.json`
