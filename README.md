# Event-Management-System
The Event Management System automates event processes, allowing exclusive control by administrator-like users who oversee event creation, user addition, and system management. With a user-friendly interface, secure authentication, and a structured database, it ensures seamless and efficient event management.

Features:
Login and Signup Classes
The Login and Signup classes manage user authentication and registration. User password credentials are securely hashed and stored in the User_tb table of the database using SecureData class of C#. Proper validation mechanisms are implemented to ensure data integrity using functions like IsNullOrEmpty, IsNullOrWhitespaces and Regex.

Main Class
The Main class serves as the main interface of the application. It displays a welcome note, a DataGrid to view available events, and buttons for registering new events, participants, and feedback. This class interacts with other classes to coordinate the flow of information and operations.

Event Class
The Event class handles the registration of new events. It collects event details such as name, date, and location, and stores them in the Event table of the database. Upon completion, it returns to the Main for a seamless user experience.

Participant Class
The Participant class manages participant registration. It includes a button to view all participants, allowing users to delete or update participant information. The class interacts with the database to maintain a record of participants associated with specific events.

All_Participant
This class shows a DataGrid which shows data of all participants from Participant table. We can search for a participant and delete and update it using the search value. It has a back button which takes us back to the participant registration window.

Feedback Class
The Feedback class enables users to provide feedback with star ratings for events. Feedback is stored in the Feedback table of the database. Past participants can provide feedback it uses EventID and PartID from other tables as Foreign key and these value must be available in those tables.
