# OOSDCW2
Object Oriented Software Development Coursework 2
In this coursework we’re going to attempt to use object orientation to create an object oriented model of the bus network in Edinburgh.

Task 1   DESIGN
The bus network comprises a number of services (e.g. service 16 to Torphin). Each service has an operator (e.g. Lothian Buses) a service ID (e.g. “1”) and a destination (e.g. “South Leith”). Each service calls at a number of bus stops (each bus stop can be associated with many services).

Design a class diagram to show your BusStop class and another class Service which manages the collection of BusStop objects which comprise all of stops on that service.  Include  a BusNetwork object that manages the set of Service objects and the entire set of BusStop objects. Your diagram should show the relationships between BusStop, Service and BusNetwork. 

You may incorporate elements of your BusStop class created for coursework 1. The BusStop class should have the properties Name (String), ID (String), Latitude and Longitude. You may wish to modify your BusStop to have the latitude and longitude properties held in a separate class called Location and then suggest an appropriate means of relating the BusStop and Location classes.

Your Service class should have an addStop() method than may be used to add a new BusStop object to a Service. Your BusNetwork class should have addStop() and addRoute() methods.

All your classes should have a ToString() method.

 

Marking Scheme
Item

Mark

Classes drawn correctly on diagram

    /5

Properties and methods shown correctly (public/private, data types etc)

    /5

Relationships shown correctly on diagram

(2 marks available for the handling of latitude and longitude)

    /5

(Marks: 1=Attempt made,2=Major Errors,3=Competent Answer, with errors, 4= Competent Answer, with minor errors, 5=No errors noted)
 
 
Task 2 (Basic)
Create a Visual Studio c# solution that contains a WPF project called BusNet, create folders for the object and data layers. 

Implement your BusNetwork, Service and BusStop classes in c# and place them in the object folder.

Add a button to your window with the caption ‘Test’ and  a textArea with the name txtOutput. The button should create an instance of BusNetwork, add two instances of Service to it and then add 5 BusStop objects to each of the BusServuce objects. The output from BusNetwork.toString() should then be displayed in txtOutput. Hint: you should see 10 stops, grouped into two services.

Update your class diagram to show the 3 layer architecture (hint: the data layer will be empty), for the presentation layer you can just show your window class.


Task 2 – (Medium)

It is possible to read in a list of Edinburgh bus stops from the BusStops.CSV file (supplied) using the class CSV Reader (supplied). CSV Reader will turn a CSV file into a 2D string array (see example code in Moodle).

Update your class diagram to show how CSVReader is  incorporated into your design in order to create BusStop objects from the file.  You might want to make use of design patterns at this stage.

Add a button labelled “Load Network” to your window which will create BusStop object for each unique bus stop in the BusStops.CSV file (there should be 2189 bus stops in the file).

Modify your BusNetwork class to have a findStop() method, this should take a busStop ID as a parameter and return a string containing (the stop ID, name and latitude/longitude). Add a button labelled “Find Stop” that takes a stop ID (via a text box) and displays the appropriate stop details in txtOutput (if the stop exists).

Task 2 – (Advanced)

The file EdinburghBusNet.csv contains an entry for each example of a bus service calling at a bus stop. The header and first line of BusNet look like this ….

ServiceID

Service

Destination

BusStopID

Operator

1Clermiston

1

Clermiston

183607047

Lothian Buses

This tells us that the service with the ID “1Clermiston” calls at bus stop ID 183607047, it also tells us that the service is going to “Clermiston” and is operated by Lothian Buses. You can use this data to create a set of Service objects (there should be 103 services) and link them to the appropriate BusStop objects.  

Create a drop-down list of service IDs on your window, when a service is selected from the list, the service details and the list of bus stops associated with that service should be printed to the text area.

Marking Scheme
Highlight on your class diagram where you have made use of design patterns!
Item

Mark

Basic Tasks

 

Test button works correctly

     /5

Class diagram updated to show tiers

     /2

Medium Tasks

 

Incorporation of CSVReader into your design

     /2

Load Network button works correctly

     /5

Find Stop button works correctly

     /5

Advanced Tasks

 

Load Network button correctly

     /5

Design Patterns

 

Use of design patterns in your design

(max 2 patterns. 1- poor attempt, 2 – some issues, 3 – pattern used correctly)

     /6

 

 

Task 3   DISCUSSION
If you have used design patterns in your design for tasks 1 and 2, explain the advantages their use brought to you.

 If you have not used design patterns, suggest a modification to your system which would utilise a design pattern (include a class diagram with your answer).

In both cases justify your choice of pattern.

Your answer should be no more than 2 A4 sides in length (including diagrams).

You are strongly encouraged to look at the marking scheme (below) which gives further details of the criteria which are being assessed.

 Marking Scheme -

Item

Mark

Discussion of the advantages of design patterns

      /5

Incorporation of pattern within your design, including justification

      /5

 

Deliverables            
You should upload the following to Moodle:

1.    A  copy of the submission template, with your work added, please save it as a .PDF named “oosd<matric>.pdf”

DO NOT PLACE THIS PDF IN YOUR .ZIP ARCHIVE, PLEASE UPLOAD IT DIRECTLY TO MOODLE.

 2.    Your Visual Studio Solution for task 2 (as a .ZIP file) – called solution.zip

If there are any issues concerning over use of tools such as ChatGPT or copying of work from other students the markers may ask you to undertake a 1:1 demonstration of your work in order to establish authorship.

