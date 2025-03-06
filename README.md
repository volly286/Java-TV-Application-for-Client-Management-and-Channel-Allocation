# Java Spring Boot/JavaFX Application  
**Author**: Marin Valentin-Gabriel 432B  

## Introduction  
The presented application is developed using Java Spring Boot for the backend and JavaFX for the frontend, with CSS for styling. It manages an N:M relationship between two entities: clients and TV stations. The project combines the advantages of a modern architecture based on Spring Boot, providing a robust and scalable backend, with a user-friendly and easy-to-use graphical interface developed with JavaFX.

## Technologies Used  
- **Java Spring Boot**: The Spring Boot framework is used to develop the backend of the application. It provides quick setup, support for REST APIs, and easy integration with MySQL.  
- **JavaFX and CSS**: JavaFX is used to create a modern and responsive graphical interface. CSS is used to customize the design of elements in the application.  
- **MySQL**: The database used is MySQL, and the connection to the application is made using the mysql-connector library.

## Application Description  
The application manages the N:M relationship between two main entities:
- **Clients** - represented by attributes: first name, last name, and email.
- **TV Stations** - each having a name and description.

The application's functionalities include:
- CRUD (Create, Read, Update, Delete) for the `clients` and `tv_stations` tables.
- Associating and dissociating the entities `clients` and `tv_stations` through an intermediate table `clients_tv_stations`.

## Database Diagram  
The database diagram represents the N:M relationship between `clients` and `tv_stations` through the `clients_tv_stations` table. It was generated using MySQL Workbench and can be accessed via the file `MySQL_Diagram.html` in the resources folder.

## Application Folder Structure  
The complete project structure can be found in the resources folder, under the name `Project_Structure_Java.html`.

## Important Code Sections  

### CRUD Functionalities:

#### List Clients:
- The `getAllClients()` method fetches the list of all clients from the backend via a GET HTTP request.
- Constructs the HTTP request and sends it to the backend to retrieve the response.
- Checks the HTTP response status and handles errors.

#### Add Client:
- The `handleAdd()` method retrieves the data entered by the user, validates it, and creates a `Client` object.
- It calls the `ClientService` service to add the client to the database.
- Exception handling and user notification.

#### Edit Client:
- The `handleEdit(Client client)` method opens a window to edit an existing client.
- The client's data is pre-filled in the edit form.

#### Delete Client:
- The `deleteClient(int id)` method deletes a client from the backend via a DELETE HTTP request.
- Sends the request to the server and checks the response.
- Error handling for an incorrect response.

## Installation and Usage Guide

### Install JDK21:
1. Download the file `jdk-21-windows-x64.exe` from the official JDK website.
2. Run the installer and follow the indicated steps.
3. Add JDK 21 to the PATH:
   - Open system settings (System Properties -> Environment Variables).
   - In the `Path` variable, add the path to the JDK's bin folder (e.g., `C:\Program Files\Java\jdk-21\bin`).

### Install Maven:
1. Locate the `Maven_Installer` folder in the resources.
2. Copy the `apache-maven` folder to `C:\Program Files`.
3. Add Maven to PATH:
   - In Environment Variables, add the path to Maven's `bin` folder (e.g., `C:\Program Files\apache-maven\bin`).

### Install Jackson:
1. Locate the `jackson_Installer` folder in the resources.
2. Copy the Jackson files to `C:\Program Files\Java`.
3. Add Jackson to PATH:
   - In Environment Variables, add the path to the Jackson files.

### Install JavaFX:
1. Locate the `JavaFX_Installer` folder in the resources.
2. Copy the `javafx-sdk` folder to `C:\Program Files\Java`.
3. Add JavaFX to PATH:
   - In Environment Variables, add the path to JavaFX's `bin` folder.

### Install MySQL:
1. Download and install MySQL Server 8.0.40 from the resources folder or the official MySQL website.
2. Follow the steps in the installation wizard:
   - Select “Server only” if no other MySQL components are needed.
   - Configure the server with a secure username and password.

### Configure MySQL:
1. Open MySQL Workbench or any other MySQL client.
2. Connect to the server using the credentials set during installation.
3. Create a new database and import the `db.sql` file from the resources folder.
4. Configure the `application.properties` file in the backend folder:
   - Replace the values with your database details, MySQL username, and password.

### Run the Application:
1. After completing the above steps, run the application using the provided executable.
2. If the application encounters issues, check the following:
   - The MySQL server is running.
   - The data in the `application.properties` file is correct.
   - Environment variables (Path) are set correctly.

## References
- Java SE Development Kit 21 Documentation, [Online]. Available: https://docs.oracle.com/en/java/javase/21/.
- Spring Boot Documentation, [Online]. Available: https://spring.io/projects/spring-boot.
- JavaFX Documentation, [Online]. Available: https://openjfx.io/.
- MySQL Documentation, [Online]. Available: https://dev.mysql.com/doc/.
- IEEE Conference Templates, [Online]. Available: https://www.ieee.org/conferences/publishing/templates.html.
- FasterXML, "Jackson Library Documentation," [Online]. Available: https://github.com/FasterXML/jackson.
- Apache Software Foundation, "Apache Maven Project Documentation," [Online]. Available: https://maven.apache.org/.
