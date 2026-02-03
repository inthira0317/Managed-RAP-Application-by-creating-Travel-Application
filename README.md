# Managed-RAP-Application-by-creating-Travel-Application
***We will implement a simple travel provider app that can be used to manage flight bookings. A single travel should be  booked by the travel provider for an existing customer through a travel agency and include one or multiple flight bookings.***


In this case you can see the customer one is the travel provider and travel agency. we will plan a trip and book for customer through travel provider in real time like<ins> makemytrip</ins> and travel agency such as airasia andn indigo .

*They entered the booking detail , supplementry detail what the customer wants after the process they will save in the back end and approved by the travel agency .*

Two different views of the travel app.


1.Processor :- creates individual travel instances, creates and manages individual flights and adds supplements to flight bookings.

2.Approver :- Verfication of the recorded travel data entered by the processor.

>[!IMPORTANT]
>/DMO/Travel is the root entity.There can be n number of bookings and n number of supplements I need some extra services like particular food in flight. 
>It is the composition relationship between the travel , the booking and the supplement entries where the travel entity represents roots of the data model.
> [!NOTE]
> This project is built using the **Managed RAP (RESTful ABAP Programming Model)**, where all transactional behavior is controlled by the framework via the root entity.

> [!TIP]
> Always create and modify **Booking** and **Supplement** entities through the **Travel root entity (`/DMO/Travel`)** to ensure data consistency and lifecycle control.

> [!IMPORTANT]
> `/DMO/Travel` is the **root entity**.  
> Bookings and Supplements are **composition child entities** and **cannot exist independently**.

> [!WARNING]
> Direct manipulation of child entities outside the Travel context may lead to **inconsistent data** and **RAP runtime errors**.

> [!CAUTION]
> Deleting a **Travel** instance will automatically delete all related **Bookings** and **Supplements** due to the **composition relationship**.
_________________________________________________________________________________________________

*We have the three entity and we will create one business object by putting the  /DMO/TRAVEL , /DMO/BOOKING , /DMO/BBOKINGSUPPLEMENT WE WILL START WITH THE TRAVEL NOT ONLY WE HAVE THIS M TRANSACTIONAL DATA these all are the transactional data table also on top of the master data table  we have to create the interface view and we need CDS VIEWS  and that we have to utilize
in the transactional table and master data table so we get the extra information like*

* /DMO/TRAVEL_M
* /DMO/BOOKING_M
* /DMO/BOOKINGSUPPL_M

  **THESE ARE THE PERSISTENT TABLE WHERE THE DATA WILL BE SAVED**








