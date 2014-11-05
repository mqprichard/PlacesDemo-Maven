PlacesDemo-Maven
================

Android demo with Google Geocoding, Elevation and Civic Information API: for Maven and ant (Eclipse ADT) builds.
The same source code project can be used for both project types

Using Google APIs
-----------------
You will need a Google API key to access the [Geocoding API](https://developers.google.com/maps/documentation/geocoding/), [Elevation API](https://developers.google.com/maps/documentation/elevation/) and [Google Civic Information API](https://developers.google.com/civic-information/): these services have courtesy limits, which allow limited use free of charge. Use the [Google API Console](https://code.google.com/apis/console) to create a Google API project, add the required services (APIs & Auth -> API) and then create an API Key (APIs & Auth -> Credentials). Create a Browser key and leaved the Allowed Referers field blank.

Create the following class file (GooglePlacesKey.java) in src/com/example/appdynamicsplacesdemo adn copy your API key:
```
package com.example.appdynamics.placesdemo;

public class GooglePlacesKey {
    public static final String API_KEY = "<your API key>";
}
```

Eclipse ADT Builds
------------------
1.  Import -> Existing Android code into workspace
2.  Properties -> Android -> Android 5.0 (API Level 21)
3.  Build Path -> Configure Build Path -> Libraries -> Add External JARs
4.  Clean and rebuild the project

The following JAR files need to be added to the project:

* [google-api-client-1.19.0.jar](http://search.maven.org/remotecontent?filepath=com/google/api-client/google-api-client/1.19.0/google-api-client-1.19.0.jar)
* [google-api-services-civicinfo-v2-rev7-1.19.0.jar](http://search.maven.org/remotecontent?filepath=com/google/apis/google-api-services-civicinfo/v2-rev7-1.19.0/google-api-services-civicinfo-v2-rev7-1.19.0.jar)
* [google-http-client-1.19.0.jar](http://search.maven.org/remotecontent?filepath=com/google/http-client/google-http-client/1.19.0/google-http-client-1.19.0.jar)
* [google-http-client-android-1.19.0.jar](http://search.maven.org/remotecontent?filepath=com/google/http-client/google-http-client-android/1.19.0/google-http-client-android-1.19.0.jar)
* [google-http-client-gson-1.19.0.jar](http://search.maven.org/remotecontent?filepath=com/google/http-client/google-http-client-gson/1.19.0/google-http-client-gson-1.19.0.jar)
* [gson-2.3.jar](http://search.maven.org/remotecontent?filepath=com/google/code/gson/gson/2.3/gson-2.3.jar)
