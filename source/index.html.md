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

All HTTPS requests will have a set of predefined parameters as listed below. These parameters may be overwritten if needed otherwise the default or calculated values will be sent with every event.

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
en | | fxm.pages.view
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
_fxm.events.push(['_fxm.form.view',{}]);
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


### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Form Submit

```javascript
_fxm.events.push(['_fxm.form.submit',{}]);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

## Add Cart Item
## Article View
## Download
## Email *
## Error
## Exit
## Form Field Change
## Form Field Error
## Onsite Ad
## Order

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
Remember — a happy kitten is an authenticated kitten!
</aside>

## Poll
## Product Review
## Product View
## Purchase Item
## Remove Cart Item
## Search
## Survey
## Video
## Visit Profile
## Visitor Profile
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
