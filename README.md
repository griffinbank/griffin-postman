## Griffin API Postman Collection

This is a postman collection covering the Griffin API. See https://docs.griffin.sh/ for more details.

## Getting started

1. Register for a [Griffin sandbox account](https://griffin.sh/sandbox), if you haven't already.
2. Follow our [getting started with the API guide](https://docs.griffin.sh/docs/guides/getting-started-with-the-api) to learn how to create an API key and make simple requests.
3. Install [Postman](https://www.getpostman.com/downloads/)

## Import collection 

In your Postman workspace, click `Import`, then you can choose to either download our [collection JSON file](./postman_collection.json) and select it as a file, or copy its contents and import as 'raw text'.

## Set your API key

Once you have your API key, set it as an [environment variable](https://learning.postman.com/docs/sending-requests/variables/) named `griffin-api-key`, within your workspace.

### Making requests

Each request in the Griffin collection has a [Postman test](https://learning.postman.com/docs/writing-scripts/test-scripts/) that runs on the response. This test will interrogate each response body and for every URL assign a corresponding [Postman environment variable](https://learning.postman.com/docs/sending-requests/variables/).

As an example, when making the `Index` request (in the `setup` folder), you'll see the response body includes an `api-key-url`, among others. You should also now see a Postman environment variable named `api-key-url` with the URL as the value. We lean on this to easily 'navigate' the API from the root rather than hardcode routes and interpolate resource IDs.

## Using the Postman Collection

Within our collection you'll find three top-level folders: `Setup`, `Reference`, and `Guides`.

### Setup

Once you have your API configured, the first thing you'll want to do is run the `Setup` folder. This make a series of API requests from the `index` route and populate a bunch of Postman environment variables that you'll need to do anything useful, e.g. your `organization-url`, `organization-corporations-url` etc.

### Reference

As a companion to our [API reference documentation](https://docs.griffin.sh/api), here you'll find individual requests grouped by resource.

### Guides

Currently the collection has the `Onboard your customers` guide. It includes the series of API calls described in our [Onboarding your Customers](https://docs.griffin.sh/docs/guides/onboarding-your-customers) guide.
