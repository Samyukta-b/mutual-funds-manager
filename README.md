# Mutual Funds Manager

This is a backend-based Mutual Fund manager which allows users to add and view mutual funds of their choice written in Go.  

# Prerequisites

- Go programming language             -> `https://go.dev/doc/install`
- MongoDB Community Server Download   -> `https://www.mongodb.com/try/download/community`
- MongoDB Compass                     -> `https://www.mongodb.com/try/download/compass`
- Postman API tool                    -> `https://www.postman.com/downloads/`

Make sure the MongoDB Server is runnning. To check, go to Start and type `Services`. Look for the MongoDB server and make sure its running. If not, right click and select `Start`.

# Setting Up Environment Variables

If MongoDB is installed, find the directory where it is installed. The default installation path for MongoDB on Windows is typically: `C:\Program Files\MongoDB\Server\<version>\bin`. Replace <version> with the version number you installed (e.g., 5.0).

# Setting up MongoDB Compass

After connecting to `localhost:27017`, create a new Database `mutual_funds` with Collection name as `funds`. 

# Setting up Postman

Postman is a tool for testing and interacting with APIs. To set up Postman for interacting with the APIs, create a new Collection named "mutual fund manager" and add Requests within it. Right-click on the collection to add a request, then choose the HTTP request method `(GET, POST, PUT, DELETE)` and paste the corresponding URL for the desired API endpoint. The methods and URLs for this project are provided below.

## API Endpoints:

### Lists All Mutual Funds `GET`
        
URL: `http://localhost:8080/getAllFunds`
Description: Lists all the mutual funds available in the database

### Create new mutual fund `POST`
URL: `http://localhost:8080/addFund/`
Description: Allows creation of a new mutual fund data

## Getting Started

Run the application using `go run main.go`. 

## Example Input Data on Postman

Input data can be entered by selecting `Body` tab, then choosing `raw and JSON` format, and pasting the data accordingly. Ensure to follow the provided example for input data structure.

```
{
    "name": "Motilal Oswal ",
    "category": "Equity",
    "cagr": [
        {
            "1_year": 10.5,
            "3_year": 8.7,
            "5_year": 9.2
        }
    ],
    "rating": 5
}
```

# Resources & others

MongoDB tutorial: https://www.youtube.com/playlist?list=PL4cUxeGkcC9h77dJ-QJlwGlZlTd4ecZOA

For reference: ![Download Postman Video demo ](postman-demo-video.mp4)
