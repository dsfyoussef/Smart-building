Project Description
This project involves creating a client to interact with Azure Digital Twins (ADT) and building a digital twin model for smart space management. It consists of two main parts: creating models and generating a graph of interconnected objects (spaces, thermostats, etc.) within an IoT application. note that this code will help juste to create the relation and the graphical interface of your digital twin model and not to send the data on it.

Features:

1.Loading Models (LoadModels):

The project allows you to load models defined in JSON from a specific folder, which are then validated to ensure they conform to the Digital Twin Definition Language (DTDL) format.
The models are then created within the ADT system.

2.Creating Digital Twins (BuildGraph):

Digital twins are created to represent physical objects (e.g., spaces and thermostats).
A space model is created, and objects such as rooms and thermostats are added.
Relationships (links) are established between these objects. For example, a floor contains rooms, and a room contains a thermostat.

3.Model and Relationship Creation:

Each model represents an entity type, such as a Space (with properties like "Temperature" and "Comfort") or a Thermostat.
Relationships between the models are defined, such as a floor containing rooms or a room containing a thermostat.

4.Authentication and Connection with Azure ADT:

The client authenticates with Azure using DefaultAzureCredential, allowing it to connect to the specified Azure Digital Twins instance in the configuration.

Main Code:

Program.cs: This file contains the main logic of the application. 
It loads configurations (such as the Azure Digital Twins instance URL) from an appsettings.json file. 
It then connects to ADT, loads the models, and creates digital objects and their relationships.

Key Method Calls:

 -LoadModels(): Loads and validates model files.
 
 -BuildGraph(): Creates digital objects (twins) and defines their relationships.
 
 -CreateDigitalTwin(): Creates a digital twin using a model and adds properties.
 
-CreateRelationship(): Creates a relationship between two digital twins.

Model Files:

The model files (e.g., SpaceModel.json, Room.json, Thermostat.model.json) define the structure of the digital objects created in the ADT system. They are in the DTDL (Digital Twin Definition Language) format, a language used to describe digital twins.

SpaceModel.json: A model representing a space with properties such as "Temperature" and "ComfortIndex".

Room.json: A model representing a room, with properties like "Temperature" and "Humidity".

Thermostat.model.json: A model representing a thermostat, with configuration and measurement properties.

Conclusion:

This project is a great starting point for interacting with Azure Digital Twins in C# and understanding how to create and manage digital models and twins in an IoT environment. It provides a framework for integrating physical data into digital systems using the Azure Digital Twins API.
