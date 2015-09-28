
Ambry Services
==============

The Ambry Service module contains a collections of objects and APIs for accessing Ambry libraries in a variety of ways, including locally, via a CLI and remotely. It also contains definitions for Docker containers in which to run these services. 

The services include:

- A Docker container for running the Public Search application
- A Docker container for running the Login application
- A Docker container for running the User Application
- A Docker container for running the Library ( aka "Collection Server" ) 
- A Docker container for running IPython Notebook
- The Application and Registration Service
- A Docker container for running the Application and Registration Service. 

The Application and Registration Service coordinates the interactions of the docker containers. 

- When a user logs in via the Login application, the Login Application uses the ARS to eitehr find or start a User Application for the user. 
- When in the User Application, the user accesses a collection, the UA contacts the ARS to find or start a Library container for the collection. 
- When the user creates or opens an IPython notebook, the UA contacts the ARS to find or create a Notebook container. 

The ARS also can create:
- Rublic Search application containers
- Login Application containers
- The main Library container

The ARS has an RPC interface, implemented in Pyro. 
