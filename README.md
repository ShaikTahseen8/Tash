Change Request Manager – Java + MongoDB (With Auto Sync Service)
A simple Java-based Change Request Management System that performs CRUD operations using MongoDB, and includes a background Sync Manager that periodically writes all change requests to a local file (sync_data.txt).
🚀 Features
✔ Add new Change Requests
✔ View all Change Requests
✔ Update existing Change Requests
✔ Delete requests by ID
✔ MongoDB persistence
✔ Auto-Sync service that runs every 60 seconds
✔ Writes synced data to sync_data.txt
✔ Clean DAO layer & Object-Document mapping
✔ Java console menu interface
📌 Project Structure
src/
 ├── com.changemanager
 │   ├── Main.java
 │   ├── dao/
 │   │     └── ChangeRequestDAO.java
 │   ├── model/
 │   │     └── ChangeRequest.java
 │   ├── sync/
 │   │     └── SyncManager.java
 │   └── util/
 │         └── MongoDBConnection.java
🛠 Technologies Used
Java 17+
MongoDB (local instance on localhost:27017)
MongoDB Java Driver
Threads / Runnable (Sync Manager)
FileWriter (data export)
⚙ Setup Instructions
1. Install MongoDB
Make sure MongoDB is running locally:
mongodb://localhost:27017
Database used: change_request_db
Collection created automatically: change_requests
2. Add MongoDB Java Driver
Use Maven or manually add JAR:
<dependency>
    <groupId>org.mongodb</groupId>
    <artifactId>mongodb-driver-sync</artifactId>
    <version>4.11.1</version>
</dependency>
3. Run the Application
Compile and run:
javac Main.java
java Main
🖥 How It Works
Main Menu
When you run the program:
1. Insert  
2. View All  
3. Update  
4. Delete  
0. Exit
🧩 Key Components
### 1️⃣ ChangeRequestDAO
Handles all MongoDB operations:
insert()
getAll()
getById()
update()
delete()
2️⃣ ChangeRequest Model

Represents a Change Request with fields:

title

description

status

priority

assignedTo


Includes mapping:

Java → MongoDB (toDocument())

MongoDB → Java (fromDocument())



---

3️⃣ SyncManager

Background thread that:

Runs every 60 seconds

Fetches all Change Requests

Writes them to sync_data.txt


Example entry:

ChangeRequest{id='65a1...', title='Bug Fix', status='Open', priority=2, assignedTo='John'}

📂 Output File (Sync Data)

A file named sync_data.txt is created/updated every minute.

🧪 Sample Usage

Insert Example:

Title: UI Bug
Description: Button not clickable
Status: Open
Priority: 2
Assigned To: Priya

View All Example:

ChangeRequest{id='675...', title='UI Bug', status='Open', priority=2, assignedTo='Priya'}

⚠ Common Issues

Issue	Solution

MongoDB connection error	Ensure MongoDB is running at localhost:27017
Invalid ID format	Use the exact MongoDB _id string
Sync thread not running	Check console for Sync completed: message

📝 Future Enhancements (Optional)

Add logging (Log4j/SLF4J)

Add GUI (JavaFX / Swing)

Add REST API layer (Spring Boot)

Add field validations

Add search/filter operations

🙌 Author

Change Management System – Java + MongoDB
Created for learning & academic use.

If you'd like, I can also generate:

✅ UML Diagram
✅ Class Diagram
✅ Architecture Diagram
✅ JavaDoc documentation
✅ GitHub-ready README with badges

Just tell me!Here is a clean, professional, well-structured README.md for your project.
You can copy-paste it directly into your repo.

Change Request Manager – Java + MongoDB (With Auto Sync Service)

A simple Java-based Change Request Management System that performs CRUD operations using MongoDB, and includes a background Sync Manager that periodically writes all change requests to a local file (sync_data.txt).

🚀 Features

✔ Add new Change Requests

✔ View all Change Requests

✔ Update existing Change Requests

✔ Delete requests by ID

✔ MongoDB persistence

✔ Auto-Sync service that runs every 60 seconds

✔ Writes synced data to sync_data.txt

✔ Clean DAO layer & Object-Document mapping

✔ Java console menu interface

📌 Project Structure

src/
 ├── com.changemanager
 │   ├── Main.java
 │   ├── dao/
 │   │     └── ChangeRequestDAO.java
 │   ├── model/
 │   │     └── ChangeRequest.java
 │   ├── sync/
 │   │     └── SyncManager.java
 │   └── util/
 │         └── MongoDBConnection.java

🛠 Technologies Used

Java 17+

MongoDB (local instance on localhost:27017)

MongoDB Java Driver

Threads / Runnable (Sync Manager)

FileWriter (data export)
⚙ Setup Instructions

1. Install MongoDB

Make sure MongoDB is running locally:

mongodb://localhost:27017

Database used: change_request_db

Collection created automatically: change_requests
2. Add MongoDB Java Driver

Use Maven or manually add JAR:

<dependency>
    <groupId>org.mongodb</groupId>
    <artifactId>mongodb-driver-sync</artifactId>
    <version>4.11.1</version>
</dependency>

3. Run the Application

Compile and run:

javac Main.java
java Main
🖥 How It Works

Main Menu

When you run the program:

1. Insert  
2. View All  
3. Update  
4. Delete  
0. Exit
🧩 Key Components

### 1️⃣ ChangeRequestDAO

Handles all MongoDB operations:

insert()

getAll()

getById()

update()

delete()

2️⃣ ChangeRequest Model

Represents a Change Request with fields:

title

description

status

priority

assignedTo

Includes mapping:

Java → MongoDB (toDocument())

MongoDB → Java (fromDocument())

3️⃣ SyncManager

Background thread that:

Runs every 60 seconds

Fetches all Change Requests

Writes them to sync_data.txt


Example entry:

ChangeRequest{id='65a1...', title='Bug Fix', status='Open', priority=2, assignedTo='John'}

📂 Output File (Sync Data)

A file named sync_data.txt is created/updated every minute.

🧪 Sample Usage

Insert Example:

Title: UI Bug
Description: Button not clickable
Status: Open
Priority: 2
Assigned To: Priya

View All Example:

ChangeRequest{id='675...', title='UI Bug', status='Open', priority=2, assignedTo='Priya'}

⚠ Common Issues

Issue	Solution

MongoDB connection error	Ensure MongoDB is running at localhost:27017
Invalid ID format	Use the exact MongoDB _id string
Sync thread not running	Check console for Sync completed: message

📝 Future Enhancements (Optional)

Add logging (Log4j/SLF4J)

Add GUI (JavaFX / Swing)

Add REST API layer (Spring Boot)

Add field validations

Add search/filter operations


