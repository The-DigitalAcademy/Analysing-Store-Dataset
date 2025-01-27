# Analysing The Super Store Orders Dataset

This project is developed by [Mafube Mokone](https://github.com/Mafube) and [Nthabiseng Mathabatha](https://github.com/agnesnthabi)

# Super Store Sales Analyses

This project, conducted by Nthabiseng and Mafube, focuses on analyzing the Super Store's data to uncover hidden patterns and generate valuable insights. As a prominent retail establishment, the Super Store holds a wealth of information that can be leveraged to enhance its operations and strategic decision-making.

The primary objective is to identify meaningful trends and actionable insights within the data, providing a comprehensive blueprint to optimize sales strategies, improve performance, and ensure sustained success for the Super Store.

# Description
This project focuses on exploring an extensive sales dataset using advanced analytical tools and methodologies. The goal is to discover valuable insights hidden within the data. Key areas of analysis include examining sales trends, identifying top-performing products, and calculating critical revenue metrics such as total sales and average revenue per order.

Beyond the numbers, these findings will be translated into engaging visualizations, ensuring they effectively communicate insights and drive informed decisions among stakeholders.


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
- [Mafube Mokone](https://github.com/Mafube)

![Untitled (1)](https://github.com/user-attachments/assets/ba6626dd-e940-4cbe-af28-223c00b7ab46)

1. **Customers and Orders**:
   - **Relationship**: One-to-many (one customer can have multiple orders).
   - **Purpose**: This relationship tracks which customer placed which orders.

2. **Orders and Order Details**:
   - **Relationship**: One-to-many (one order can have many items).
   - **Purpose**: This relationship breaks down an order into individual items (order details), including the product category, quantity, and pricing details. 

3. **Categories and Order Details**:
   - **Relationship**: Many-to-one (many order details can belong to one category).
   - **Purpose**: This allows for tracking of order items within specific product categories. 

4.  **Products and Subcategories**:
   - **Relationship**: Many-to-one (many products belong to one subcategory).
   - **Purpose**: This relationship allows for the classification of products into specific subcategories.
     
5. **Categories and Subcategories**:
   - **Relationship**: One-to-many (one category can have multiple subcategories).
   - **Purpose**: This relationship allows a category to be divided into multiple subcategories, enabling more detailed classification of products. 

6. **Delivery Addresses and Orders**:
   - **Relationship**: One-to-one (one order has one delivery address).
   - **Purpose**: This ensures that each order has a unique address to which it will be delivered.

7. **Countries and Delivery Addresses**:
   - **Relationship**: One-to-many (one country can have multiple delivery addresses).
   - **Purpose**: This relationship links each delivery address to a country.
   - 
8. **States and Cities**:
   - **Relationship**: One-to-many (one state can have multiple cities).
   - **Purpose**: This allows cities to be grouped under specific states.

9. **States and Countries**:
   - **Relationship**: Many-to-one (many states can belong to one country).
   - **Purpose**: This relationship connects states to their respective country, ensuring proper geographic categorization.

10. **Cities and States (or Countries)**:
   - **Relationship**: One-to-many (one state can have many cities).
   - **Purpose**: This ensures that each city is correctly categorized within its state or country.
     
11. **Customers and Segments**:
   - **Relationship**: One-to-one (each customer belongs to exactly one segment).
   - **Purpose**: Customers are classified into distinct segments based on specific attributes .

12. **Customers and Customer Segments (Bridge Table)**:
   - **Relationship**: The `customer_segments` table is used to link a customer to a segment. Since a customer belongs to only one segment, this table simplifies the overall design by using a bridge approach while avoiding redundancy.
   - **Purpose**: This bridge table serves as a clean way to link customers to their segments without repeating customer data in the `segments` table.
---

## Facts about the store dataset

---
## Analyzing the dataset
**1. For Executives, Sales Teams, and Business Intelligence.**

**Sales Performance.**

- Which product categories or subcategories generate the highest and lowest sales and profits?
- Are there specific regions or markets where sales consistently outperform others, and why?
- How does the discount percentage correlate with profit margins across different product categories?


