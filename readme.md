# Introduction

These REST APIs are provided for resellers who are registered in cloakify.

## Use Cases

You can get all plans , get your customers and request new subscriptions.

## Authorization

To authenticate an API request, you should provide your API key in the `resellerApiKey` header.


| Parameter | Type | Description                |
| :--- | :--- |:---------------------------|
| `resellerApiKey` | `string` | **Required**. Your API key |

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

## Postman Collection

You can find the postman collection in this repository by the name `Cloakify-resellers.postman_collection.json`
