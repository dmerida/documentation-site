{
"title": "Quote",
"pagetitle": "Quote",
"description": "How to Quote an option from Search",
"icon": "fa-exchange",
"weight": 2,
"alwaysopen": false,
"default_ak": "8626cf56-e364-4fd1-4fe0-311e23ac6355",
"default_user": "",
"gists": [
    {
        "n":"1 Room",
        "g":"54d5fa6313c9eb80f916b8b1c63298c7",
        "o":["graphiql"],
        "u":"tgx-bot",
        "ak":"8626cf56-e364-4fd1-4fe0-311e23ac6355"
    }
        ]
}

Quote is an operation used to assess and valuate the rate before the actual booking. It returns the information as the Search response for a hotel rate with up-to-date price, along with additional information regarding the rate: rate breakdown and cancellation policies.

## Advanced criteria
There are different parameters that can be set up in the request - The below ones are mandatory:

- **optionRefId**: Identifier of the option chosen in Search
- **language**: Language to be used in the request

In the Query Variables, you should modify the optionRefId with the option id value returned in the search response and send the query.

## How to request 
Here you can find 2 examples of how to Quote a Search option, one for 1 room and the other one for multi-room. </br>

{{% graphiql-tabs %}}

54d5fa6313c9eb80f916b8b1c63298c7
Please, bear in mind that you should place on _optionRefId_ field the value from the **_id_** field of the option you want to Quote from Search.
/54d5fa6313c9eb80f916b8b1c63298c7

{{% /graphiql-tabs %}}

{{< graphiql-styles >}}
{{% graphiql-script-tabs %}}

## Important

{{% alert theme="danger" %}}
Please, bear in mind that there are some **mandatory data** you should include at this step:

-  <u>__Cancellation policies__</u>: _Within the cancelPolicy structure response there is a **refundable** field. If this field is filled in with false, it means that the room has 100% cancellation cost, so the room is non-refundable._
-  <u>__Remarks__</u>
-  <u>__Taxes__</u>
{{% /alert %}}
