
<div align="center">

# THE SLIIPS PROJECT IS CURRENTLY DORMANT, THIS REPOSITORY IS NOT CURRENTLY BEING MAINTAINED.

</div>

---

Sliips API
==================

# THIS DOCUMENTATION IS OUT OF DATE!

Welcome to the Sliips UI API! If you're looking for the API documentation, this is the right place!

Authentication
--------------

Various parts of the API require authenticated access. This is managed by [JSON Web Tokens](https://jwt.io/) which are presented to the server as **Authorization Headers.**

We do not currently provide a non user API - and infact block all CORS requests to our user authentication endpoint.

Read the [authentication guide](https://github.com/iamacup/sliips-api-docs/blob/master/sections/authentication.md) for details of the various authentication end points.

We have not yet developed the mass-market / company endpoint and so only provide an individual user endpoint at this time.

JSON only
---------

We use JSON for all API data. The style is no root element and camelcase for object keys. This means that you should send the `Content-Type` header `Content-Type: application/json;` when you're sending data to the API, and the API always responds with JSON.


Response format
---------------

The response is always in the following format assuming there has not been any fundemental backend error (which will usually be returned as a non-successful response status):

```bash
{
    "generalStatus": <String>"success" | "error",
    "payload": <Any>,
    "authStatus": <String>"yes" | "no" | "error" | "unknown"
}
```

With the optional parameter of

```bash
{
    "statusCode": <String>
}
```

Rate limiting
-------------

We do not currently rate limit the API.

API endpoints
-------------
<!-- START API ENDPOINTS -->

- [Authentication](https://github.com/iamacup/sliips-api-docs/blob/master/sections/authentication.md)

<!-- END API ENDPOINTS -->


Conduct
-------

Please note that this project is released with a [Contributor Code of Conduct](https://github.com/iamacup/sliips-api-docs/blob/master/CONDUCT.md). By participating in discussions about the Sliips API, you agree to abide by these terms.

License
-------

These API docs are licensed under [Creative Commons (CC BY-SA 4.0)](http://creativecommons.org/licenses/by-sa/4.0/). Please share, remix, and distribute as you see fit.

---

If you have a specific feature request or find a bug, [please open a GitHub issue](https://github.com/iamacup/sliips-api-docs/issues/new). We encourage you to fork these docs for local reference and happily accept pull requests with improvements.

We would love to talk with anyone that has questions or comments, this is an open project driven by the Sliips values - www.sliips.com/contact-us/.
