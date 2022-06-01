# graphql-restaurant-exercise

## About
A simple project to run a ecpress-graphql server

## Run Instructions
1. Clone project or download the project
2. Open terminal on mac
3. cd into the cloned or downloaded project directory
4. Install dependencies by running
```sh
npm install
```
5. Run the server
```sh
node index.js
```

Once the server is running navigate to: `localhost:5500/graphql`


## Useful graphql queries
```graphql
query getrestaurant($iid: Int = 1) {
  restaurant(id: $iid) {
    name
    description
  }
}

query getrestaurants {
  restaurants {
    id
    name
    description
    dishes {
      name
      price
    }
  }
}

mutation setrestaurant {
  setrestaurant(input: {
    name: "Granite",
    description: "American",
  }) {
    name
    description
  }
}

mutation Deleterestaurant($iid: Int = 1) {
  deleterestaurant(id: $iid) {
    ok
  }
}

mutation editrestaurant($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}
```
