---
layout: single
title: DELETE customers
toc: true
toc_sticky: true
sidebar:
  nav: "docs"
---
Use `DELETE` with the `customers` endpoint to remove customers from a store database. When you delete customers, you must also [delete their orders](delete-orders.md).

## Request

To `DELETE` a customer, enter `curl -X DELETE http://{server_url}:{port}/customer/{id}` with your server and port and a valid customer `id`.

## Response

The following sections describe possible responses from the `customers` endpoint when using the `DELETE` method.

### Success response

A successful `DELETE` returns `200 OK` with the deleted customer object.

### Error response

An error contains one of the following HTTP status codes.

| Status Code             | Description                                       |
|-------------------------|---------------------------------------------------|
| 404 Not Found           | The server could not find the requested resource. |
| 500 Service Unavailable | The server could not complete the request.        |
| ECONNREFUSED            | The service is unavailable.                      |

## Related Topics

* [Customers](customers.md)
* [POST customers](post-customers.md)
* [PATCH customers](patch-customers.md)
