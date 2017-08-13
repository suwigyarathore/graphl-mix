# Graphql Mix (Combining multiple data sources in one query)

This is starter project for enthusiast who wants to convert there existing backend code
which gets data from multiple sources (databases or Rest API) to a Graphql backend into single query

This project uses below data sources to combine one data source

* MongoDB (via Mongoose)
* Sqlite (via Sequelize)
* Rest API (via node-fetch)

## About GraphQL

GraphQL is a query language for APIs and a runtime for fulfilling those queries with your existing data. GraphQL provides a complete and understandable description of the data in your API, gives clients the power to ask for exactly what they need and nothing more, makes it easier to evolve APIs over time, and enables powerful developer tools.
To read mode about it [http://graphql.org/]

### More Elegant Data Retrieval :
GraphQL is all about simplicity — and with that simplicity comes a more elegant methodology and experience concerning data retrieval. Because data is collected under a common endpoint or call that is variable concerning the type of data and request as stated in the initial call, several huge benefits are intrinsic to the call system.

### More Backend Stability :
With simplicity comes stability — this is a basic fact of life. The more simple a process is, the less likely there are to be faults in the planning, construction, execution, and continued operation over time. GraphQL makes queries more simple and elegant — and as a result, improves the stability of the entire process

### Better Query Efficiency: 
GraphQL unifies data that would otherwise require multiple endpoints, or in the worst case scenario ad hoc endpoints and complex repeat retrievals, and gives the requester a single, simple entry point.

### GraphQL Is a Specification :
Perhaps one of the greatest benefits of GraphQL is that the overhead for adoption is low specifically due to its status as a specification. While there are always new tools on the market, many developers shy away from adopting these solutions because they’re “too involved” or “too invested” in their REST architecture.

### GraphQL Improves Understanding and Organization :
Perhaps the biggest benefit of implementing GraphQL is one of importance to the API ecosystem as a whole — 99% of the time, an API can be organized into a simple and understandable graph schema, and doing so forces you to better organize and understand your data, the flow of that data, and the inefficiencies and errors in that system.

## Getting Started [Based on Mac]

### Prerequisites

First you need to install mogodb server from [https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/]
Or follow below steps for brew based installation

Update Homebrew’s package database
```
$ brew update
```

Install MongoDB
```
$ brew install mongodb
```

Create the data directory
```
$ mkdir -p /db/mongodb
``` 

Run MongoDB
```
mongod --dbpath ./db/mongodb

```
* If mongo db already started pls use  ``` killall mongod ```
* If lock file error comes pls delete all subfiles in /data/mongodb folder


### Installing

Now lets start our Graphql mix project 

```
git clone https://github.com/suwigyarathore/graphl-mix.git
cd <cloned directory name>
npm install
npm start
```

And go to browser on below to see your application link

```
http://localhost:3000/
```

and run below query


```
{
  author(firstName:"Edmond", lastName:"Jones") {
    id
    posts{
      title
      views
      author{
        firstName
      }
    }
  }
  getFortuneCookie
}
```

End with an example of getting some data out of the system or using it for a little demo


## License

This project is licensed under the MIT License 

## Acknowledgments

* Pls refer [https://dev-blog.apollodata.com/] for more details
* Pls use [http://sqlitebrowser.org/] for viewing sqlite database
* pls user [https://mongobooster.com/] for viewing mongo database
