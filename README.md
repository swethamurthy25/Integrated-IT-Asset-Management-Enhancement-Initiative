## $\textcolor{red}{Case\ Study\ on\ Integrated\ IT\ Asset\ Management\ Enhancement\ Initiatives}$

### $\textcolor{red}{Project\ Description}$
The "Integrated IT Asset Management Enhancement Initiative" serves as a pivotal endeavor within the organization's digital transformation and cost optimization strategy. This project is dedicated to elevating IT Asset Management (ITAM) to a state of meticulous precision, ensuring the tracking and reporting of asset value and ownership throughout their entire lifecycle. While substantial progress was achieved in the previous fiscal year, with the definition and implementation of IT asset procurement processes and standards, the upcoming phase is committed to addressing the Deploy, Service, and Retire stages of the IT Asset Management lifecycle.

### $\textcolor{red}{Problem\ Statement\ and\ Challenges}$
According to the recent audit report, IniTech Solutions is experiencing a problem with the present techniques for managing asset data which includes data duplication and mismanagement, visualization issues, and decentralized data models.

### $\textcolor{red}{Recommended\ Solution}$
To address the challenges faced by IniTech Solutions, the optimal solution involves developing a system that maintains a database of asset details, ensuring real-time updates. This system should include an asset portal with a dashboard, allowing users to both view allocated assets and submit requests for new ones, as advised by IT auditors.

### $\textcolor{red}{High\ Level\ Process\ Design}$

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/395f04ed-7855-4b00-b392-5490dadaf1ce)

### $\textcolor{red}{Network\ Topology\ (Infrastructure\ Diagram)}$

The network topology of the Initech system is divided into three layers: the presentation layer, the business layer, and the database layer. The presentation layer ensures that the communications it receives are formatted appropriately for the recipient application. In addition, the presentation layer serves as the user's and workers' first point of contact when they use the online application. It consists of desktop computers, laptop computers, and mobile devices that customers utilize to access the application. 

The proxy server is then used to perform two-factor authentication when a user or employee attempts to access the system. The proxy server acts as a firewall, preventing the attacker from gaining access to the private network. Any data entered by the user via the user interface must pass through the firewall to reach the business and database layers. This is because the firewall acts as the network security device that monitors and filters inbound and outbound network traffic by an organization's security policies. The organization’s whole network is secured with the help of a firewall.

The data that successfully gets through the firewall will be routed to the business logic layer which contains web servers in it. The Business Logic Layer manages the business rules, calculations, and logic that determines how an application should function. Here we have two web servers for stockroom management and asset management where the actual process of stockroom inventory management and the serialized asset tracking process happens. The database layer contains the repositories that encapsulate the logic required to access data sources. They centralize common data access functionality, providing better maintainability and decoupling the infrastructure or technology used to access databases from the domain model layer. Initech Solutions has a centralized data repository where we can store the most up-to-date information on asset records, stockroom management data, and so on.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/0dca7555-ecde-41bb-8cb2-6ca0dce10462)


### $\textcolor{red}{Data\ Modelling\ with\ ER\ Diagram}$

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


### $\textcolor{red}{Business\ Functions}$

#### Business Function 1 - Serialized Asset Tracking
A computerized asset management system can help with asset management, maintenance operations simplification, and project administration and planning. A centralized software solution that connects with existing systems to aggregate data collection from physical assets regardless of make, model, or manufacturer into one place. It also helps businesses expedite asset management and decrease human error. Additionally, businesses will gain complete asset visibility including location, status, and usage history, using a single web-based dashboard that enables quick search and tag filtering.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/ca47e5d4-ca52-489d-8440-75e8bb33e40d)

#### Business Function 2 - Stockroom Management
A serialized asset can be stored in a unique storage location defined by a building and room. An effective inventory management approach results in a well-organized stockroom management center. A well-organized warehouse improves the efficiency of present and future fulfillment strategies. This includes cost savings and improved product quality for companies that employ warehouses to manage inventories.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/34c57a9a-c9ea-4071-b228-6ec7288732dd)

#### Business Function 3 - ITAM Process
The request and fulfillment process is a management procedure that touches every other function since it requires data updates in the central repository once the request is reviewed by another team. Stakeholders have five primary functions.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/7b5792d6-776e-4d20-b4b0-126dc4f4d2b5)

#### Business Function 4 - Security Process
The goal of security management is to maintain high-level security in every function and separate the access of functions to various roles based on the stakeholder level of authority. This is done to ensure that the underlying sensitive data is kept as secure as possible.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/1b70827e-54ec-4c27-878e-6e76e4929430)


### $\textcolor{red}{User\ Interface\ Design}$

#### WireFrame 1 - Desktop-based GUI for Asset Management System (Security Process)
* First and foremost, when a client or an Initech employee attempts to log in to the company's website, they must choose their logging-in option via the user login page. * Then, for a safe and secure login, a login page with two-factor authentication is developed.
* To use Initech Solutions' services, every user must first create an account on InitechSolutions.com. Employees of Initech will be registered for the same.
* Following the completion of the registration process, the user will be directed to the login page.
* Upon successful login with a user ID and password, the user will be directed to the authentication page, where they will receive a unique code or OTP on their mobile 
  phones, which must be entered on the authentication page.
* Then the user will be able to visit the homepage of Initech Solutions after successfully logging in.
* From the home page, the user can navigate to the required sections (asset tracking, stockroom management, ITAM process, security).

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/1c9f5b6a-e55a-405e-b095-3e45c29728e3)

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/26b7849b-f6ff-4e07-b5d2-857018579431)

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/c3997d54-9d2a-4ef8-84e0-64b1aa8e8b8e)

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/ec80ceff-b262-426c-83ec-519d875413f5)

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/2ca85349-c5ed-4894-808a-f785c4dfe1b3)


#### WireFrame 2 - Asset Tracking Dashboard 
The asset tracking dashboard is a visual representation of the overall information in the serialized asset tracking process. The quantity of assets reflects the entire number of assets accessible for usage, whereas the purchase in the fiscal year shows the total amount spent on the asset in that year. The asset value for each day has been charted. In addition to this, the dashboard features feed sections that include the asset tag id and the asset's due date.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/20e4bd40-f149-4049-8635-e8f86e1dc10a)


### WireFrame 3 - Stockroom Management

The stock room management webpage has been designed to assist the user in gaining access to the stockrooms. Each stockroom is assigned unique identifiers. To have the access approved, users have to provide inputs such as unique identifier details, room number, building number, address, and security control options on the webpage. The security control options will be validated and if the physical key matches, the access will be approved. Once the access is approved, the user can be able to access the stockroom.  On the other hand, the access will be refused if the unique identifier information is inaccurate, or the physical key is not matched. In that case, the user has to contact the stockroom manager responsible for that particular stockroom in order to gain access.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/8961157a-dc3c-41fa-8487-6cd7e467f0a7)


### WireFrame 4 - ITAM Process - Asset Entry

All five processes in the ITAM process – asset entry, asset request, fulfillment process, support process, and asset retirement process have their own user interface. The asset entry user interface is used to enter asset data into the repository. The user must provide inputs such as the asset ID, asset name, asset model, asset location, and the details of the person to whom the asset is assigned. After providing all the required information, the user must select the update repository option to save the asset information to the repository, and this process should be repeated whenever the asset status or asset condition changes.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/acab8f16-58ea-446a-8206-0c7a290e51c0)


### Wireframe 5: ITAM Process - Asset Request

Employees will be able to submit a request to install equipment from a stock room via the request process. They can utilize the asset request user interface for this purpose. The employee must provide input data such as employee ID, employee name, project name, and preferred asset type (for example HP in our case). The details will be retrieved from the repository that matches the employee’s selection criteria, and a message will be displayed indicating whether he can proceed with the request. Then the user can proceed to submit the new request by clicking the submit request button. These access requests will be handled by the fulfillment team.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/12cd187d-a98c-42c9-82b2-e82920d6fdc6)

### Wireframe 6: ITAM Process – Asset Fulfillment Request

The technicians will be able to handle the asset request via the asset fulfillment user interface. This user interface will display the overall number of tickets (requests) to handle, as well as the open, pending, on-hold, and closed requests. The technician can view the request details by clicking on the request number, and he also has the authority to verify the asset status prior to processing the request. If the request fails to pass the asset status validation check, the user interface provides the option to deny the request.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/350da43f-afe5-4686-93c4-c107c3c870b6)


### Wireframe 7: ITAM Process – Support

The employee can submit the service requests for the support services like installation of software, replacement of hard drives or system refresh, through the user interface built for the support process. In the support user interface, the user must enter the employee ID, asset id, and phone number as input, and select asset status and issue/services from the dropdown menu. The user interface additionally includes a text area for describing the issue (add note section).

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/06e846f9-5ab3-4671-be0f-a8113cdbf003)

### Wireframe 8: ITAM Process – Asset Retirement

The asset retirement user interface assists the technician in the asset disposal maintenance When submitting the request, the user must include information such as the asset identification number, location of the asset, model name, asset owner data, asset status (disposal, retired, lost, damaged, or stolen), and asset submission date. Upon submitting the details, a notification is sent to the delivery team for asset collection along with the asset status,  and the details are updated in the repository.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/c2ab54a9-98f9-4d05-bd17-1b4caa748f3f)


### Wireframe 9: ITAM Process Dashboard

The various phases of the ITAM process have been displayed in a single dashboard. The asset entry pie chart depicts the total volume of asset types such as desktops, laptops, monitors, and servers. The asset request pie chart depicts the status and number of requests from different categories. In addition to that, the dashboard includes the week-wise fulfillment status in the form of a graph. The numbers of retired assets for the years 2020 and 2021 can also be viewed, along with the number of support requests resolved.

![image](https://github.com/swethamurthy25/Integrated-IT-Asset-Management-Enhancement-Initiative/assets/112581595/8527c452-a786-49e3-a8bc-0a091c157adc)



## References:

Tilley, S. R. (2020). Systems analysis and design. Cengage.




