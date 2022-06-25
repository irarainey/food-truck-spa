# San Francisco Food Truck Map

To better enable administration for the licensing of the vast array of food trucks in the San Francisco area, the city manage a dataset of food trucks together with information on the type of food they serve, their location, and their licence status.

This dataset is made available to the public, in a range of different formats, for use in third parties applications. This dataset can be found on the [city's data portal](https://data.sfgov.org/Economy-and-Community/Mobile-Food-Facility-Permit/rqzj-sfat/data).

I have built a simple REST API to import this data into an Azure CosmosDB and provide a `GET` method to query food trucks in a specified area. This data is returned in [GeoJSON](https://datatracker.ietf.org/doc/html/rfc7946) format which can then be used to render easily on a map. The REST API project can be found [in this repository](https://github.com/irarainey/food-truck-api).

This project is a simple HTML / JavaScript application to render food trucks returned from the API on a map using [leaflet.js](https://leafletjs.com/).

This simple single-page application is hosted as an Azure Static Web App and can be found at [https://foodtrucks.codeshed.dev](https://foodtrucks.codeshed.dev).

![San Francisco Food Trucks](https://foodtruckapistorage.blob.core.windows.net/images/foodtrucks.codeshed.dev.png)

The application loads the map with a default start location of the Microsoft office in San Francisco, and an 800 metre range. This can be amended using the controls in the toolbar and reloading the map.
