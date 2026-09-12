## Custom Objects

The HandsMen Threads Salesforce CRM project includes the following custom objects:

* **HandsMen Customer** – Stores customer-related information.
* **HandsMen Order** – Manages customer order information.
* **HandsMen Product** – Stores product details.
* **Inventory** – Manages inventory-related information.
* **Marketing Campaign** – Stores marketing campaign information.

## Lightning App

Created a Lightning App named **HandsMen Threads** to provide a centralized interface for the Salesforce CRM project.

### Navigation Items

* HandsMen Customer
* HandsMen Order
* Inventory
* HandsMen Product
* Reports
* Dashboard
* Account
* Contact
* Marketing Campaign

### User Profile

* System Administrator

### HandsMen Customer – Fields

* **Email** – Email field used to store the customer's email address.
* **Phone** – Phone field used to store the customer's phone number.
* **Loyalty Status** – Picklist field with the values: Gold, Silver, and Bronze.
  
## Object Relationships

The HandsMen Threads Salesforce CRM project includes the following object relationships:

* **Marketing Campaign → HandsMen Customer** – Lookup Relationship
* **HandsMen Product → HandsMen Order** – Lookup Relationship
* **HandsMen Order → HandsMen Customer** – Lookup Relationship
* **Inventory → HandsMen Product** – Master-Detail Relationship

