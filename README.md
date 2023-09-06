# Integrated-IT-Asset-Management-Enhancement-Initiative

## Project Description:

The "Integrated IT Asset Management Enhancement Initiative" serves as a pivotal endeavor within the organization's digital transformation and cost optimization strategy. This project is dedicated to elevating IT Asset Management (ITAM) to a state of meticulous precision, ensuring the tracking and reporting of asset value and ownership throughout their entire lifecycle. While substantial progress was achieved in the previous fiscal year, with the definition and implementation of IT asset procurement processes and standards, the upcoming phase is committed to addressing the Deploy, Service, and Retire stages of the IT Asset Management lifecycle.

## Problem Statement

According to the recent audit report, IniTech Solutions is experiencing a problem with the present techniques for managing asset data which includes data duplication and mismanagement, visualization issues, and decentralized data models.

## Technology Solution

To resolve IniTech Solutions' crisis, it would be best to create a system where a database of asset information is stored and updated in real-time and can be viewed in an asset portal, on whose dashboard users can submit requests for assets that have already been allocated or request for a new asset, as recommended by IT auditors.


## High-Level Process Design

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/395f04ed-7855-4b00-b392-5490dadaf1ce)


## Network Topology (Infrastructure Architecture)

The network topology of the Initech system is divided into three layers: the presentation layer, the business layer, and the database layer. The presentation layer ensures that the communications it receives are formatted appropriately for the recipient application. In addition, the presentation layer serves as the user's and workers' first point of contact when they use the online application. It consists of desktop computers, laptop computers, and mobile devices that customers utilize to access the application. 

The proxy server is then used to perform two-factor authentication when a user or employee attempts to access the system. The proxy server acts as a firewall, preventing the attacker from gaining access to the private network. Any data entered by the user via the user interface must pass through the firewall to reach the business and database layers. This is because the firewall acts as the network security device that monitors and filters inbound and outbound network traffic in accordance with an organization's security policies. The organization’s whole network is secured with the help of a firewall.

The data that successfully gets through the firewall will be routed to the business logic layer which contains web servers in it. The Business Logic Layer manages the business rules, calculations, and logic that determines how an application should function. Here we have two web servers for stockroom management and asset management where the actual process of stockroom inventory management and the serialized asset tracking process happens. The database layer contains the repositories that encapsulate the logic required to access data sources. They centralize common data access functionality, providing better maintainability and decoupling the infrastructure or technology used to access databases from the domain model layer. Initech Solutions has a centralized data repository where we can store the most up-to-date information on asset records, stockroom management data, and so on.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/0dca7555-ecde-41bb-8cb2-6ca0dce10462)


## Entity Relationship Diagram

The ER Diagram has six entities: 

### Employee
The employee table consists of various attributes that are associated with every employee who works for IniTech Solutions. The attributes of employee table are Emp_ID, Dept_ID, Asset_ID, Emp_Name, Emp_DOB, Email_id, and Emp_Address. Here, Emp_ID acts as a primary key that has no NULL value. Dept_ID and Asset_ID act as the foreign keys. Employee entity has one to many relationships with asset entity.

### Department
The department entity includes attributes like Dept_ID (name of the department) and the branch ID (branch name). Dept_ID acts as the primary key here, which has no NULL value. Department entity has one to many relationships with employee entities because one department might have many employees in it.

### Vendor
The vendor entity includes attributes like Vendor_ID, Asset _ID, Transaction_Amount , Invoice_Number, and Date_of _Purchase. Here, Vendor_ID acts as a primary key which has no NULL value and Asset_ID acts as a foreign key. The vendor entity has many to many relationships with the asset entity.

### Stockroom
The stockroom entity includes attributes like StockroomID, Assset_ID, Stock_room_contact, and Stock_room_Address. The StockroomID acts as the primary key and Asset_ID acts as the foreign key. The stock room entity has one to one relationship with the asset manager.

### Asset Manager
The asset manager entity includes attributes like Emp_ID, Stockroom_ID, Asset_ID, and Date_Worked_on_Asset. Here, the Emp_ID acts as the primary key which has no NULL value, and Asset_ID and Stockroom_ID act as a foreign key. The asset manager entity has one to one-to-one relationship with the stockroom, this is because one asset manager will be in charge of one stockroom. 

### Asset
The asset entity includes attributes like Asset_ID, Asset_Status, Stockroom_ID , Asset_Model , Asset_Condition , Vendor_ID, Asset_Location_ID, and Asset_Price. Here, Asset_ID acts as the primary key which has no NULL value. Stockroom_ID and Vendor_ID act as foreign keys. The asset entity has a many-to-one relationship with the stockroom entity because many assets can be placed in one stockroom. 

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/3d22d78a-3edc-404f-9c20-fe4f78b4c304)


## Business Functions

### Business Function 1 - Serialized Asset Tracking

A computerized asset management system can help with asset management, maintenance operations simplification, and project administration and planning. A centralized software solution that connects with existing systems to aggregate data collection from physical assets regardless of make, model, or manufacturer into one place. It also helps businesses expedite asset management and decrease human error. Additionally, businesses will gain complete asset visibility including location, status, and usage history, using a single web-based dashboard that enables for quick search and tag filtering.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/ca47e5d4-ca52-489d-8440-75e8bb33e40d)

### Business Function 2 - Stockroom Management

A serialized asset can be stored in a unique storage location defined by a building and room. An effective inventory management approach results in a well-organized stockroom management center. A well-organized warehouse improves the efficiency of present and future fulfillment strategies. This includes cost savings and improved product quality for companies that employ warehouses to manage inventories.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/34c57a9a-c9ea-4071-b228-6ec7288732dd)

### Business Function 3 - ITAM Process

The request and fulfillment process is a management procedure that touches every other function since it requires data updates in the central repository once the request is reviewed by another team. Stakeholders have five primary functions.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/7b5792d6-776e-4d20-b4b0-126dc4f4d2b5)

### Business Function 4 - Security Process

The goal of security management is to maintain high-level security in every function and separate the access of functions to various roles based on the stakeholder level of authority. This is done to ensure that the underlying sensitive data is kept as secure as possible.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/1b70827e-54ec-4c27-878e-6e76e4929430)


