# URL-Shortener
I have designed a URL shortener that takes in a valid URL and returns a shortened URL, redirecting the user to the previously provided URL.

It also keeps track of total visits/clicks on the URL.

Routes:

POST/URL – Generates a short new URL and returns the shortened URL in the format example.com/random-id.

GET/:id – Redirects the user to the original URL

GET/URL/analytics/:id – Returns the clicks for the provided short id

Created empty SHORT-URL folder
npm init -> will create a package.json file for us.

Now we require some dependencies:
npm i express

For database, I am using mongoose:
npm i mongoose

Created first file index.js
Then created controllers, routes and models
In models there is url.js -> I made model in mongoose, then made Schema
Properties in the Schema are: shortId, redirectURL, visithistory  then made the URL.

Now I made URL of the router:

Now in controller, I made url.js: made an async function to generate a new short url, I used a service named npmjs.com and used the short id package.

On the terminal wrote these commands for verification:
show dbs
use short-url
show collections
urls
db.urls.find({})

Used postman

POST request ->http://localhost:8001/url
now in body write url of any website -> it will generate short id
we will cross check it in our database by writing command db.urls.find({}).
Now in GET request http://localhost:8001/id
