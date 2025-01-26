# Super Store Sales Analyses

This project, conducted by Nthabiseng and Mafube, focuses on analyzing the Super Store's data to uncover hidden patterns and generate valuable insights. As a prominent retail establishment, the Super Store holds a wealth of information that can be leveraged to enhance its operations and strategic decision-making.

The primary objective is to identify meaningful trends and actionable insights within the data, providing a comprehensive blueprint to optimize sales strategies, improve performance, and ensure sustained success for the Super Store.

# Description
This project focuses on exploring an extensive sales dataset using advanced analytical tools and methodologies. The goal is to discover valuable insights hidden within the data. Key areas of analysis include examining sales trends, identifying top-performing products, and calculating critical revenue metrics such as total sales and average revenue per order.

Beyond the numbers, these findings will be translated into engaging visualizations, ensuring they effectively communicate insights and drive informed decisions among stakeholders.
For your GitHub readme, you can introduce the Superstore dataset by explaining the significance of each feature. Here's how you might approach it:

---

## Features of the Superstore Dataset

The **Superstore** dataset contains various attributes related to sales transactions. 

- **Row ID**: A unique identifier for each row in the dataset.
- **Order ID**: A unique identifier for each order placed, helping to track individual sales transactions.
- **Order Date**: The date when the order was placed, allowing for trend analysis over time.
- **Ship Date**: The date when the order was shipped.
- **Ship Mode**: The method of shipping used for the order.
- **Customer ID**: A unique identifier for each customer, used to track customer purchases and preferences.
- **Customer Name**: The name of the customer who placed the order, useful for segmentation and personalized marketing.
- **Segment**: Classifies customers into different groups (e.g., Consumer, Corporate, Home Office), which helps in analyzing customer behavior across segments.
- **Country**: The country where the customer is located, allowing for regional analysis of sales and performance.
- **City**: The city where the customer resides, providing insight into local market trends and targeting.
- **State**: The state or province where the customer is located, useful for more granular regional analysis.
- **Postal Code**: The postal code associated with the customer's delivery address, helping with geographic segmentation and delivery logistics.
- **Region**: Broad geographic classification (e.g., East, West, etc.), aiding in performance comparison across larger areas.
- **Product ID**: A unique identifier for each product, used to track and analyze product-level sales data.
- **Category**: The high-level classification of products (e.g., Furniture, Office Supplies), useful for market trend analysis.
- **Sub-Category**: A more specific classification under the Category (e.g., Chairs, Binders), providing deeper insights into product performance.
- **Product Name**: The name of the product, which identifies specific items within the store’s inventory.
- **Sales**: The monetary value of each sale, crucial for measuring revenue and understanding product performance.
- **Quantity**: The number of items sold in each order, useful for inventory management and sales volume analysis.
- **Discount**: The discount applied to the order, which can affect profitability and sales strategies.
- **Profit**: The profit made from each sale, essential for evaluating business profitability and product pricing strategies.

---

## Normalizarion

1. **Customers and Orders**:
   - **Relationship**: One-to-many (one customer can have multiple orders).
   - **Purpose**: This relationship tracks which customer placed which orders. It allows for the organization of order history for each customer and facilitates customer service, billing, and marketing efforts based on their purchase history.

2. **Orders and Order Details**:
   - **Relationship**: One-to-many (one order can have many items).
   - **Purpose**: This relationship breaks down an order into individual items (order details), including the product category, quantity, and pricing details. It helps in analyzing which products are most commonly ordered, understanding sales patterns, and managing inventory.

3. **Categories and Order Details**:
   - **Relationship**: Many-to-one (many order details can belong to one category).
   - **Purpose**: This allows for tracking of order items within specific product categories. It helps in categorizing sales and analyzing trends based on product categories, which is useful for inventory management, marketing, and sales reporting.

4.  **Products and Subcategories**:
   - **Relationship**: Many-to-one (many products belong to one subcategory).
   - **Purpose**: This relationship allows for the classification of products into specific subcategories. It helps in organizing and categorizing products based on more specific characteristics within a larger category. This is useful for product discovery, inventory management, and targeted marketing campaigns.

5. **Categories and Subcategories**:
   - **Relationship**: One-to-many (one category can have multiple subcategories).
   - **Purpose**: This relationship allows a category to be divided into multiple subcategories, enabling more detailed classification of products. This is beneficial for businesses that sell products across a wide range of types, making it easier to group them into smaller, more specific subcategories for better organization and customer experience.


6. **Delivery Addresses and Orders**:
   - **Relationship**: One-to-one (one order has one delivery address).
   - **Purpose**: This ensures that each order has a unique address to which it will be delivered. It enables effective order fulfillment and tracking of shipping details for each customer.

7. **Countries and Delivery Addresses**:
   - **Relationship**: One-to-many (one country can have multiple delivery addresses).
   - **Purpose**: This relationship links each delivery address to a country. It helps in determining the shipping origin, calculating shipping costs, and complying with regional shipping rules.

8. **States and Cities**:
   - **Relationship**: One-to-many (one state can have multiple cities).
   - **Purpose**: This allows cities to be grouped under specific states, which is useful for identifying regional trends, managing regional sales operations, and addressing legal or logistical requirements that vary by state.

9. **States and Countries**:
   - **Relationship**: Many-to-one (many states can belong to one country).
   - **Purpose**: This relationship connects states to their respective country, ensuring proper geographic categorization. It is useful for managing operations like taxation, regional policies, and shipping constraints specific to a country’s states.

10. **Cities and States (or Countries)**:
   - **Relationship**: One-to-many (one state can have many cities).
   - **Purpose**: This ensures that each city is correctly categorized within its state or country. It aids in organizing city-specific information for logistical purposes like shipping, customer service, or tax calculations.
11. **Customers and Segments**:
   - **Relationship**: One-to-one (each customer belongs to exactly one segment).
   - **Purpose**: Customers are classified into distinct segments based on specific attributes . By grouping customers into segments, businesses can target marketing, sales strategies, and customer service efforts to specific customer types.

12. **Customers and Customer Segments (Bridge Table)**:
   - **Relationship**: The `customer_segments` table is used to link a customer to a segment. Since a customer belongs to only one segment, this table simplifies the overall design by using a bridge approach while avoiding redundancy.
   - **Purpose**: This bridge table serves as a clean way to link customers to their segments without repeating customer data in the `segments` table. It simplifies the structure by acting as a reference between customers and segments, providing clear, normalized data.
---

### Summary of Purposes:
- **Customer and Order Tracking**: The relationships allow businesses to manage orders placed by customers, track their order histories, and analyze purchasing patterns.
- **Product and Category Management**: These relationships help businesses categorize and analyze products, making it easier to manage inventory, sales reporting, and marketing strategies.
- **Shipping and Delivery**: The delivery address and country relationships enable effective logistics management, ensuring orders are delivered to the correct locations with accurate shipping costs.
- **Geographic Structure**: The state, city, and country relationships allow businesses to operate efficiently across different regions, taking into account regional rules, shipping constraints, and customer preferences.
- **Product and Subcategory**: One subcategory can contain many products, but each product belongs to only one subcategory. This helps in organizing products into smaller groups within broader categories.
- **Category and Subcategory**: One category can have multiple subcategories, enabling a more granular classification of products. This helps businesses to manage complex product assortments and allows customers to easily navigate a broad range of products
![Untitled (1)](https://github.com/user-attachments/assets/8f91720c-fc31-409c-a486-46c079cd27db)

## Facts about the store dataset


