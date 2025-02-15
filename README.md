==========================
        Read Me
==========================

GeoLocator v2.0
The geolocation algorithm contains both geoparser that extract locations and a geo-coder that assigns latitude and longitude to each location.

The algorithm takes tweet JSON file as input, or tweet-like sentence as input. However, you can not specify the user information in sentence, so we recommand that you use the full JSON file, which includes more information as the system is trained. However, the geoparser is the same no matter if user location is available or not.

In addition to a gelocation algorithm, the package contains a fuzzy match algorithm that takes web 2.0 tags plus latitude and longitude as input, and compares them with location entries in the GeoNames gazetteer to determine whether the web 2.0 entries match with the gazetteer entries or they are novel.

/////////////// Introduction ///////////////

Tagging the command line input

The output format for the commandline and batch file: Each recognized location is one of those types: TP,tp, ST,st,BD,bd,AB,ab. TP, ST, BD, AB are output from the Named Entity Recognizer. tp,st,bd,ab are the output from the rule based and toponym lookup parsers.

The geocoding result is able to output all the information that is stored in the GeoNames gazetteer for a location, such as country, state info, latitude and longitude, geographical feature type (whether it's a city, country, state, mountain, airport, or something. The meaning of the specific type can be looked up in GeoNames.org).  

/////////////// How to Install ///////////////

The algorithm can run on Windows, Mac, or Linux/Unix platforms.

1.Check out the project.
In eclipse, try import ->project from git.

2. After checked out the project into Eclipse workspace,
Go to the terminal (if you are using linux or mac osx), or cygwin for windows, cd to the geo-locator folder, run isntall.sh to install the software.
This is a long process because we have to download jar files, resources from geonames, and most time-consuming is the indexing of the geoname.
The estimate time is about 1 hour. It varies with your machine. 

Please go to quickstart to see how to use the geolocator.

To run the fuzzy match algorithm in edu.cmu.geoparser.nlp.spelling, please see the instructions in FuzzyGeoMatch project.

Please send email to wei.zhang@cs.cmu.edu or gelern@cs.cmu.edu if you find any bug or have any question, or any suggestions.



////////////// To Do List //////////////////

1. Improve the speed of the geolocator.
2. Use ranking instead of binary classification for geocoder
3. Add openstreetmap data for matching streets and buildings
