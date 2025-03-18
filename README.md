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
At the end of each month do you see that your sock supply has dwindled significantly? This is where Socks2Go comes in! We are an eCommerce sock subscription service. Our customers sign up and receive a box of socks each month.
## Data Model
![Screenshot 2025-03-13 162337](https://github.com/user-attachments/assets/798def86-2cab-4e65-b422-1e348e74f3ee)
## Data Dictionary

## Queries

 1. QUERY 1 (Simple)


<img width="729" alt="Screenshot 2025-03-17 at 4 10 52 PM" src="https://github.com/user-attachments/assets/13e5fcd9-0759-43e5-a0da-9fb938d2e577" />

 2. QUERY 2 (Complex)


<img width="975" alt="Screenshot 2025-03-17 at 4 13 50 PM" src="https://github.com/user-attachments/assets/f61e2304-00fc-47b8-b000-91ac90229c10" />

 3. QUERY 3 (Complex)


<img width="671" alt="Screenshot 2025-03-17 at 4 16 05 PM" src="https://github.com/user-attachments/assets/8240e82d-86cc-4503-b3ad-174123f8419e" />

 4. QUERY 4 (Complex): What query 4 does is put out the info of each subscription plan's name and price per month, then counts how many people are subscribed to each plan by counting active subscription , and then using that multiplies the numbers to calculate how much total revenue each plan brings in. Then it groups everything by the plan name and sorts the results in descending order (High to low) by total revenue.


<img width="1029" alt="Screenshot 2025-03-17 at 4 16 11 PM" src="https://github.com/user-attachments/assets/883cc6a3-0c35-405e-8879-ccb3f7572944" />

From this info we as a buisness can quickly see which subscription plans are the most popular by seeing subscription and along with that we can see which ones make the most money. This could guide and ultimatly influnce many decisions about marketing by pushing certain plans more, or adjustments to plan pricing by lowering the price of underperforming plans. 


 5. QUERY 5 (Complex): Query 5 adds up the total weight of all incoming shipments from that specifc supplier, and then uses groupby and having filters to only show those suppliers whose total shipped weight is greater than 10,500. After that, it sorts the list by the total weight shipped from smallest to largest and only displays the top two supplliers out of the 3 we currently have.


<img width="1028" alt="Screenshot 2025-03-17 at 4 16 29 PM" src="https://github.com/user-attachments/assets/84ccf8c1-7e48-48c5-8562-73f699b1815b" />

By being able to see which suppliers have shipped more than 10,500 pounds in weight it will help spot who our biggest suppliers are. By being able to see who of our suppliers are moving most of the product, we can see who our best suppliers and most important partners are. we can also see the suppliers who aren’t meeting that threshold, which could raise questions about their efficiency and question our choices.


 6. QUERY 6(Simple)


<img width="983" alt="Screenshot 2025-03-17 at 4 15 21 PM" src="https://github.com/user-attachments/assets/eaa30e9c-ae9f-417c-bbee-9c9ec613db7c" />

## Database Information
