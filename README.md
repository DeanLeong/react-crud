# React + CRUD

## Learning Objectives

- Perform create, read, update, delete actions in JavaScript using Axios
- Use the Airtable API to store our data
- Create a React frontend to interact with our data

## HTTP

HTTP stands for **Hyper-Text Transfer Protocol**. If the client and server communicate, then HTTP is the structure of that communication. HTTP dictates how the client requests information from a server and how the server responds. Each message is similarly formatted - so you can think of them as like electronic telegrams.

Requests consist of these three parts:

1. Request line (including the URL and the HTTP Method)
1. Request header (additional information about the request and what we expect in the response)
1. Body message (optional - things like form data)

Responses in turn consist of these three parts:

1. Status (a status code indicating how the request was handled)
1. Response header (additional information about the response)
1. Body message (optional - an html document, JSON, XML)

Clients make requests to a location (called a URL) using a method. There are 10 possible HTTP methods, but only 5 that are important:

| Method Name | Description |
| --- | --- |
| GET | Used for retrieving data from a server. |
| POST | Used for sending data to the server. |
| PUT | Used for replacing data on the server. |
| PATCH | Used for updating data on the server. |
| DELETE | Used for deleting data from the server. |

When the server receives a request, it processes the message and then sends a response. The server always sends a response, though sometimes that response is just to tell the client that there was an error. Generally, the response will be an HTML document.

## How to do it with Axios

We can do all these actions in Axios.

Post (create):
```js
const makeApiCall = async () => {
  const req = await axios.post(yourUrl, { data: 'you want to send to the server' })
}
```

Put (update):
```js
const makeApiCall = async () => {
  const req = await axios.put(yourUrl, { data: 'you want to send to the server' })
}
```

Delete (delete):
```js
const makeApiCall = async () => {
  const req = await axios.delete(yourUrl)
}
```

## Airtable

"Airtable works like a spreadsheet but gives you the power of a database to organize anything."

We are going to use Airtable to create an API for ourselves with just a few clicks. When you get to the next unit, you will be learning how to build out a full-fleged, super powerful backend with a full database. In this unit, to keep things simple, we will just use Airtable to store our data. But, good news! We can implement full CRUD so that your projects will be *awesome*.

1. Create an Airtable account.
1. Create a base (no template needed).
1. Create the following columns:
- title (text)
- text (text)
- author (text)
- created_at (created time)
1. Navigate to `https://airtable.com/api` and select your base.

## Integration with React

Let's create a React app to consume our Airtable data!

[Solution Code]() will be provided after the class is finished.
