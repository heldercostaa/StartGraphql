# Start GraphQL

A simple server side application that uses GraphQL to manage Authors and Books data.

## Setup

Install dependencies using `yarn` (or `npm`):

```bash
$ cd ../StartGraphql
$ yarn        # npm install
$ yarn start  # npm start
```

## Usage

Access [http://localhost:5000/graphql](http://localhost:5000/graphql) on your browser and start querying.

### Query examples

```graphql
# Get all author names and their written book names
{
  authors {
    name
    books {
      name
    }
  }
}

# Get a single book of id 1 and its author name
{
  book(id: 1) {
    name
    author {
      name
    }
  }
}

# Add a new book and expect the new id and the book name as a response
mutation {
  addBook(authorId: 1, name: "Fantastic Beasts and Where to Find Them") {
    id
    name
  }
}
```

## Technologies

This project uses:

- Node
- Express
- GraphQL
