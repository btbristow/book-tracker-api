---
layout: single
title: POST customers
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
Use `POST` with the `customers` endpoint to create new customers in the store database, most commonly before creating orders. When testing with JSON Server, you must add one customer at a time.

## Request

To add a new customer, enter a `POST` request similar to the following, with your server and port:

```bash
curl -X POST '{server_url}:{port}/customers' \
--header 'Content-Type: application/json' \
--data '{
    "last_name": "Johnson",
    "first_name": "Emily",
    "telephone": 5551234567,
    "email": "emily.johnson@example.com"
}'
```

## Response

The following sections describe possible responses from the `customers` endpoint when using the `POST` method.

### Success response

A successful `POST` returns `201 Created` with the customer object, including a new `id` property (for example, `"id": "4g540"`).

### Error response

An error contains one of the following HTTP status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [Customers](customers.md)
* [PATCH customers](patch-customers.md)
* [DELETE customers](delete-customers.md)
