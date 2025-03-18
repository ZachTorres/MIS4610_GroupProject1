# Group 7 - Project #1
## Team Name
21482 Group 7
## Team Members
Clay Campbell\
Karishma Pandit\
Anay Patel\
Matthew Schwanekamp\
Zachary Torres
## Problem Description
At the end of each month do you see that your sock supply has dwindled significantly? This is where Socks2Go comes in! We are an eCommerce sock subscription service. Our customers sign up and receive a box of socks each month. Our customers of the subscription will sign up and receive a box of socks each month depending on subscription tier. Our system tracks the subscription details, order histories, and inventory levels to ensure timely deliveries and customer satisfaction and the data we gather can be used to enhance the shopping experience by exploiting flaws providing valuable insights into customer trends.
## Data Model
Our data model is based on the hypothetical structure of a sock subscription service.

First, our central entity, entitled SockSubscriptionService, serves simply as a "placeholder" to connect all the different branches of entities in the rest of our model. Following our first branch, we then have the Department entity. As one company will have many departments, there is a one-to-many relationship established. From there, we have our Employee entity. As one department will have many employees but an employee can only be a part of one department, there is a one-to-many relationship between a department and an employee.

The next branch is the Supplier branch. As one company will have many suppliers, and, in this scenario, there are no external companies, there is a one-to-many relationship between them. Then, there is an entity entitled IncomingShipment that is meant to track any and all incoming shipments. As each individual supplier will send many shipments to the company, but each shipment can only be sent by one company, a one-to-many relationship is established.

The third branch concerns the company's actual physical inventory and some of its characteristics. First, there is an Inventory entity that simply tracks, by month, what socks are in storage. Each separate instance of an Inventory represents a different month of the year. Then, there is a design entity with a one-to-many relationship with Inventory whereby one inventory contains many designs. Finally, there is also a Promotion entity that keeps track of the different promotions that the company can have on different inventories. As one inventory can have multiple promotions associated with it, and one promotion can have multiple inventories associated with it, so an associative entity, InventoryPromotion, was created to track such relationships.

Our final branch concerns both our subscribers, their orders, and the shipments associated with such orders. First, the entity Distributor keeps track of each of the distributors associated with the company and their information. Then, the OutgoingShipment entity keeps track of the many shipments from each distributor. Separately, an entity, SubscriptionPlan, tracks the different kinds of plans, roughly equating to the number of socks each subscriber gets per month. Then, the entity Subscription, which has a one-to-many relationship with SubscriptionPlan, keeps track of each individual subscriber and their information. Finally, there is an entity, Order, that is associated with both OutgoingShipment and Subscription. Each order will have been made by a subscriber, so there is a one-to-many relationship between those two entities. However, each order is also a part of an OutgoingShipment, as it would be too difficult to try and ship each order individually. Thus, Order has another one-to-many relationship between itself and OutgoingShipment.

![Screenshot 2025-03-13 162337](https://github.com/user-attachments/assets/798def86-2cab-4e65-b422-1e348e74f3ee)
## Data Dictionary
![Table 1 Subscriber](https://github.com/user-attachments/assets/82f507b6-b604-41ad-9b75-8c9015b69c7c)
![Table 2 Subscription Plans](https://github.com/user-attachments/assets/a7a3e1d8-7046-4795-b7b4-f9af3ed69cab)
![Table 3 Orders](https://github.com/user-attachments/assets/c3821555-02ef-48bb-9c16-df272119ebb0)
![Table 4 Employee](https://github.com/user-attachments/assets/098407b2-dfa2-4e65-9d1c-ac0eeb95b0c2)
![Table 5 Department](https://github.com/user-attachments/assets/21546723-55a2-46ba-9bce-9bcf4d794453)
![Table 6 Supplier](https://github.com/user-attachments/assets/e670b81a-e2df-47d9-9d98-afac00d8381e)
![Table 7 Distributors-Partners](https://github.com/user-attachments/assets/19c60f3f-3054-40e8-9196-b2d9392a287c)
![Table 8 Incoming Shipments](https://github.com/user-attachments/assets/75b20861-62ab-48e3-9735-1604db9a9151)
![Table 9 Inventory](https://github.com/user-attachments/assets/8dc40695-5039-4f70-8b63-cb2e16e9b90d)
![Table 10 Promotions](https://github.com/user-attachments/assets/0428f714-eba2-4271-8e57-e6c4ac148d60)
![Table 11 Designs](https://github.com/user-attachments/assets/37cb7e35-7646-40c2-992c-2e600ae845ec)

## Queries

 1. QUERY 1 (Simple) - This query lists all the subscribers who started in February. This is helpful to a manager to first know if the number of new users is larger or smaller compared to other months. Additionally, this could be helpful for promotions for customers who have been around for a certain amount of months.

<img width="746" alt="Screenshot 2025-03-18 at 9 47 45 AM" src="https://github.com/user-attachments/assets/982302cd-6ab9-4732-b783-1357a57e974b" />


 2. QUERY 2 (Complex) - This query shows what people are spending more on average compared during January. This is helpful because January is typically a month where people dial back their purchasing after the holiday season, so people still purchasing more than our average customer could be targeted for our more high-end sock lines.

<img width="838" alt="Screenshot 2025-03-18 at 9 48 45 AM" src="https://github.com/user-attachments/assets/fd550654-3fa5-405c-9ad4-e1c62eaf5426" />


 3. QUERY 3 (Complex) - This query lists our subscription plans with more than 20 users. This is helpful to know which plans are doing well so we can double down and further meet these customers needs. 

<img width="679" alt="Screenshot 2025-03-18 at 9 49 24 AM" src="https://github.com/user-attachments/assets/f437dad7-cf2b-430f-9f7e-f99bb42d4523" />



 4. QUERY 4 (Complex): What query 4 does is put out the info of each subscription plan's name and price per month, then counts how many people are subscribed to each plan by counting active subscription , and then using that multiplies the numbers to calculate how much total revenue each plan brings in. Then it groups everything by the plan name and sorts the results in descending order (High to low) by total revenue.


<img width="1029" alt="Screenshot 2025-03-17 at 4 16 11 PM" src="https://github.com/user-attachments/assets/883cc6a3-0c35-405e-8879-ccb3f7572944" />

From this info we as a buisness can quickly see which subscription plans are the most popular by seeing subscription and along with that we can see which ones make the most money. This could guide and ultimatly influnce many decisions about marketing by pushing certain plans more, or adjustments to plan pricing by lowering the price of underperforming plans. 


 5. QUERY 5 (Complex): Query 5 adds up the total weight of all incoming shipments from that specifc supplier, and then uses groupby and having filters to only show those suppliers whose total shipped weight is greater than 10,500. After that, it sorts the list by the total weight shipped from smallest to largest and only displays the top two supplliers out of the 3 we currently have.


<img width="1028" alt="Screenshot 2025-03-17 at 4 16 29 PM" src="https://github.com/user-attachments/assets/84ccf8c1-7e48-48c5-8562-73f699b1815b" />

By being able to see which suppliers have shipped more than 10,500 pounds in weight it will help spot who our biggest suppliers are. By being able to see who of our suppliers are moving most of the product, we can see who our best suppliers and most important partners are. we can also see the suppliers who aren’t meeting that threshold, which could raise questions about their efficiency and question our choices.


 6. QUERY 6(Simple): What Query 6 does is display subscription ID, email, status, and start date for any subscription is currently Active” and started in 2024.


<img width="983" alt="Screenshot 2025-03-17 at 4 15 21 PM" src="https://github.com/user-attachments/assets/eaa30e9c-ae9f-417c-bbee-9c9ec613db7c" />

This data allows us to see the active subscriptions that started in 2024 which can give us visulization of how many subscribers we gained that year and whether they’re still around. using this information we can also add to this query to also see promotions that were used to see which ones we can reuse to increase our users.

7. QUERY 7 (Simple): This query calculates the total number of socks available in inventory by summing up the stockQuantity field.

![image](https://github.com/user-attachments/assets/f8f4b30a-b08d-46b1-8118-5e78117007c9)
   
Having a clear view of total inventory is critical for supply chain management. This query allows managers to track stock levels, ensuring that demand can be met without unnecessary overstocking. If the number is too low, they may need to order more supplies or adjust marketing efforts to avoid running out of stock. Conversely, if the number is too high, they might consider running promotions to move excess inventory.

8. QUERY 8 (Simple): This query retrieves a list of all employees along with their first name, last name, and department name by joining the Employee table with the Department table.

![image](https://github.com/user-attachments/assets/7dd67b7e-9c78-4715-afe0-4667ff67ceca)

Understanding the distribution of employees across departments is essential for workforce planning and resource allocation. Managers can use this query to assess staffing levels, ensure departments are adequately staffed, and make strategic hiring decisions. Additionally, HR can use this data to track internal mobility and optimize team structures.

9. QUERY 9 (Complex): This query retrieves a list of distributors along with the total number of outgoing shipments they have processed. It filters out distributors with 3 or fewer shipments and sorts the results in descending order.

![image](https://github.com/user-attachments/assets/b4cc124c-e228-4088-84cd-470be4d95dec)

Tracking the number of shipments handled by each distributor is essential for supply chain management and logistics planning. This query helps identify high-performing distributors that are actively handling large volumes, ensuring that operations run smoothly. It also highlights underperforming distributors, which may indicate inefficiencies or potential partnership risks that require further investigation.

10. QUERY 10 (Complex): This query retrieves information about distributors and the number of distinct regions they cover based on outgoing shipments. It selects the distributor ID and name, counts the unique destination addresses (regionsCovered) for each distributor, and filters the results to only include distributors who cover more than three regions. 

![image](https://github.com/user-attachments/assets/2642146a-e4c8-4d8e-933b-d2293561d1cd)

This information can be valuable for strategic decision-making, such as identifying strong partners for expanding market presence, optimizing supply chain logistics, and focusing on distributors who contribute significantly to the company's distribution network. Understanding which distributors cover the most regions can also aid in resource allocation and partnership prioritization.

## Database Information

CALL TP_Q1();
CALL TP_Q2();
CALL TP_Q4();
CALL TP_Q4();
CALL TP_Q5();
CALL TP_Q6();
CALL TP_Q7();
CALL TP_Q8();
CALL TP_Q9();
CALL TP_Q10();
