# GraphQLQuery1
GraphQL Exercise for a restaruant database with name, description, en dishes they offer.
With the functionality added, you can get the list of restaurants, add restaurants, modify them and delete them.
To execute this app download the files, install the node dependencies and run index.js. It will run in port localhost:5500/graphql.

Here are the Grapql queries:


mutation editrestaurants($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}

mutation setrestaurants {
  setrestaurant(input: {
    name: "cacatua",
    description: "super",
  }) {
    name
    description
  }
}

mutation deleterestaurants($iid: Int = 3) {
  deleterestaurant(id: $iid) {
    ok
  }
}

query getrestaurants {
  restaurants {
    name
    description
    dishes {
      name
      price
    }
  }
}
