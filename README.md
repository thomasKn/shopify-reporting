# Meteor Boilerplate using Shopify Polaris

This project aims to help anyone building a Shopify app with Meteor JS.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Before getting started you need to install [Node](https://nodejs.org/en/) and [Meteor](https://www.meteor.com/) on your machine. You also need to create a [Shopify Partner](https://help.shopify.com/api/getting-started) account and create a new Shopify app.

### Installing

To launch the project on your machine you first need to clone the repo.
Open your terminal and run:

```
git clone https://github.com/thomasKn/shopify-reporting.git
```

Then install the dependencies:

```
meteor npm install
```

Then create a file named settings-development.json and add your Shopify App credentials. The redirectUri field should be ```http://localhost:3000/callback/```. This file will be used during the launch of the Meteor server. More info about Meteor settings [here](https://themeteorchef.com/base/settings).

```
{
  "public": {},
  "private": {
    "OAuth": {
      "shopify": {
        "sharedSecret": "YOUR-SHOPIFY-APP-SECRET-KEY",
        "redirectUri": "http://localhost:3000/callback/",
        "apiKey": "YOUR-SHOPIFY-APP-API-KEY"
      }
    }
  }
}
```

And finally you can launch the server:

```
npm start
```

Then go to http://localhost:3000/, create an account and connect a Shopify store from the settings page http://localhost:3000/settings. Your orders should automatically be imported (http://localhost:3000/orders).

## Built With

* [Shopify Polaris](https://polaris.shopify.com/) - The Shopify library used for UI
* [Meteor](https://www.meteor.com/) - Full stack JS framework
* [React](https://reactjs.org/) - Front end JS framework
* [The Meteor Chef Base](https://themeteorchef.com/base/introduction) - Base is a starting point for Meteor applications. The file structure of the project is explained [here](https://themeteorchef.com/base/file-structure)
