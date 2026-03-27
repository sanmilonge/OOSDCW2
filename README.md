# BusNet – Bus Network Management System (OOSD Coursework 2)

![Language](https://img.shields.io/badge/Language-C%23-blue)
![Framework](https://img.shields.io/badge/Framework-WPF-.NET-purple)
![Architecture](https://img.shields.io/badge/Architecture-OOP-green)
![Design Pattern](https://img.shields.io/badge/Pattern-Factory-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)
![License](https://img.shields.io/badge/License-Educational-lightgrey)

---

## Overview

**BusNet** is a C# WPF application developed for **Object-Oriented Software Development (OOSD) Coursework 2**.
The system models a real-world bus network, allowing users to load, manage, and query bus stops and services using structured object-oriented design.

The application demonstrates key software engineering principles including modular design, separation of concerns, and the use of design patterns.

---

## Objectives

* Design a scalable object-oriented system
* Model real-world entities (bus stops, services, locations)
* Implement data-driven functionality using CSV input
* Apply design patterns (Factory Pattern)
* Build an interactive graphical user interface (WPF)

---

## System Architecture

The application is composed of several core components:

### Core Classes

* **BusStop**

  * Represents an individual bus stop
  * Stores ID, name, and geographic location

* **Location**

  * Encapsulates latitude and longitude

* **Service**

  * Represents a bus service (route)
  * Maintains a list of associated bus stops

* **BusNetwork**

  * Central controller managing:

    * All bus stops
    * All services
  * Provides lookup and aggregation functionality

---

### Supporting Components

* **ServiceFactory**

  * Implements the Factory Design Pattern
  * Responsible for creating `Service` objects

* **CSVReader** *(external dependency in project)*

  * Reads structured data from CSV files
  * Used to populate stops and routes

* **MainWindow (WPF UI)**

  * Handles user interaction
  * Connects UI controls to backend logic

---

## Features

* Load bus stops from CSV data
* Load bus routes and associate stops dynamically
* Search for bus stops by ID
* View services and their associated stops
* Interactive GUI using WPF
* Data-driven system design
* Factory Pattern implementation for object creation

---

## Project Structure

```bash
.
├── BusStop.cs           # Bus stop entity
├── BusNetwork.cs        # Network manager
├── Service.cs           # Bus service logic
├── ServiceFactory.cs    # Factory pattern implementation
├── Location.cs          # Geographic data model
├── MainWindow.xaml.cs   # UI logic (WPF)
├── resources/
│   ├── BusStops.csv
│   └── EdinburghBusNet.csv
└── README.md
```

---

## How It Works

### 1. Load Bus Stops

* Reads `BusStops.csv`
* Creates `BusStop` objects
* Stores them in a dictionary for fast lookup

### 2. Load Routes

* Reads `EdinburghBusNet.csv`
* Groups stops into services
* Uses `ServiceFactory` to create service objects

### 3. User Interaction

* Search for a stop by ID
* Select a service from a dropdown
* View full route details

---

## How to Run

### Prerequisites

* .NET SDK (6.0 or higher)
* Visual Studio (recommended for WPF)

### Steps

```bash
dotnet build
dotnet run
```

Or open the solution in Visual Studio and run the project.

---

## Example Functionality

* Load network → Displays total number of stops
* Load routes → Populates services dynamically
* Search stop → Returns stop details with coordinates
* Select service → Displays full route and stops

---

## Design Principles

### Object-Oriented Design

* **Encapsulation**: Data stored in well-defined classes
* **Abstraction**: Complex logic hidden behind methods
* **Modularity**: Clear separation between components

### Design Patterns

* **Factory Pattern**

  * Used to instantiate `Service` objects
  * Improves scalability and maintainability

---

## Data Structures Used

| Structure  | Purpose                               |
| ---------- | ------------------------------------- |
| Dictionary | Fast lookup of bus stops by ID        |
| List       | Ordered storage of services and stops |

---

## Limitations

* No persistent storage beyond CSV files
* Minimal input validation on CSV data
* UI is functional but not optimized for UX
* No asynchronous processing for large datasets

---

## Future Improvements

* Add database integration (SQL or NoSQL)
* Implement MVVM architecture for WPF
* Add filtering and search enhancements
* Improve UI/UX design
* Add error handling for malformed CSV data
* Implement unit and integration testing

---

## Author

Oluwasanmi Longe
Matriculation Number: 40798397
GitHub: https://github.com/sanmilonge

---

## License

This project is intended for academic and educational use only.

---
