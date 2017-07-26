---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - terminal
  - postman

toc_footers:
  - <a href='https://finance.pi.team'>Sign Up here for more</a>
  - <a href='#'>PiTeam Api Docs</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Kittn API! You can use our API to access Kittn API endpoints, which can get information on various cats, kittens, and breeds in our database.

We have language bindings in terminal, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](https://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Authentication

> To authorize, use this code:

```terminal
# With terminal, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: access_token"
```

```postman
const kittn = require('kittn');

let api = kittn.authorize('access_token');
```

> Make sure to replace `access_token` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](https://finance.pi.team/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: access_token`

<aside class="notice">
You must replace <code>access_token</code> with your personal API key.
</aside>

<!--Contacts API docs ends -->

# Contacts

## Get All Contacts

```postman
curl "https://finance.pi.team/api/contacts/list"
  -H "Authorization: access_token"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "team_id": 1,
    "open_id": 1,
    "name": "Sanatan Bhardwaj",
    "email": "sanatan0105@gmail.com",
    "image": "/storage/contacts/2092775939.png",
    "phone": "8553533405",
    "contact1": "Sanatan0105@gmail.com",
    "contact2": "",
    "currency_id": "356",
    "payment_terms": 15,
    "bill_address1": "M.v.j. College Of Engineering, Hostel 02",
    "bill_address2": "Ark Serene County, Flat 011- Block 01",
    "bill_city": "Bangaluru",
    "bill_state": "Karnataka",
    "bill_postal_code": "560067",
    "bill_country_id": "91",
    "ship_phone": "",
    "ship_contact": "8553533405",
    "ship_address1": "M.v.j. College Of Engineering, Hostel 02",
    "ship_address2": "Ark Serene County, Flat 011- Block 01",
    "ship_city": "Bangaluru",
    "ship_state": "Karnataka",
    "ship_postal_code": "560067",
    "ship_country_id": "91",
    "instructions": "",
    "account_no": "",
    "id_no": "",
    "vat_no": "1232342",
    "fax_no": "",
    "mobile_no": "8553533405",
    "toll_free_no": "",
    "website": "",
    "balance": "0.00",
    "created_by_id": 41,
    "modified_by_id": 41,
    "created_at": "2017-07-24 18:03:59",
    "updated_at": "2017-07-24 18:03:59",
    "deleted_at": null,
    "emails": null,
    "gst_code": null
  },
  {
    "id": 2,
    "team_id": 2,
    "open_id": 2,
    "name": "Freelance",
    "email": "aneilfreelancer@gmail.com",
    "image": "/storage/contacts/2143150589.png",
    "phone": "8130950367",
    "contact1": "8130950367",
    "contact2": "8130950367",
    "currency_id": "840",
    "payment_terms": 15,
    "bill_address1": "Address",
    "bill_address2": "Address",
    "bill_city": "Bengaluru",
    "bill_state": "Karnataka",
    "bill_postal_code": "560070",
    "bill_country_id": null,
    "ship_phone": "",
    "ship_contact": "",
    "ship_address1": "",
    "ship_address2": "",
    "ship_city": "",
    "ship_state": "",
    "ship_postal_code": "",
    "ship_country_id": null,
    "instructions": "",
    "account_no": "",
    "id_no": "",
    "vat_no": "",
    "fax_no": "",
    "mobile_no": "",
    "toll_free_no": "",
    "website": "",
    "balance": "0.00",
    "created_by_id": 41,
    "modified_by_id": 41,
    "created_at": "2017-07-12 20:20:33",
    "updated_at": "2017-07-12 20:20:34",
    "deleted_at": null,
    "emails": null,
    "gst_code": null
  }
]
```

This endpoint retrieves all contacts.

### HTTP Request

`GET https://finance.pi.team/api/contacts/list`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include contacts that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Contact

```postman
curl "https://finance.pi.team/api/contact/<OPEN-ID>"
  -H "Authorization: access_token"
```

> The above command returns JSON structured like this:

```json
{
  "id": 627,
  "team_id": 43,
  "open_id": 1,
  "name": "Test Customer",
  "email": "test@avansaber.com",
  "image": "/storage/contacts/1558704516.png",
  "phone": null,
  "contact1": "Contact One",
  "contact2": "",
  "currency_id": "840",
  "payment_terms": 15,
  "bill_address1": "Line One",
  "bill_address2": "Line Two",
  "bill_city": "City",
  "bill_state": "State",
  "bill_postal_code": "1234",
  "bill_country_id": "IN",
  "ship_phone": "",
  "ship_contact": "",
  "ship_address1": "",
  "ship_address2": "",
  "ship_city": "",
  "ship_state": "",
  "ship_postal_code": "",
  "ship_country_id": "US",
  "instructions": "",
  "account_no": "",
  "id_no": "",
  "vat_no": "",
  "fax_no": "",
  "mobile_no": "",
  "toll_free_no": "",
  "website": "",
  "balance": "0.00",
  "created_by_id": 41,
  "modified_by_id": 41,
  "created_at": "2017-07-12 19:48:15",
  "updated_at": "2017-07-12 19:48:15",
  "deleted_at": null,
  "emails": [
      {
          "id": ""
      }
  ],
  "gst_code": null
}
```

This endpoint retrieves a specific contact.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET https://finance.pi.team/contacts/<OPEN-ID>`

### URL Parameters

Parameter | Description
--------- | -----------
OPEN ID | The ID of the contact to retrieve

## Download a Inovoice

```terminal
curl "https://finance.pi.team/api/kittens/2"
  -X DELETE
  -H "Authorization: access_token"
```

```postman
require 'kittn'

api = Kittn::APIClient.authorize!('access_token')
api.kittens.delete(2)
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint retrieves a specific kitten.

### HTTP Request

`GET https://finance.pi.team/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

<!--Contacts API docs ends -->



<!-- Invoice API Docs -->

# Invoices

## Get All Invoices

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('access_token')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('access_token')
api.kittens.get()
```

```terminal
curl "https://finance.pi.team/api/kittens"
  -H "Authorization: access_token"
```

```postman
const kittn = require('kittn');

let api = kittn.authorize('access_token');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET https://finance.pi.team/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Invoice

```terminal
curl "https://finance.pi.team/api/kittens/2"
  -H "Authorization: access_token"
```

```postman
const kittn = require('kittn');

let api = kittn.authorize('access_token');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET https://finance.pi.team/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Download a Inovoice

```terminal
curl "https://finance.pi.team/api/kittens/2"
  -X DELETE
  -H "Authorization: access_token"
```

```postman
const kittn = require('kittn');

let api = kittn.authorize('access_token');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint retrieves a specific kitten.

### HTTP Request

`DELETE https://finance.pi.team/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete


<!-- Quotation API docs -->

# Quotations

## Get All Quotations

```terminal
curl "https://finance.pi.team/api/kittens"
  -H "Authorization: access_token"
```

```postman
const kittn = require('kittn');

let api = kittn.authorize('access_token');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET https://finance.pi.team/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Invoice

```terminal
curl "https://finance.pi.team/api/kittens/2"
  -H "Authorization: access_token"
```

```postman
const kittn = require('kittn');

let api = kittn.authorize('access_token');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET https://finance.pi.team/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Download a Inovoice

```terminal
curl "https://finance.pi.team/api/kittens/2"
  -X DELETE
  -H "Authorization: access_token"
```

```postman
const kittn = require('kittn');

let api = kittn.authorize('access_token');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint retrieves a specific kitten.

### HTTP Request

`DELETE https://finance.pi.team/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

<!-- Quotation API docs ends -->