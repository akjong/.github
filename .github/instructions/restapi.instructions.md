---
description: "Instructions for working with REST APIs"
applyTo: "**"
---

## HTTP Endpoint

In general, HTTP endpoints are defined as the following `<namespace>/<version>/<target>/<action>`, for example: `/constraints/v0/builder/delegate`. Following REST API conventions, `action` is usually a combination of the HTTP method + the action defined in the endpoint.

## API Response Standard

### Success Response

- Get: response data directly. http.status: 200
- Post/Delete/Put: empty response or response data directly. http.status: 200

### Fail Response

- Fail: Client side reason. http.status: 40x

```json
{
  "code": 40x,
  "message": "client request params wrong"
}
```

- Fail: Server side reason. http.status: 50x

```json
{
  "code": 50x,
  "message": "server internal error"
}
```
