# Restaurant Order Management System

## Project Overview

The **Restaurant Order Management System** is a Salesforce-based CRM application developed to manage restaurant operations and related activities in a centralized and efficient manner.

The system manages **Restaurants, Customers, Menu Items, Orders, Tables, Payments, Deliveries, and Chefs**. Salesforce automation, Apex, and Lightning Web Components are used to reduce manual work, maintain data accuracy, and improve the overall restaurant management process.

## Objectives

- Manage restaurant and restaurant-related information in a centralized system.
- Manage customers and their orders.
- Manage menu items, categories, prices, and availability.
- Manage restaurant tables and seating information.
- Create and track customer orders.
- Track order status from placement to delivery.
- Manage order-related payments.
- Assign delivery partners and track delivery status.
- Manage chef information and specialties.
- Automate business processes using Salesforce Flow.
- Implement custom business logic using Apex.
- Provide interactive functionality using Lightning Web Components.
- Generate reports and dashboards for restaurant analysis.
- Maintain data accuracy and security.

## Technologies Used

- Salesforce Lightning Platform
- Salesforce Custom Objects
- Salesforce Standard Objects
- Salesforce Flow
- Apex
- Apex Trigger
- Batch Apex
- Scheduled Apex
- Lightning Web Components (LWC)
- Salesforce Reports
- Salesforce Dashboards
- Salesforce Validation Rules
- Salesforce Record Types
- Salesforce Schema Builder

## Data Model

### Standard Objects

- **Account** – Restaurant
- **Contact** – Customer

### Custom Objects

- **Menu Item**
- **Order**
- **Table**
- **Payment**
- **Delivery**
- **Chef**

### Relationships

- Account → Menu Item
- Contact → Order
- Table → Order
- Order → Payment
- Order → Delivery
- Chef → Menu Item

## Menu Management

The **Menu Item** object is used to manage restaurant menu information.

It includes:

- Menu Item Name
- Category
- Price
- Availability Status
- Restaurant
- Chef

### Menu Categories

- Starters
- Main Course
- Desserts
- Beverages

### Availability Status

- Available
- Out of Stock

## Order Management

The **Order** object is used to maintain customer order information.

It includes:

- Order Number
- Customer
- Order Date
- Order Type
- Order Status
- Total Amount
- Table

### Order Types

- Dine-In
- Takeaway
- Online

### Order Statuses

- Placed
- Preparing
- Ready
- Delivered
- Cancelled

## Table Management

The **Table** object manages restaurant table information.

It includes:

- Table Number
- Seating Capacity
- Table Status

### Table Statuses

- Available
- Occupied
- Reserved

Table numbers are configured to be unique to avoid duplicate table records.

## Payment Management

The **Payment** object is used to track payments associated with restaurant orders.

It includes:

- Order
- Payment Date
- Payment Method
- Amount
- Payment Status

### Payment Methods

- Cash
- Card
- UPI

### Payment Statuses

- Paid
- Pending

## Delivery Management

The **Delivery** object manages order delivery information.

It includes:

- Restaurant Order
- Delivery Partner
- Delivery Date
- Delivery Status

### Delivery Statuses

- Assigned
- Out for Delivery
- Delivered

## Chef Management

The **Chef** object stores information about restaurant chefs.

It includes:

- Chef Name
- Employee ID
- Phone
- Specialty

### Chef Specialties

- South Indian
- North Indian
- Chinese
- Continental

## Validation Rules

The project implements validation and data-integrity controls for:

- Menu Item Price must be greater than zero.
- Payment Amount must be greater than zero.
- Order Date cannot be a future date.
- Delivery Date cannot be earlier than the Order Date.
- Table Number must be unique.
- Duplicate active orders for the same table are prevented.

Active orders are considered orders with the following statuses:

- Placed
- Preparing
- Ready

## Record Types

### Order Record Types

- Dine-In
- Takeaway
- Online

### Payment Record Types

- Cash Payment
- Digital Payment

## Automation

The project uses **Salesforce Flow** for:

- Creating customer orders.
- Processing payments.
- Automatically setting newly created orders to **Placed**.
- Automatically setting completed payments to **Paid**.
- Automatically updating the related order when a delivery is marked **Delivered**.
- Generating daily order summary information.
- Sending delayed delivery notifications.
- Generating daily sales reports for the Restaurant Manager.

## Apex Implementation

The project includes the following Apex components:

- **OrderDuplicateActiveTrigger** – prevents duplicate active orders for the same table.
- **DailyRestaurantSalesBatch** – processes today's orders and calculates daily restaurant sales.
- **DailyOrderConfirmationScheduler** – processes daily orders and sends order confirmation emails.
- **DeliveryReminderScheduler** – identifies delayed deliveries and sends delivery reminder notifications.

## Lightning Web Components

The project includes the following LWC components:

### Restaurant Dashboard

Provides information about:

- Today's Orders
- Daily Revenue

### Order Management

Provides:

- Place Order
- View Order Status

### Payment

Provides:

- Process Payment
- View Payment History

### Delivery

Provides:

- Assign Delivery Partner
- Track Delivery Status

These components provide an interactive interface for managing important restaurant operations.

## Reports

The following Salesforce reports were created:

- Daily Orders Report
- Sales Report
- Menu Item Sales Report
- Payment Report
- Delivery Report
- Customer Order Report
- Pending Orders Report
- Completed Deliveries Report
- Top Selling Menu Items Report

These reports provide operational and analytical information about orders, customers, payments, deliveries, sales, and menu items.

## Dashboard

The **Restaurant Dashboard** provides a centralized view of key restaurant performance information.

It includes:

- Total Orders
- Total Customers
- Daily Revenue
- Pending Orders
- Completed Deliveries
- Top Selling Menu Items

The dashboard helps restaurant management monitor important business information from a single interface.

## Security

The project implements Salesforce security features to protect restaurant data.

The major security configurations include:

- Organization-Wide Defaults configured as **Private**.
- Role hierarchy for restaurant operations.
- System Administrator profile.
- Restaurant Manager profile.
- Cashier profile.
- Chef profile.
- Delivery User profile.

### Roles

- Admin
- Restaurant Manager
- Cashier
- Chef
- Delivery Executive

## Testing

The project was tested using different business scenarios, including:

- Creating a customer order.
- Automatically setting an order status to Placed.
- Preventing invalid menu item prices.
- Preventing invalid payment amounts.
- Preventing future order dates.
- Preventing duplicate active orders.
- Processing payments.
- Automatically setting payment status to Paid.
- Assigning delivery partners.
- Updating delivery status.
- Automatically updating the related order when delivery is completed.
- Processing daily sales using Batch Apex.
- Testing scheduled notification processes.

The implemented functionality was tested successfully in the Salesforce Developer Edition environment.

## Project Features

- Restaurant Management
- Customer Management
- Menu Item Management
- Table Management
- Order Management
- Payment Tracking
- Delivery Management
- Chef Management
- Order Status Automation
- Payment Status Automation
- Delivery Status Automation
- Duplicate Active Order Prevention
- Data Validation
- Scheduled Notifications
- Apex-based Business Logic
- Interactive LWC Components
- Reports and Dashboards
- Role-Based Security

## Project Screenshots

Screenshots of the working Salesforce application, including the following components, are included in the project documentation:

- Salesforce Data Model / Schema Builder
- Menu Item Management
- Order Management LWC
- Payment LWC
- Delivery LWC
- Restaurant Dashboard LWC
- Salesforce Flows
- Apex Trigger and Classes
- Salesforce Reports
- Restaurant Dashboard
- Security and Role Hierarchy

## Learning Outcomes

Through this project, I gained practical experience in **Salesforce administration and development**, including:

- Salesforce data modelling
- Standard and custom objects
- Lookup relationships
- Custom fields
- Validation rules
- Record Types
- Salesforce Flow
- Screen Flows
- Record-Triggered Flows
- Scheduled Flows
- Apex programming
- Apex Triggers
- Batch Apex
- Scheduled Apex
- Lightning Web Components
- Salesforce Reports
- Salesforce Dashboards
- Salesforce security and role management

The project also improved my problem-solving, debugging, testing, documentation, and application-development skills.

## Future Scope

The system can be further enhanced by integrating:

- Order Item / Order Line management
- Menu-item selection while placing orders
- Shopping cart functionality
- Online payment gateways
- Customer-facing online ordering
- Email and SMS notifications
- Real-time delivery tracking
- Mobile application support
- Inventory and ingredient management
- Advanced sales analytics
- AI-based menu recommendations
- Integration with mapping and external delivery services

## Project Type

**Individual Salesforce Project**

## Developed By

**[Your Name]**

## Platform

**Salesforce**
