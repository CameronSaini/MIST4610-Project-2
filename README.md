# MIST4610 Group Project 2

Team Name: DELETE FROM UGA_football_team WHERE PlayerName = 'Carson Beck';

# Team Members:

Miles Cohall [@fromj50](https://github.com/fromj50)

Lucas Ramos [@jlr97647](https://github.com/jlr97647)

Cameron Saini [@cameronsaini](https://github.com/CameronSaini)

Hitanshi Shah [@hshah56](https://github.com/hshah56)

Tyler Martin [@tjm44974](https://github.com/tjm44794)

# Problem Description:

Our team was tasked with designing a comprehensive database for a construction project management firm. Continuing with the foundation that we had built in our first project, we opted to slightly modify our data model. Originally, our data model placed a central focus on the contractors entity. However, we realized that our data model offered lackluster insight into the projects themselves. We created two new entities, a budgets table and an invoices table. The budgets entity allows us to track where each individual project stands in terms of spending. Additionally, our new invoices entity ensures transparent financial tracking between contractors, owners, et cetera. Acknowledging these new elements, along with the elements already described and justified in project one, our database allows the firm to streamline operations and improve collaboration amongst involved parties. 

# Data Model:

This data model represents a construction project management system, organizing key aspects such as property ownership, project details, financials, tasks, permits, and supplier relationships. At its core, land_property represents properties with attributes like location, size, and value, linked to owners, who may own multiple properties. Projects are the central entity, tracking details such as start and end dates, status, and ownership. Each project connects to supporting entities like budgets (tracking financials), invoices (billing records), project_tasks (specific activities within projects), and permits (regulatory compliance).


The model includes contractors, capturing details about companies or individuals working on projects, with a many-to-many relationship managed through the projects_ has_contractors table. Similarly, suppliers provide materials and are linked to projects via the supplier_has_projects table. Architecture_firms and their associated building_plans represent design work for projects.


Key relationships include one-to-many links, such as between land_property and owners or projects and their related budgets, project_tasks, invoices, and permits. Many-to-many relationships, like those between projects and contractors or suppliers, are managed through associative tables. Overall, the model provides a streamlined structure for managing construction projects, ensuring all resources, stakeholders, and compliance requirements are integrated efficiently.

<img width="711" alt="Screenshot 2024-12-03 at 5 24 13 PM" src="https://github.com/user-attachments/assets/29a824a6-d6ff-4899-b36a-1b475889185f">

# Data Dictionary:
<img width="686" alt="image" src="https://github.com/user-attachments/assets/4e631302-0dbb-438d-908b-3801f05336fd">
<img width="707" alt="image" src="https://github.com/user-attachments/assets/3a639874-7767-4a57-a529-40e12c8536ca">
<img width="692" alt="image" src="https://github.com/user-attachments/assets/fb76dfcd-b8ba-4a7d-adf3-76fe1539144a">
<img width="680" alt="image" src="https://github.com/user-attachments/assets/e4ea761c-f35f-4ddd-81fe-3d2347a212b4">
<img width="685" alt="image" src="https://github.com/user-attachments/assets/17b757df-0466-4f58-b700-054dfdc815e9">
<img width="660" alt="image" src="https://github.com/user-attachments/assets/a814c26d-98ce-47bc-a92e-ba5ab71a80b4">
<img width="667" alt="image" src="https://github.com/user-attachments/assets/3437daa6-7638-40f6-b316-e02b93c45fc6">
<img width="677" alt="image" src="https://github.com/user-attachments/assets/d26b7224-1b96-4102-bf65-4d1dd570389d">
<img width="664" alt="image" src="https://github.com/user-attachments/assets/151c5198-ab43-4a0d-859a-5f8497a79cad">
<img width="678" alt="image" src="https://github.com/user-attachments/assets/dd917e78-6fab-4031-9108-25edc8429bc7">
<img width="670" alt="image" src="https://github.com/user-attachments/assets/03374abd-a7b0-4d2a-8b8b-e0de2c17e095">
<img width="666" alt="image" src="https://github.com/user-attachments/assets/1eab4346-4b69-4bf9-b4b1-b6de986d2871">
<img width="682" alt="image" src="https://github.com/user-attachments/assets/51c75a23-b3d7-4528-999c-90eac8ac8e0e">
<img width="667" alt="image" src="https://github.com/user-attachments/assets/5daa64a0-b7f1-4c12-be9f-0548dc3b7673">
<img width="675" alt="image" src="https://github.com/user-attachments/assets/925519c5-a1b8-46bb-9c46-ce4c2c0531b6">
<img width="654" alt="Screen Shot 2024-12-03 at 7 52 01 PM" src="https://github.com/user-attachments/assets/dfb26367-e986-42c1-96d7-dd9c4fb4249d">
<img width="499" alt="Screen Shot 2024-12-03 at 7 50 29 PM" src="https://github.com/user-attachments/assets/9eb2a61c-33fa-4c1b-a64d-f343822982c6">

# Queries:

<img width="700" alt="Screen Shot 2024-12-03 at 10 47 12 PM" src="https://github.com/user-attachments/assets/0a1b6071-0b0a-4222-ae4e-efc677511090">

**Query 1:**
This query identifies the top five suppliers in terms of their total budget (their cumulative budget distributed amongst all projects linked to each respective supplier). It highlights which suppliers are the “biggest players” in terms of the firm’s operations. This can help us in many ways, such as optimizing costs and highlighting which suppliers we may want to negotiate with or ensure future collaboration with.

<img width="627" alt="Screenshot 2024-12-03 at 5 16 04 PM" src="https://github.com/user-attachments/assets/d91068b4-3324-43c2-9e46-b5485e5049a3">

**Query 2:**
This query highlights the top three contractors with the most overdue tasks in terms of total overdue duration (calculated in total days). It  helps project managers identify and address if and which contractors may pose a risk to any project timelines. This enables them to make decisions accordingly. By focusing on the most critical issues, it ensures efficient resource management and improved accountability.


<img width="628" alt="Screenshot 2024-12-03 at 5 16 41 PM" src="https://github.com/user-attachments/assets/38c63f14-89d2-4191-8e2a-71d71a71767a">

**Query 3:**
This query will enable us to view which contractors are taking on the heaviest workload with regards to tasks. Now, with the breakdown of tasks into active and overdue tasks, we have far better insight as to where we may be able to reallocate our resources in an effort to operate more effectively as a firm. Additionally, we can proactively monitor performance and make decisions based on that. 

<img width="626" alt="Screenshot 2024-12-03 at 5 17 02 PM" src="https://github.com/user-attachments/assets/9dacb63a-809c-46c9-89bb-d907125440f7">

**Query 4:**
This breakdown of the total payments made to each contractor helps bring cost transparency and also assists the managers in monitoring the financial outlays made, observing the compliance of the organization with audit requirements, and providing a clear audit trail for financial statements. Furthermore, it helps in the management of resources by assessing, for managers, whether the budgets are too spread out, if any of the contractors are overstepping the expected cost, and whether the total of invoices is within the set budget for that specific project.

<img width="627" alt="Screenshot 2024-12-03 at 6 26 18 PM" src="https://github.com/user-attachments/assets/e0985dba-3e0f-4619-a695-420076935071">

**Query 5:**
The question pinpoints projects that have been completed with a remaining cost no greater than 20% of the original cost and serves as an early indicator for managers on how to take some corrective action to eliminate the potential risks. Such corrective measures may include adjustment to allocation of resources, or even seeking more funding. Additionally, arranging the results based on the hue of the remaining budget also assists in ensuring that the managers focus on the projects most in danger of being abandoned.

<img width="625" alt="Screenshot 2024-12-03 at 6 26 48 PM" src="https://github.com/user-attachments/assets/83d44521-552c-475f-8c2f-4b26d04f4d74">


# Visualizations

**Visualization 1:**
This graph shows the owner of each property along with the property’s location and lot size. Since larger plots generally mean larger projects, management can use this information to plan out large projects. For larger sites, site preparation, budgeting, and resource allocation are extensive, so more planning needs to be done. Management can allocate a contractor that deals with large scale projects to these clients to ensure everything runs smoothly

**Property Details**

<img width="1029" alt="Screenshot 2024-12-03 at 5 44 07 PM" src="https://github.com/user-attachments/assets/57d054ca-aefc-4f57-b14a-eac26665f4d7">

**Visualization 2:**
This graph shows management the projects that are currently in progress along with the project’s spent budget and total budget, grouped by the contractor in charge of each project. This is important to management so they can alert each contractor how their budget is doing and if any budget cuts need to occur. Also, if a project were to be over budget, management could investigate why that occurred.

**Budget and Financials**

<img width="1021" alt="Screenshot 2024-12-03 at 5 46 25 PM" src="https://github.com/user-attachments/assets/1c5baab3-43c8-4f3b-aae1-8bff017b37ce">

**Visualization 3:**
It shows management how many projects are planned for each contractor. With this information, management could better divide the work so that efficiency is maximized. Some projects currently planned for Legacy Contractors, FutureBuild Solutions, and Platinum Contractors could be given to contractors with fewer projects. This way, an equal amount of work could be done by each contractor, maximizing efficiency. In turn, the contractors with fewer projects won't be wasting time sitting around doing nothing while the contractors with a lot of projects have to carry the load.

**Contractor Load**

<img width="1225" alt="Screenshot 2024-12-03 at 5 47 22 PM" src="https://github.com/user-attachments/assets/81eb64e1-ebed-4d69-bca4-56ef4832c5fb">

# Database Information

Name of the database: cs_tjm44794

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
