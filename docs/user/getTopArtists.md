Get the top artists listened to by a user. You can stipulate a time period. Sends the overall chart by default.

No authentication required.

## Parameters
| Method         | Type                                                                                               | Default | Optional | Description                                            |
| -------------- | -------------------------------------------------------------------------------------------------- | ------- | -------- | ------------------------------------------------------ |
| `user`         |[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)   |`none`   | :negative_squared_cross_mark: | The last.fm username to fetch top artists for.
| `period`       |[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)   | overall    | :white_check_mark:            | The time period over which to retrieve top albums for. Can be `overall`, `7day`, `1month`, `3month`, `6month` or `12month`
| `limit`        |[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)   | 50      | :white_check_mark:            | The number of results to fetch per page. Defaults to 50.
| `page`         |[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)   | 1       | :white_check_mark:            | The page number to fetch. Defaults to first page.
| `api_key`      |[token](https://www.last.fm/api/account/create)                                                     |`none`   | :negative_squared_cross_mark: | A Last.fm API key.


## Responses
Errors:

- 6 : Invalid parameters - Your request was either missing a required parameter, the parameter was not found, or had 0 results
- 8 : Operation failed - Something else went wrong  
- 9 : Invalid session key - Please re-authenticate  
- 10 : Invalid API key - You must be granted a valid key by last.fm  
- 11 : Service Offline - This service is temporarily offline. Try again later.  
- 13 : Invalid method signature supplied  
- 16 : There was a temporary error processing your request. Please try again  
- 26 : Suspended API key - Access for your account has been suspended, please contact Last.fm  
- 29 : Rate limit exceeded - Your IP has made too many requests in a short period  


## Examples
??? note "Example response"

    | Parameter | Value |
    | --------- | ----- |
    | username  | aidan-|
    | limit     | 3     |
    | format    | json  |

    HTTP status: `200 OK`

    ```
    http://ws.audioscrobbler.com/2.0/?api_key=YOUR_API_KEY&method=user.getTopArtists&user=aidan-&format=json&limit=3
    ```

    ```json
    {
        "topartists": {
            "artist": [
                {
                    "@attr": {
                        "rank": "1"
                    },
                    "mbid": "5eecaf18-02ec-47af-a4f2-7831db373419",
                    "url": "https://www.last.fm/music/Queen",
                    "playcount": "1511",
                    "image": [
                        {
                            "size": "small",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/34s/2a96cbd8b46e442fc41c2b86b821562f.png"
                        },
                        {
                            "size": "medium",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/64s/2a96cbd8b46e442fc41c2b86b821562f.png"
                        },
                        {
                            "size": "large",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/174s/2a96cbd8b46e442fc41c2b86b821562f.png"
                        },
                        {
                            "size": "extralarge",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/300x300/2a96cbd8b46e442fc41c2b86b821562f.png"
                        },
                        {
                            "size": "mega",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/300x300/2a96cbd8b46e442fc41c2b86b821562f.png"
                        }
                    ],
                    "name": "Queen",
                    "streamable": "0"
                },
                {
                    "@attr": {
                        "rank": "2"
                    },
                    "mbid": "f4903035-e9cd-4b7f-b462-0447b0cd490a",
                    "url": "https://www.last.fm/music/Videoclub",
                    "playcount": "1124",
                    "image": [
                        {
                            "size": "small",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/34s/2a96cbd8b46e442fc41c2b86b821562f.png"
                        },
                        {
                            "size": "medium",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/64s/2a96cbd8b46e442fc41c2b86b821562f.png"
                        },
                        {
                            "size": "large",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/174s/2a96cbd8b46e442fc41c2b86b821562f.png"
                        },
                        {
                            "size": "extralarge",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/300x300/2a96cbd8b46e442fc41c2b86b821562f.png"
                        },
                        {
                            "size": "mega",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/300x300/2a96cbd8b46e442fc41c2b86b821562f.png"
                        }
                    ],
                    "name": "Videoclub",
                    "streamable": "0"
                },
                {
                    "@attr": {
                        "rank": "3"
                    },
                    "mbid": "c0252a1b-0133-46bb-8c4f-cade46349ec3",
                    "url": "https://www.last.fm/music/Alestorm",
                    "playcount": "1079",
                    "image": [
                        {
                            "size": "small",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/34s/2a96cbd8b46e442fc41c2b86b821562f.png"
                        },
                        {
                            "size": "medium",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/64s/2a96cbd8b46e442fc41c2b86b821562f.png"
                        },
                        {
                            "size": "large",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/174s/2a96cbd8b46e442fc41c2b86b821562f.png"
                        },
                        {
                            "size": "extralarge",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/300x300/2a96cbd8b46e442fc41c2b86b821562f.png"
                        },
                        {
                            "size": "mega",
                            "#text": "https://lastfm.freetls.fastly.net/i/u/300x300/2a96cbd8b46e442fc41c2b86b821562f.png"
                        }
                    ],
                    "name": "Alestorm",
                    "streamable": "0"
                }
            ],
            "@attr": {
                "page": "1",
                "total": "1931",
                "user": "aidan-",
                "perPage": "3",
                "totalPages": "644"
            }
        }
    }
    
    ```
