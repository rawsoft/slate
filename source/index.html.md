---
title: API Reference for FoxMetrics

language_tabs: # must be one of https://git.io/vQNgJ
  - javascript
  #- csharp  

toc_footers:
  - <a href='https://www.foxmetrics.com'>Sign Up for a FREE trial</a>
  - <a href='https://docs.foxmetrics.com'>Documentation & Tutorials</a>

includes:
  - errors

search: true

code_clipboard: true
---

# Introduction

Welcome to the Kittn API! You can use our API to access Kittn API endpoints, which can get information on various cats, kittens, and breeds in our database.

We have language bindings in Shell, Ruby, Python, and JavaScript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](https://github.com/slatedocs/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Authentication

> To authorize, use this code:

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

# HTTPS Requests

```javascript
_fxm.events.push([..., {}]);
```

All HTTPS requests will have a set of predefined parameters as listed below. These parameters may be overwritten if needed otherwise the default or calculated values will be sent with every event.

The last value of the array is reserved for any number of custom attributes.

`GET https://0000000000000.cloudfront.net/f.000000000000000000000000`

> Make sure you replace the 0s with the appropriate URL that is assigned to your account and application.

### Query Parameters

Parameter | Description | Value
--------- | ----------- | -----
nv | New visitor if set to 1, existing visitor if 0
ns | New session if set to 1, existing session if set to 0
ib |
v | The generated visitor id
s | The generated session id
en | The event name | fxm.pages.view
ua | The current browser user agent string
hn | The host name that the user is currently browsing
url | The full URL that is being browsed by the user.
ref | The complete referring URL
pn | The name of the page
pt | The title of the page
sr | The screen resolution in the format (width X height)
bw | The browser width
bh | The browser height
tzo | The time zone offset for the current device
tz | The time zone for the current device
tzn | The name of the time zone for the current device
lng | The language that is currently set on the device
ce | Boolean indicator if cookie is enabled.
im | Set to 1 if its a mobile device or 0 if it isn't
tech_cd |
tech_pd |

<aside class="notice">
Ensure you use your assigned URL or replace the 0s above with your specific <code>pipeline</code> and <code>application</code> identifiers.
</aside>


# System Events



## Form View

```javascript
_fxm.events.push(['_fxm.form.view','a[_fn]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

This call sends a form view event.

### Parameters

Parameter | Description
--------- | -----------
_fn | The name of the form







## Form Submit

```javascript
_fxm.events.push(['_fxm.form.submit','a[_fn]', 'a[_fdur]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

This call sends a form submit event.

### URL Parameters

Parameter | Description
--------- | -----------
_fn | The name of the form
_fdur | The time it took to fill out and submit the form in secs.









## Form Field Change
```javascript
_fxm.events.push(['_fxm.form.fieldchange','a[_fn]', 'a[_flt]', 'a[_fln]', 'a[_flv]', 'a[_fldur]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

This call sends a data when the user changes the value of a field

### URL Parameters

Parameter | Description
--------- | -----------
_fn | The name of the form
_flt | The field type
_fln | The field name
_flv | The field value
_fldur | The time it took to change the field in seconds









## Form Field Error
```javascript
_fxm.events.push(['_fxm.form.fielderror','a[_fn]', 'a[_flt]', 'a[_fln]', 'a[_flv]', 'a[_msg]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

This call error messages at the field level

### URL Parameters

Parameter | Description
--------- | -----------
_fn | The name of the form
_flt | The field type
_fln | The field name
_flv | The field value
_msg | the error message






## Exit
```javascript
_fxm.events.push(['_fxm.pages.exit','a[_id]', 'a[_href]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

When a visitor exits the local page towards a new destination page outside of the site.

### URL Parameters

Parameter | Description
--------- | -----------
_id | The element id of the element that they clicked on
_href | The full destination URL









## Download
```javascript
_fxm.events.push(['_fxm.pages.download','a[_id]', 'a[_href]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

When a visitor downloads a file

### URL Parameters

Parameter | Description
--------- | -----------
_id | The element id of the element that they clicked on to initiate the download
_href | The full URL of the file that was downloaded








## Search
```javascript
_fxm.events.push(['_fxm.pages.search','a[_kw]', 'a[_rc]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

When a visitor performs a search

### URL Parameters

Parameter | Description
--------- | -----------
_kw | The keywords that was used in the search
_rc | The total number of items returned





## Article View
```javascript
_fxm.events.push(['_fxm.articles.view','a[_at]', 'a[_tp]', 'a[_au]', 'a[_pd]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

When a visitor views an article such as a blog post

### URL Parameters

Parameter | Description
--------- | -----------
_at | The title of the article
_tp | The topic of the article
_au | The name of the author of the article
_pd | The published date of the article in ISO8061 format














## Page View

```javascript
_fxm.events.push(['_fxm.pages.view', 'pt', 'pn', 'pgn', 'url', 'ref', {}]);
```

> The above command returns JSON structured like this:

```json
{

}
```

This endpoint retrieves all kittens.

### HTTP Request



<aside class="success">
Remember — we will automatically collect page related values of you don't specify any such as page title
</aside>









## Product View
```javascript
_fxm.events.push(['_fxm.ecommerce.productview','a[_pid]', 'a[_pn]', 'a[_pc]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

When a visitor views a product

### URL Parameters

Parameter | Description
--------- | -----------
_pid | The ID of the product
_pn | The name of the product
_pc | The category of the product, only specify its main or top level category









## Product Review
```javascript
_fxm.events.push(['_fxm.ecommerce.productreview','a[_pid]', 'a[_pn]', 'a[_pc]', 'a[_pr]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

When a visitor reviews a product

### URL Parameters

Parameter | Description
--------- | -----------
_pid | The ID of the product
_pn | The name of the product
_pc | The category of the product, only specify its main or top level category
_pr | The rating that the user specified such as 4 to represent 4/5 stars










## Visitor Profile
```javascript
_fxm.events.push(['_fxm.visitor.profile','p[id]', 'p[fname]', 'p[lname]', 'p[email]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

Update the current visitor profile

### URL Parameters

Parameter | Description
--------- | -----------
id | The unique id such as customer id for this visitor
fname | The first name of the visitor
lname | The last name of the visitor
email | The email address of the visitor








## Error
```javascript
_fxm.events.push(['_fxm.pages.error','a[_msg]', 'a[_code]', 'a[_cat]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

When a visitor experiences an error on your application

### URL Parameters

Parameter | Description
--------- | -----------
_msg | The error message
_code | The error code
_cat | The category of the error if applicable








## Add Cart Item
```javascript
_fxm.events.push(['_fxm.ecommerce.addcartitem','a[_pid]', 'a[_pn]', 'a[_pc]', 'a[_qty]','a[_pr]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

When a visitor adds an item to their cart

### URL Parameters

Parameter | Description
--------- | -----------
_pid | The ID of the product
_pn | The name of the product
_pc | The category of the product, only specify its main or top level category
_qty | The total quantity that was added to cart
_pr | The rating that the user specified such as 4 to represent 4/5 stars








## Remove Cart Item
```javascript
_fxm.events.push(['_fxm.ecommerce.removecartitem','a[_pid]', 'a[_pn]', 'a[_pc]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

When a visitor removes an item to their cart

### URL Parameters

Parameter | Description
--------- | -----------
_pid | The ID of the product
_pn | The name of the product
_pc | The category of the product, only specify its main or top level category







## Purchase Item
```javascript
_fxm.events.push(['_fxm.ecommerce.purchaseitem','a[_pid]', 'a[_pn]', 'a[_pc]', 'a[_qty]','a[_pr]', 'a[_oid]', 'a[_oln]', 'a[_tax]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

When a visitor purchases an item, this should be called for every item in addition to the _fxm.ecommerce.order call

### URL Parameters

Parameter | Description
--------- | -----------
_pid | The ID of the product
_pn | The name of the product
_pc | The category of the product, only specify its main or top level category
_qty | The total quantity that was added to cart
_pr | The rating that the user specified such as 4 to represent 4/5 stars
_oid | The order or transaction id
_oln | The order line number
_tax | The total tax for this specific item








## Order
```javascript
_fxm.events.push(['_fxm.ecommerce.order','a[_oid]', 'a[_st]', 'a[_sht]', 'a[_tt]', 'a[_bc]', 'a[_bs]', 'a[_bz]', 'a[_qty]']);
```

> The above command returns JSON structured like this:

```json
{

}
```

When a visitor places an order. This should be called in addition to _fxm.ecommerce.purchaseitem for each item.

### URL Parameters

Parameter | Description
--------- | -----------
_oid | The unique order id for this transaction
_st | The sub total
_sht | The shipping total
_tt | The tax total
_bc | The billing city
_bs | The billing state/provine
_bz | The billing zipcode/postal code
_qty | The total number of unique items







## Email *
## Onsite Ad
## Poll
## Survey
## Video
## Visit Profile

## Widgets



# Application Events


## Backgrounded
## Crashed
## Destroyed
## Installed
## Opened
## Paused
## Resumed
## Screen View
## Started
## Stopped
## Un-Installed
## Updated
