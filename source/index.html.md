---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell : terminal
  - javascript : typescript

toc_footers:
  - <a href='https://finance.pi.team'>Sign Up here for more</a>
  - <a href='#'>PiTeam Api Docs</a>

includes:
  - errors

search: true
---

# Introduction

`Welcome to the Pi-TEAM API!`

Pi-TEAM is Free online accounting and invoicing software service for small business.

You can use our API to access Pi.Team API endpoints, which can get information on contacts, invoices, quotations and more in our database.

We have language bindings in terminal, typescript! You can view code examples in the dark area to the right, and can switch the programming language of the examples with the tabs in the top right.

This example API documentation page is created for [PiTeam](https://finance.pi.team).

`Happy coding :):)`

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "https://finance.pi.team/api/authtok"\
  -X POST \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer ACCESS-TOKEN" \
  --data '{JSON.stringify(credentials)}'
```

```javascript
  import { Http, Headers } from '@angular/http';
  import { ENV } from '../../config/environment-dev';
  let headers = new Headers();
  let API_URL = "https://finance.pi.team/api/authtok";
  headers.append('Content-Type', 'application/json');
  headers.append("Authorization","Bearer " + ACCESS-TOKEN;
  this.http.post(API_URL, JSON.stringify(credentials), {headers: headers})
```

> Make sure to replace `Bearer ACCESS-TOKEN` with your API key.

Pi.Team uses API's allow access to the API. You can register a new Pi.Team account key at our [portal](https://finance.pi.team).

Pi.Team expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: Bearer ACCESS-TOKEN`

`Content-Type: application/json`

<aside class="notice">
You must replace <code>Bearer ACCESS-TOKEN</code> with your personal API key.
</aside>

<!--Contacts API docs ends -->

# Contacts

## Get All Contacts

```shell
curl "https://finance.pi.team/api/contact/list"\
  -X GET \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer ACCESS-TOKEN" \
```
```javascript
  import { Http, Headers } from '@angular/http';
  import { ENV } from '../../config/environment-dev';
  let headers = new Headers();
  let API_URL = "https://finance.pi.team/api/contacts/list";
  headers.append('Content-Type', 'application/json');
  headers.append("Authorization","Bearer " + ACCESS-TOKEN;
  this.http.get(ENV.API_URL+'contacts/list', {headers: headers})
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

### Headers

Authorization | Token
------ | -------
Bearer | ACCESS-TOKEN

Content-Type | Description
------------ | -----------
application/json |  response is a JSON object

### HTTP Request

`GET https://finance.pi.team/api/contacts/list`

## Get a specific contact

```shell
curl "https://finance.pi.team/api/contact/<OPEN-ID>"\
  -X GET \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer ACCESS-TOKEN" \
```
```javascript
  import { Http, Headers } from '@angular/http';
  import { ENV } from '../../config/environment-dev';
  let headers = new Headers();
  let API_URL = "https://finance.pi.team/api/contacts";
  headers.append('Content-Type', 'application/json');
  headers.append("Authorization","Bearer " + ACCESS-TOKEN;
  this.http.get(ENV.API_URL+'contacts/<OPEN-ID>', {headers: headers})
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

<!-- <aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside> -->

### Headers

Authorization | Token
------ | -------
Bearer | ACCESS-TOKEN

Content-Type | Description
------------ | -----------
application/json |  response is a JSON object

### HTTP Request

`GET https://finance.pi.team/contacts/<OPEN-ID>`

### URL Parameters

Parameter | Description
--------- | -----------
OPEN ID | The ID of the contact to retrieve

## Create a contact

```shell
curl "https://finance.pi.team/api/contacts"\
  -X POST \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer ACCESS-TOKEN" \
  --data '{"name":"Rubymine","phone":"8130950367","contact1":"8130950367","contact2":"8130950367","email":"aneilwebber@gmail.com","bill_address1":"UB city","bill_address2":"Cuboon Road","bill_city":"Bengaluru","bill_country_id":"IN","bill_postal_code":"560070","bill_state":"Karnataka","fax_no":"3497349574","instructions":"","mobile_no":"","ship_address1":"UB city","ship_address2":"Cuboon Road","ship_city":"Bengaluru","ship_contact":"Rubymine","ship_country_id":"IN","ship_phone":"8130950367","ship_postal_code":"560070","ship_state":"Karnataka","toll_free_no":"","vat_no":"","website":""}'
```

```javascript
{
  import { Http, Headers } from '@angular/http';
  import { ENV } from '../../config/environment-dev';
  let headers = new Headers();
  let API_URL = "https://finance.pi.team/api/contacts";
  headers.append('Content-Type', 'application/json');
  headers.append("Authorization","Bearer " + ACCESS-TOKEN;
  this.http.post(ENV.API_URL, this.contactData, {headers: headers})
}
```

> The above command returns JSON structured like this:

```json
{
  "id": 1,
  "team_id": 1,
  "open_id": 1,
  "name": "Rubymine",
  "email":"aneilwebber@gmail.com",
  "contact1":"8130950367",
  "contact2":"8130950367",
  "currency_id": "840",
  "bill_address1":"UB city",
  "bill_address2":"Cuboon Road",
  "bill_city":"Bengaluru",
  "bill_country_id":"IN",
  "bill_postal_code":"560070",
  "bill_state":"Karnataka",
  "ship_address1":"UB city",
  "ship_address2":"Cuboon Road",
  "ship_city":"Bengaluru",
  "ship_contact":"Rubymine",
  "ship_country_id":"IN",
  "ship_phone":"8130950367",
  "ship_postal_code":"560070",
  "ship_state":"Karnataka",
  "ship_postal_code": null,
  "fax_no": "3497349574",
  "website": "",
  "created_by_id": 41,
  "modified_by_id": 41,
  "created_at": "2017-07-27 08:55:49",
  "updated_at": "2017-07-27 08:55:49",
  "gst_code": null
}
```

This endpoint creates a contact record.

### Headers

Authorization | Token
------ | -------
Bearer | ACCESS-TOKEN

Content-Type | Description
------------ | -----------
application/json |  response is a JSON object

### HTTP Request

`POST https://finance.pi.team/contacts`

### URL Parameters example

Parameter(name) | Type(string)
--------- | -----------
name | "Rubymine"
phone | "8130950367"
contact1 | "8130950367"
contact2 | "8130950367"
email | "aneilwebber@gmail.com"
bill_address1 | "UB city"
bill_address2 |"Cuboon Road"
bill_city | "Bengaluru"
bill_country_id | "IN"
bill_postal_code | "560070"
bill_state | "Karnataka"
ship_address1 | "UB city"
ship_address2 | "Cuboon Road"
ship_city | "Bengaluru"
ship_contact | "Rubymine"
ship_country_id | "IN"
ship_phone | "8130950367"
ship_postal_code | "560070"
ship_state | "Karnataka"

<!--Contacts API docs ends -->



<!-- Invoice API Docs -->

# invoices

## Get All invoices

```shell
curl "https://finance.pi.team/api/invoices"\
  -X GET \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer ACCESS-TOKEN" \
```
```javascript
  import { Http, Headers } from '@angular/http';
  import { ENV } from '../../config/environment-dev';
  let headers = new Headers();
  let API_URL = "https://finance.pi.team/api/invoices/list";
  headers.append('Content-Type', 'application/json');
  headers.append("Authorization","Bearer " + ACCESS-TOKEN;
  this.http.get(ENV.API_URL+'invoices/list', {headers: headers})
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "team_id": 1,
    "open_id": 1,
    "name": "Anil verma",
    "email":"aneilfreelancer@gmail.com",
    "contact1":"123456789",
    "contact2":"123456789",
    "currency_id": "840",
    "payment_terms": 15,
    "bill_address1":"UB city",
    "bill_address2":"Whitfield Road",
    "bill_city":"Bengaluru",
    "bill_country_id":"IN",
    "bill_postal_code":"560070",
    "bill_state":"Karnataka",
    "bill_country_id": null,
    "ship_address1":"UB city",
    "ship_address2":"Nice Road",
    "ship_city":"Bengaluru",
    "ship_contact":"Rubymine",
    "ship_country_id":"IN",
    "ship_phone":"8130950367",
    "ship_postal_code":"560070",
    "ship_state":"Karnataka",
    "fax_no": "3497349574",
    "website": "",
    "balance": "0.00",
    "created_by_id": 41,
    "modified_by_id": 41,
    "created_at": "2017-07-27 08:55:49",
    "updated_at": "2017-07-27 08:55:49"
  },
  {
    "id": 2,
    "team_id": 2,
    "open_id": 2,
    "name": "Rubymine",
    "email":"aneilwebber@gmail.com",
    "contact1":"8130950367",
    "contact2":"8130950367",
    "currency_id": "840",
    "payment_terms": 15,
    "bill_address1":"UB city",
    "bill_address2":"Cuboon Road",
    "bill_city":"Bengaluru",
    "bill_country_id":"IN",
    "bill_postal_code":"560070",
    "bill_state":"Karnataka",
    "bill_country_id": null,
    "ship_address1":"UB city",
    "ship_address2":"Cuboon Road",
    "ship_city":"Bengaluru",
    "ship_contact":"Rubymine",
    "ship_country_id":"IN",
    "ship_phone":"8130950367",
    "ship_postal_code":"560070",
    "ship_state":"Karnataka",
    "fax_no": "3497349574",
    "website": "",
    "balance": "0.00",
    "created_by_id": 41,
    "modified_by_id": 41,
    "created_at": "2017-07-27 08:55:49",
    "updated_at": "2017-07-27 08:55:49"
    }
]
```

This endpoint retrieves all invoices.

### Headers

Authorization | Token
------ | -------
Bearer | ACCESS-TOKEN

Content-Type | Description
------------ | -----------
application/json |  response is a JSON object

### HTTP Request

`GET https://finance.pi.team/api/invoices/list`

<!-- ### Query Parameters -->

<!-- Parameter | Default | Description
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include invoices that have already been adopted.
 -->
<!-- <aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside> -->

## Get a specific invoice

```shell
curl "https://finance.pi.team/api/invoices/<OPEN-ID>"\
  -X GET \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer ACCESS-TOKEN" \
```
```javascript
  import { Http, Headers } from '@angular/http';
  import { ENV } from '../../config/environment-dev';
  let headers = new Headers();
  let API_URL = "https://finance.pi.team/api/invoices";
  headers.append('Content-Type', 'application/json');
  headers.append("Authorization","Bearer " + ACCESS-TOKEN;
  this.http.get(ENV.API_URL+'invoices/<OPEN-ID>', {headers: headers})
```

> The above command returns JSON structured like this:

```json
{
  "id": 627,
  "team_id": 43,
  "open_id": 1,
  "name": "Test Customer",
  "email": "test@avansaber.com",
  "contact1": "Contact One",
  "currency_id": "840",
  "payment_terms": 15,
  "bill_address1": "Line One",
  "bill_address2": "Line Two",
  "bill_city": "City",
  "bill_state": "State",
  "bill_postal_code": "1234",
  "bill_country_id": "IN",
  "ship_country_id": "US",
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
}
```

This endpoint retrieves a specific invoice.

<!-- <aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside> -->

### Headers

Authorization | Token
------ | -------
Bearer | ACCESS-TOKEN

Content-Type | Description
------------ | -----------
application/json |  response is a JSON object

### HTTP Request

`GET https://finance.pi.team/invoices/<OPEN-ID>`

### URL Parameters

Parameter | Description
--------- | -----------
OPEN ID | The ID of the invoice to retrieve

## Create an invoice

```shell
curl "https://finance.pi.team/api/invoices"\
  -X POST \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer ACCESS-TOKEN" \
  --data '{"title":"New invoice","customer_email":"aneilwebber@gmail.com","customer_name":"aneil","ded_items":": [{"item_id":"itemID","name":"item-name","price":"100","qty":"10","total":"1000"}],"due_date":"2017-08-11","items":[{"item_id":"itemID","name":"item-name","price":"100","qty":"10","total":"1000"}]}'
```

```javascript
{
  import { Http, Headers } from '@angular/http';
  import { ENV } from '../../config/environment-dev';
  let headers = new Headers();
  let API_URL = "https://finance.pi.team/api/invoices";
  headers.append('Content-Type', 'application/json');
  headers.append("Authorization","Bearer " + ACCESS-TOKEN;
  this.http.post(ENV.API_URL, this.invoiceData, {headers: headers})
}
```

> The above command returns JSON structured like this:

```json
{ 
  "title":"Invoice#44"
  "amount_paid":"0.00"
  "amount_paid_local":"0.00"
  "balance":"5535.00"
  "balance_local":"5535.00"
  "company_currency_id":"840"
  "contact_id":628
  "created_at":"2017-07-27 11:58:43"
  "created_by_id":41
  "customer_email":"aneilwebber@gmail.com"
  "customer_name":"aneil"
  "debit_gl":1
  "dedTab":Array[1]
  "ded_amount":"600.00"
  "deleted_at":null
  "due_date":"2017-08-11"
  "encrypted_id":"1044346515"
  "inv_items_tab":Array[2]
  "inv_tax_tab":Array[1]
  "open_id":24
  "status_id":1
  "sub_total":"6000.00"
  "summary":"Summery goes here"
  "taxTab":Array[2]
  "tax_amount":"135.00"
  "tax_amount_local":"135.00"
  "tax_rate1":0
  "team_id":43
  "total_amount":"5535.00"
  "total_amount_local":"5535.00"
  "updated_at":"2017-07-27 11:58:43"
}
```

This endpoint creates a invoice record.

### Headers

Authorization | Token
------ | -------
Bearer | ACCESS-TOKEN

Content-Type | Description
------------ | -----------
application/json |  response is a JSON object

### HTTP Request

`POST https://finance.pi.team/invoices`

### URL Parameters example

Parameter(name) | Type(string)
--------- | -----------
title | New invoice
customer_email | aneilwebber@gmail.com
customer_name | aneil
ded_items | [{"item_id":"itemID","name":"item-name","price":"100","qty":"10","total":"1000"}]
due_date | 2017-08-11
items | [{"item_id":"itemID","name":"item-name","price":"100","qty":"10","total":"1000"}]


<!-- Quotation API docs -->

# Quotations

## Get All quotations

```shell
curl "https://finance.pi.team/api/quotations"\
  -X GET \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer ACCESS-TOKEN" \
```
```javascript
  import { Http, Headers } from '@angular/http';
  import { ENV } from '../../config/environment-dev';
  let headers = new Headers();
  let API_URL = "https://finance.pi.team/api/quotations/list";
  headers.append('Content-Type', 'application/json');
  headers.append("Authorization","Bearer " + ACCESS-TOKEN;
  this.http.get(ENV.API_URL+'quotations/list', {headers: headers})
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "team_id": 1,
    "open_id": 1,
    "name": "Anil verma",
    "email":"aneilfreelancer@gmail.com",
    "contact1":"123456789",
    "contact2":"123456789",
    "currency_id": "840",
    "payment_terms": 15,
    "bill_address1":"UB city",
    "bill_address2":"Whitfield Road",
    "bill_city":"Bengaluru",
    "bill_country_id":"IN",
    "bill_postal_code":"560070",
    "bill_state":"Karnataka",
    "bill_country_id": null,
    "ship_address1":"UB city",
    "ship_address2":"Nice Road",
    "ship_city":"Bengaluru",
    "ship_contact":"Rubymine",
    "ship_country_id":"IN",
    "ship_phone":"8130950367",
    "ship_postal_code":"560070",
    "ship_state":"Karnataka",
    "fax_no": "3497349574",
    "website": "",
    "balance": "0.00",
    "created_by_id": 41,
    "modified_by_id": 41,
    "created_at": "2017-07-27 08:55:49",
    "updated_at": "2017-07-27 08:55:49"
  },
  {
    "id": 2,
    "team_id": 2,
    "open_id": 2,
    "name": "Rubymine",
    "email":"aneilwebber@gmail.com",
    "contact1":"8130950367",
    "contact2":"8130950367",
    "currency_id": "840",
    "payment_terms": 15,
    "bill_address1":"UB city",
    "bill_address2":"Cuboon Road",
    "bill_city":"Bengaluru",
    "bill_country_id":"IN",
    "bill_postal_code":"560070",
    "bill_state":"Karnataka",
    "bill_country_id": null,
    "ship_address1":"UB city",
    "ship_address2":"Cuboon Road",
    "ship_city":"Bengaluru",
    "ship_contact":"Rubymine",
    "ship_country_id":"IN",
    "ship_phone":"8130950367",
    "ship_postal_code":"560070",
    "ship_state":"Karnataka",
    "fax_no": "3497349574",
    "website": "",
    "balance": "0.00",
    "created_by_id": 41,
    "modified_by_id": 41,
    "created_at": "2017-07-27 08:55:49",
    "updated_at": "2017-07-27 08:55:49"
    }
]
```

This endpoint retrieves all quotations.

### Headers

Authorization | Token
------ | -------
Bearer | ACCESS-TOKEN

Content-Type | Description
------------ | -----------
application/json |  response is a JSON object

### HTTP Request

`GET https://finance.pi.team/api/quotations/list`

## Get a specific quotation

```shell
curl "https://finance.pi.team/api/quotations/<OPEN-ID>"\
  -X GET \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer ACCESS-TOKEN" \
```
```javascript
  import { Http, Headers } from '@angular/http';
  import { ENV } from '../../config/environment-dev';
  let headers = new Headers();
  let API_URL = "https://finance.pi.team/api/quotations";
  headers.append('Content-Type', 'application/json');
  headers.append("Authorization","Bearer " + ACCESS-TOKEN;
  this.http.get(ENV.API_URL+'quotations/<OPEN-ID>', {headers: headers})
```

> The above command returns JSON structured like this:

```json
{
  "id": 627,
  "team_id": 43,
  "open_id": 1,
  "name": "Test Customer",
  "email": "test@avansaber.com",
  "contact1": "Contact One",
  "currency_id": "840",
  "payment_terms": 15,
  "bill_address1": "Line One",
  "bill_address2": "Line Two",
  "bill_city": "City",
  "bill_state": "State",
  "bill_postal_code": "1234",
  "bill_country_id": "IN",
  "ship_country_id": "US",
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
}
```

This endpoint retrieves a specific quotation.

### Headers

Authorization | Token
------ | -------
Bearer | ACCESS-TOKEN

Content-Type | Description
------------ | -----------
application/json |  response is a JSON object

### HTTP Request

`GET https://finance.pi.team/quotations/<OPEN-ID>`

### URL Parameters

Parameter | Description
--------- | -----------
OPEN ID | The ID of the quotation to retrieve

## Create an quotation

```shell
curl "https://finance.pi.team/api/quotations"\
  -X POST \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer ACCESS-TOKEN" \
  --data '{"title":"New quotation","customer_email":"aneilwebber@gmail.com","customer_name":"aneil","ded_items":": [{"item_id":"itemID","name":"item-name","price":"100","qty":"10","total":"1000"}],"due_date":"2017-08-11","items":[{"item_id":"itemID","name":"item-name","price":"100","qty":"10","total":"1000"}]}'
```

```javascript
{
  import { Http, Headers } from '@angular/http';
  import { ENV } from '../../config/environment-dev';
  let headers = new Headers();
  let API_URL = "https://finance.pi.team/api/quotations";
  headers.append('Content-Type', 'application/json');
  headers.append("Authorization","Bearer " + ACCESS-TOKEN;
  this.http.post(ENV.API_URL, this.quotationData, {headers: headers})
}
```

> The above command returns JSON structured like this:

```json
{ 
  "title":"quotation#44"
  "amount_paid":"0.00"
  "amount_paid_local":"0.00"
  "balance":"5535.00"
  "balance_local":"5535.00"
  "company_currency_id":"840"
  "contact_id":628
  "created_at":"2017-07-27 11:58:43"
  "created_by_id":41
  "customer_email":"aneilwebber@gmail.com"
  "customer_name":"aneil"
  "debit_gl":1
  "dedTab":Array[1]
  "ded_amount":"600.00"
  "deleted_at":null
  "due_date":"2017-08-11"
  "encrypted_id":"1044346515"
  "inv_items_tab":Array[2]
  "inv_tax_tab":Array[1]
  "open_id":24
  "status_id":1
  "sub_total":"6000.00"
  "summary":"Summery goes here"
  "taxTab":Array[2]
  "tax_amount":"135.00"
  "tax_amount_local":"135.00"
  "tax_rate1":0
  "team_id":43
  "total_amount":"5535.00"
  "total_amount_local":"5535.00"
  "updated_at":"2017-07-27 11:58:43"
}
```

This endpoint creates a quotation record.

### Headers

Authorization | Token
------ | -------
Bearer | ACCESS-TOKEN

Content-Type | Description
------------ | -----------
application/json |  response is a JSON object

### HTTP Request

`POST https://finance.pi.team/quotations`

### URL Parameters example

Parameter(name) | Type(string)
--------- | -----------
title | New quotation
customer_email | aneilwebber@gmail.com
customer_name | aneil
ded_items | [{"item_id":"itemID","name":"item-name","price":"100","qty":"10","total":"1000"}]
due_date | 2017-08-11
items | [{"item_id":"itemID","name":"item-name","price":"100","qty":"10","total":"1000"}]

<!-- Quotation API docs ends -->