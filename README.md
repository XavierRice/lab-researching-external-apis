# Researching External APIs Lab

## Getting Started

1. Fork and clone this repository.

1. Answer the questions below by editing this readme. Leave the questions and prompts, and answer in between them. Take the time to read back the work, and edit what you've written so that your answers are clear and anyone reading it can easily understand what you've written.

1. When it is applicable, please add screenshots, photos, and links.

## Instructions

You will be planning a new application to develop that uses a third-party API. The app should be a simple idea, as the goal is to research and determine if an API is appropriate for your API.

Choose one of the following categories and APIs:

- Music: [Spotify API](https://developer.spotify.com/documentation/web-api)
- Movies: [OMDB API](https://www.omdbapi.com)
- Text Translator: [Rapid Translate](https://rapidapi.com/auth/sign-up?referral=/sibaridev/api/rapid-translate-multi-traduction)
- Sports: [Sports Score](https://rapidapi.com/tipsters/api/sportscore1)
- City Info: [311 Call Aggregator](https://data.cityofnewyork.us/browse?Dataset-Information_Agency=311)
- Art : [Metropolitan Museum of Art ](https://metmuseum.github.io)

Next, describe your application idea. Your application idea should be simple and make use of the data received by the API. It can make use of other data if necessary.

> Your application idea: The House Party app--it would be a community playlist app. A party or a resturant could create a shared playlist. The owner of the playlist could deny certain songs, or limit the genres- but the songlist would be expanded because everyone would have access. Great for parties or resturants and bars where the staff picks the music.

Write 3 - 5 user stories for your application. Include each below.

> 1. As a <PARTY Host or Resturant Manger> i could regulate the genres of music people are selecting from. 

> 2. As a <PARTY Host or Resturant Manger> i could ban certain song selections.

> 3. As a <PARTY GUEST or RESTURANT EMPLOYEE> i could select songs that i think people would enjoy.

> 4. As a <PARTY GUEST or RESTURANT EMPLOYEE> if my songs were enjoyed or ⭐️'d by multiple people i would get the opportunity to pick more.

> 5. As a <PARTY Host or Resturant Manger or Guest || Employee> if i enjoyed the song selections i could save it to a spotify playlist in my account.

> 6. As a <PARTY GUEST or RESTURANT EMPLOYEE> i would not need a spotify account to particpate in music selection but i would drive me to get one.


What data is needed to complete your application? Describe the data below and provide a link in the documentation showing where to get this data.

> The data I need for my app is ...

  <POST> creating and manipulating playlist: [https://developer.spotify.com/documentation/web-api/reference/create-playlist]
  <GET>  selecting and manipulating the genre selections: [https://developer.spotify.com/documentation/web-api/reference/get-recommendation-genres]
   <GET> searching for music to add to the playlist [https://developer.spotify.com/documentation/web-api/reference/search]


Determine the number of free requests you can make to the API. Include a link in the documentation showing where you found this limit, if possible.

> The number of free requests I can make is found at: [https://developer.spotify.com/documentation/web-api/concepts/rate-limits]
"Spotify's API rate limit is calculated based on the number of calls that your app makes to Spotify in a rolling 30 second window." although.. "A few API endpoints, like the playlist image upload endpoint, have a custom rate limit that may differ from your app-wide rate limit." I assume we would need to apply for an "Extended Quota Mode". 

Would the number of free requests you can make to the API be sufficient for you to develop a basic version of the application within a week? Why or why not?

>  I believe at first yes! For a MVP - We would need to be stragic in making request-take advantage of Get Multiple Albums for frequently requested artists. and take advangtage of the snapshot-id feature. [https://developer.spotify.com/documentation/web-api/concepts/playlists]
                     [https://developer.spotify.com/documentation/web-api/reference/get-multiple-albums]

Does working with the API require the use of a credit card? If possible, include a link in the documentation showing where you found this requirement.

> A credit card is NOT required however i would need a devlopers to have a spotify account though i don't belive it needs to be a paid account.

Write one GET request to your chosen API with Postman. This may involve requesting an API key or other steps. If you requested an API Key, **don't include it.** Instead, replace that part of the URL WITH `<MY API KEY>.` 

> Requested URL : https://api.spotify.com/v1/artists/1vCWHaC5f2uS3yhpwWbIA6/albums?album_type=SINGLE&offset=20&limit=10

Include a snippet of the data you received from the above request.

```
Honestly, trying to figure it out now. I have a client Id and Client secret but trying to figure it out in postman.
As of now the spotify API uses express or curl which i dont fully understand as of yet-but there is access through rapidAPI but it requires a credit card!!  this is what i get:   

4011 err and 

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Postman-Token: 81d28241-ffb1-460b-ad01-cb7c46c1a671
Host: spotify23.p.rapidapi.com
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
Response Headers
Date: Fri, 25 Aug 2023 16:50:54 GMT
Content-Type: application/json
Transfer-Encoding: chunked
Connection: keep-alive
X-RapidAPI-Version: 1.2.8
X-RapidAPI-Region: AWS - us-east-1
X-RapidAPI-Proxy-Response: true
Server: RapidAPI-1.2.8


```

> **Note**: If you could not get an API key for any reason (like it required a credit card or took too long for an API key to be delivered), just leave a note here and do your best to answer the questions anyway.

What file do you need to store an API key safely?

> The filename is typically .ENV file

Why do you want to place that file within the `.gitignore` file?

> Your answer here... you want to ignore the file and not push it up to gitHub for unfettered access.

