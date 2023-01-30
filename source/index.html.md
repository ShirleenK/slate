---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - http
  - php
  - javascript

toc_footers:

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Documentation for the Invoice Review API
---

# Introduction

Welcome to the Invoice Review API.

# Authentication

> To authorize:

```php
# Add the route
```
```http
https://{{url}}{{linkid:}}
```

> Make sure to replace with your API key.

Invoice Review uses API keys to allow access to the API.

Invoice Review expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: API-Key`

<aside class="notice">
You must replace <code>API-Key</code> with your personal API key.
</aside>

# Invoice Review

## GET Invoice Review

```php
# Add the route.
```
```http
https://{{url}}{{linkid:}}
```

> The above http request returns JSON structured like this:

```json
{
  "type": "Purchase Invoice",
  "date": "26/01/2023",
  "dueDate": "26/02/2023",
  "budgetId": "",
  "addedById": "",
  "departmentId": null,
  "description": "",
  "invNo": "INV#1000",
  "currency": "EUR",
  "lines": [
    {
      "categoryId": "",
      "description": "",
      "showCode": "APA 2",
      "net": 20.00,
      "VAT": 0.00,
      "total": 20.00
    },
  ]
}

```

This endpoint retrieves a specific Invoice Review.

### HTTP Request

`GET https://{{url}}{{linkid:}}`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Invoice Review to retrieve

<aside class="notice">
The <code>linkId</code> is the main Id used to retrieve the data.
</aside>

## PATCH Invoice Review

```php
# Add the route.
```

```http
  https://{{url}}{{linkid:}}
```

> The above http request returns JSON structured like this:

```json
{
  "type": "Purchase Invoice",
  "date": "26/01/2023",
  "dueDate": "26/02/2023",
  "budgetId": "",
  "addedById": "",
  "departmentId": null,
  "description": "",
  "invNo": "INV#1000",
  "currency": "EUR",
  "lines": [
    {
      "categoryId": "",
      "description": "",
      "showCode": "APA 2",
      "net": 20.00,
      "VAT": 0.00,
      "total": 20.00
    },
  ]
}
```

This endpoint edit a specific Invoice Review.

### HTTP Request

`PATCH https://{{url}}{{linkid:}}`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Invoice Review to edit

## GET Comment

```php
# Add the route.
```

```http
  https://{{url}}{{linkid:}}
```

> The above http request returns JSON structured like this:

```json
{
  "count": 1,
  "data": [
    {
      "addedById": "",
      "dateTime": "",
      "comment": "Some comment will be displayed here"
    }
  ]
}

```

This endpoint edit a specific Comment on a Invoice Review.

### HTTP Request

`PATCH https://{{url}}{{linkid:}}`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Comment to get
ID | The Id of the comments to retrieve

## GET File Uploads

```php
# Add the route.
```

```http
  https://{{url}}{{linkid:}}
```

> The above http request returns JSON structured like this:

```json
{
  "count": 3,
  "files": [
    "1st_image.png",
    "2nd_image.jpg",
    "3rd_document.pdf"
  ]
}

```

This endpoint get all the File Uploads on a Invoice Review.

### HTTP Request

`GET https://{{url}}{{linkid:}}`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the images to get
ID | The ID of the images to retrieve.

## GET Beneficiary

```php
# Add the route.
```
```http
https://{{url}}{{linkid:}}
```

> The above http request returns JSON structured like this:

```json
{
  "supplierid": "813cd784-fd65-49f6-b7ff-ab52f63f18be",
  "suppliername": "Supplier with a very long name to test the input width restriction",
  "beneficiaries": {
      "providers": {
          "813cd784-fd65-49f6-b7ff-ab52f63f18be": {
              "beneficiary_details": {
                  "Currency": "EUR",
                  "AccountIdentifier": "MC5814607007647022122585228",
                  "BankIdentifier_1": "CCBPMCM1",
                  "AddressLine1": "LE MONTAIGNE BUR N1 A1 1A2 BLOCA",
                  "FirstName": "ASM ANTEXIS",
                  "LastName": " ",
                  "CountryCode": "MC",
                  "AddressLine2": "2 AVENUE DE LA MADONE 98000 MONACO"
              },
              "payment_methods": {
                  "SEPA Payment": "2"
              },
              "addedby": "2e96abc8-0851-7f62-6f68-5e3c279747d7",
              "approved": true
          }
      }
  },
  "currency": "AUD",
  "contactname": null,
  "contacttitle": null,
  "phone": null,
  "mobile": null,
  "email": null,
  "website": null,
  "address": null,
  "baname": null,
  "bano": null,
  "sortcode": null,
  "bic": null,
  "iban": null,
  "vatcountry": null,
  "vatnumber": null,
  "vatrate": "0.00",
  "reciteration": "1"
}


```

This endpoint retrieves a the beneficiary for an Invoice Review.

### HTTP Request

`GET https://{{url}}{{linkid:}}`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Invoice Review to retrieve.
ID | The ID of the beneficiary to retrieve.


<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>


