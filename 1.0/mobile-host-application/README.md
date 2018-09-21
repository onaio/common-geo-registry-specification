# Mobile Host Application Specification

The mobile host application (i.e. OpenSRP, DHIS2 Android App, etc.) has a large role in this implementation. It is responsible for managing all business logic related to mobile mapping, storing program data and interacting with both the GeoWidget and the RESTful Geo-Object Mobile Interface. The mobile host application is responsible for activating the GeoWidget when appropriate using Android intents, posting program data in GeoJSON for GeoWidget consumption and supporting callbacks from the GeoWidget to get more program data for display. Futhermore, the mobile host application is responsible for retaining a list of new and updated Geo-Objects and posting them to the GeoRegistry using the RESTful Geo-Object mobile interface.

## Definitions

* Geo-Objects - Geo-Objects are points and polygons stored in GeoJSON that are pertinent for the functioning of the health system. They may include metadata that supports business classification of each object, but no program data should be stored in the GeoRegistry or GeoWidget.
* Program Data - We define program data separately from the Geo-Objects. Program Data is information that applies to running a real-world program. Program data relies on information in the GeoRegistry and GeoWidget.

## Assumptions

* The mobile host application is responsible for all business logic and storage of program data.