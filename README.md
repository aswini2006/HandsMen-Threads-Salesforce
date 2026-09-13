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

## Formula Fields

### Inventory

* **Stock Status** – Formula field with Text return type.
* **Formula:** `IF(Stock_Quantity__c > 10, "Available", "Low Stock")`

## Remaining Fields

### HandsMen Customer

* **Total Purchases** – Number field used to store the customer's total purchases.

### HandsMen Product

* **SKU** – Text field used to identify the product.
* **Price** – Currency field used to store the product price.
* **Stock Quantity** – Number field used to store the available product quantity.

### HandsMen Order

* **Status** – Picklist with the values: Pending, Confirmed, and Rejection.
* **Quantity** – Number field used to store the order quantity.
* **Total Amount** – Number field used to store the total order amount.

### Inventory

* **Warehouse** – Text field used to store warehouse information.
* **Stock Quantity** – Number field used to track inventory quantity.

### Marketing Campaign

* **Start Date** – Date field used to store the campaign start date.
* **End Date** – Date field used to store the campaign end date.

### HandsMen Customer

* **FirstName** – Text field used for the customer's first name.
* **LastName** – Text field used for the customer's last name.
* **Full Name** – Formula field with Text return type.
* **Formula:** `FirstName__c + " " + LastName__c`

## Validation Rules

### HandsMen Order

* **Rule Name:** Total Amount
* **Field:** Total Amount
* **Validation Formula:** `Total_Amount__c <= 0`
* **Error Message:** Please Enter Correct Amount
* **Error Location:** Total Amount field

### Inventory

* **Rule Name:** Stock Quantity
* **Field:** Stock Quantity
* **Validation Formula:** `Stock_Quantity__c <= 0`
* **Error Message:** the inventory count is never less than zero.
* **Error Location:** Top of Page

### HandsMen Customer

* **Rule Name:** Email
* **Field:** Email
* **Validation Formula:** `NOT CONTAINS(Email, "@gmail.com")`
* **Error Message:** Please fill Correct Gmail
* **Error Location:** Top of Page

## Profile

### Platform 1

Created a custom profile named **Platform 1** by cloning the **Standard User** profile.

### Custom Object Access

Access was configured for:

* **HandsMen Product**
* **Inventory**
