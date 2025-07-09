# Blood-Bank-Management-System
This program implements a simple Blood Bank Management System using C++ object-oriented principles.

- The Blood Bank Management System is designed as an object-oriented C++ program
that simulates essential functions of a blood bank. The methodology involves defining
a BloodBank class that encapsulates the data and operations necessary to manage
blood inventories, donors, and blood requests. The program logic is organized into
several methods within this class to create a structured and modular approach.

- Data Structures and Initialization
- Blood Type and Inventory Arrays: The program uses arrays to store information
about blood types and their corresponding inventory quantities. Each blood type has
a specific index, and an array inventory is used to track the number of units available
for each type.

- Donor and Request Arrays: Arrays donors, donorBloodTypes, and requests store
the names of donors, their blood types, and blood type requests, respectively.

- Counters: Variables donorCount and requestCount track the number of registered
donors and the number of blood requests, ensuring efficient access to the next
available array position.

- Class Constructor
The BloodBank class constructor initializes donorCount and requestCount to zero,
setting the initial state of the system and preparing it for operation.

-  Methods for Key Operations
Each of the main operations—registering donors, requesting blood, viewing
inventory, listing donors, and viewing requests—is implemented as a method within
the BloodBank class. The methodology for each function is as follows:

- Donor Registration (registerDonor):
The method takes a donor’s name and blood type as input.
It verifies the blood type by checking against the bloodTypes array.

- If the blood type is valid, the donor’s details are added to donors and
donorBloodTypes, the inventory for that blood type is incremented, and donorCount
is updated.
If the blood type is invalid or if the donor list is full, appropriate error messages are
displayed.

- Blood Request Processing (requestBlood):
This method takes a blood type as input, validating it against the bloodTypes array.
If the requested blood type has units available in the inventory, it decreases the count
and adds the blood type to requests, incrementing requestCount.

- If the blood type is unavailable or invalid, it displays an error message.
- Viewing Inventory (viewInventory):
This method iterates over bloodTypes and inventory arrays, displaying the quantity
of each blood type.
It allows the user to see the available stock of each blood type in real time.

- Viewing Registered Donors (viewDonors):
This method iterates through the donors array and displays the name and blood type
of each donor.
If no donors are registered, it displays a message stating that there are no donors.

- Viewing Blood Requests (viewRequests):
Similar to the viewDonors method, this method iterates through requests to display
each blood type that has been requested.
If no requests are recorded, it displays a message indicating this.

-  User Interface and Interaction
A main() function contains a menu-driven interface that continuously prompts the
user to select an option from the list (register donor, request blood, view inventory,
view donors, view requests, or exit).
Based on the user’s choice, the corresponding method of the BloodBank class is
called.
- The main() function also handles basic input validation by ensuring that only valid
menu choices trigger a response and displays an error for invalid choices.

- Validation and Constraints
Blood Type Validation: Both the registerDonor and requestBlood methods include
a validation step to ensure the blood type is among the eight recognized types.

- Capacity Limits: The system imposes a limit on the number of donors and requests
that can be registered (100 each) based on the fixed-size arrays. Error messages
inform the user if capacity is reached.

- Inventory Checks: Blood requests are processed only if there are available units in
inventory, preventing negative counts and ensuring realistic behavior.

- Error Handling and Feedback
The system provides feedback through messages that inform users of successful
registrations, requests, and inventory updates.
Error messages are displayed if a user attempts to register an invalid blood type,
request unavailable blood, or exceed the donor/request limit
