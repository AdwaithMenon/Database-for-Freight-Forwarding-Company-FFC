# **Database-for-Freight-Forwarding-Company-FFC**

## **Project Description**

### **Business Context**

The organization that we have considered is a freight forwarding company. The name of our freight 
forwarder company is FFC. A freight forwarding company facilitates shipments of goods / materials 
between two parties ,i.e exporter and importer. The goods are shipped in containers in large carrier ships 
(also known as vessels) from the port of loading to the port of destination. The freight forwarder is 
responsible for documentation, inward & outward movement of goods, and handoffs.

### **Scope**

We have only considered exports of sea consignments for the purpose of this project. The customer in the 
current scope is the Exporter. The words “customer” and “exporter” have been used interchangeably in 
the project description. For this project, The FFC’s scope ends once the estimated time of arrival (ETA) at 
the destination has been updated to the exporter.

### **Key Assumptions & Business Rules**

**Note:** There are gaps in the AS-IS process and some of the below mentioned business rules and 
assumptions have not been incorporated in the AS-IS process - these are the gaps we want to address in 
our TO-BE process. However, to avoid redundancy, we have listed all relevant applicable assumptions 
and rules. All of these assumptions and business rules are incorporated in the proposed TO-BE 
process.The Enhanced ERD is based on the following rules & assumptions.

1. The customer lead is received online through the website only.
2. The customer has to fill up the online query form before getting accounted in the database.
3. All the necessary documents required for shipping have to be provided by the customer online 
through the website portal.
4. Customers can submit the query without providing any document. However, this delays the 
process of shipping. Since the shipment document (See item 13 & 14 below) can only be 
prepared on the basis of the packing list provided by the customer.
5. Customer leads are processed in the FIFO (First In First Out) method. 
6. On receiving the customer lead, the sales executive opens the case (Case Status = Open) and 
assigns a case id.
7. A shipment refers to goods or cargo that are shipped together. The words “shipment” and 
“consignment” are used interchangeably in this project.
8. Shipments (consignments) are transported (shipped) in containers.
9. One consignment can be shipped in one or more containers. However, every container can be 
associated with one and only one consignment.
10. Containers are kept in the shipping vessels owned by shipping lines. A shipping line can have 
zero or more shipping vessels. Each vessel can be owned by one and only shipping line.
11. Each customer can have zero or more shipments. However, each shipment will be associated with 
one and only one customer.
12. Each consignment will be associated with one and only one shipping line. One shipping line can 
have zero or more consignments.
13. Each shipment will be carried on one and only one vessel and each vessel can carry one or more 
consignments.
14. A freight forwarding company issues a shipping document (referred as Bill of Lading henceforth) 
(B/L) to the exporter. The B/L contains the name of the port of loading, port of discharge, cargo 
description, cargo weight, cargo volume, number of packages, container id, and the name of 
exporter. One B/L can include one or more containers. A container can have one and only one 
B/L
15. An exporter provides a packing list for a consignment to help freight forwarding company 
prepare the (B/L). The packing list contains the number of packages, cargo weight, cargo volume, 
INCO terms and cargo description.
16. One shipment can have one or more packing lists combined. However, each packing list can be 
associated with one and only one shipment.
17. Each vessel can carry one or more containers. But each container will be linked to one and only 
one vessel.
18. One B/L can have one or more packing lists combined. However, each packing list can be 
associated with one and only one B/L.
