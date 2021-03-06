# San Francisco Food Truck Map

To better enable administration for the licensing of the vast array of food trucks in the San Francisco area, the city authority manage a dataset of food trucks together with information on the type of food they serve, their location, and their licence status.

This dataset is made available to the public, in a range of different formats, for use in third-party applications. This dataset can be found on the [city's data portal](https://data.sfgov.org/Economy-and-Community/Mobile-Food-Facility-Permit/rqzj-sfat/data).

I have built a simple REST API to import this data into an Azure CosmosDB and to provide a `GET` method to query food trucks within a specified area. This data is returned in [GeoJSON](https://datatracker.ietf.org/doc/html/rfc7946) format which can then be used to render trucks easily on a map. The REST API project can be found [in this related repository](https://github.com/irarainey/food-truck-api).

This project is a simple JavaScript application to render food trucks returned from the API on a map using [leaflet.js](https://leafletjs.com/).

The default start location for the map the Microsoft office in San Francisco, with an 800 metre range specified. These parameters can be amended using the controls in the toolbar.

![San Francisco Food Trucks](https://githubrepoimages.z33.web.core.windows.net/foodtrucks.codeshed.dev.png)

