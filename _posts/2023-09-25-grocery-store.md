---
layout: post
author: Noah Chaffin 
category: jekyll-update 
image: /assets/images/grocery_hope.png
---

In this post, I will outline my ER diagram and schema for an online grocery shopping web application.  


<!-- <img src="/assets/images/grocery_hope.png">    -->

![Test](https://raw.githubusercontent.com/NoahChaffin123/blog/refs/heads/master/assets/images/grocery_new_flow.png)


<!-- INside curly brackets, type in URL, need some ruby translation. Relative URL liquid Jekyll -->

For my ER diagram, my goal was to visualize how the entities were going to interact with each other, and how they interacted with each other. Each entity had a multitude of attributes, but there was one of them had: an ID. I included this into the ER diagram because I knew this would be important in my schema. 

The overall link between my entities says this: A customer account (which contains a phone number, account ID, and address) will place an order, which has a time, date, ID, special instructions, a quantity desired, and the option of delivery or pickup. This order will contain items, and each different item has a manufacturer, quantity available, price, a name, and an ID. In the case that an item is out of stock, there are substitute items that can be used to replace the original item. 


<img src="/assets/images/Grocery_Store_Data_Model-2023-09-25_22-02.png">
<!-- ![](/assets/images/Grocery_Store_Data_Model-2023-09-25_22-02.png "Schema") -->

In my schema, I have four tables: customer, order, ordering, and item. For the most part, the columns are basic things that are copied from the ER diagram, such as phone numbers or the name of an account owner. The primary keys, however, were a different story. In my customer, order, and item table, the primary key was the ID. This made it where the "order" table could successfully link the items and customer together using their respective IDs. The "ordering" table allows a customer to choose a specific amount of an item and whether or not they want a substistute item if the item they want is missing