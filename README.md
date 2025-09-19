Thank you for sharing the additional images! These charts further enhance your Superstore Analytics Dashboard by providing a broader view of the data. I’ve updated the GitHub README to incorporate all the provided visualizations, assigning filenames based on their titles for consistency. You can upload these images to an `images` folder in your repository and update the paths if needed. Below is the revised README:

---

# Superstore Analytics Dashboard

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-1.5+-yellow.svg)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7+-orange.svg)
![HTML](https://img.shields.io/badge/HTML-5-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

A comprehensive analytics dashboard for a superstore's e-commerce data, featuring a Python backend for data processing and visualization, and an HTML-based frontend for interactive insights. The project analyzes customer behavior, product performance, and order trends to support data-driven business decisions.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Visualizations](#visualizations)
- [Frontend Interface](#frontend-interface)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
This project provides a dual-component analytics dashboard for a superstore dataset:
- **Backend (Python)**: Uses Pandas for data processing and Matplotlib for generating visualizations from three CSV files (`Orders`, `Customers`, `Products`).
- **Frontend (HTML)**: Displays interactive insights through a web interface with sections for home, customers, products, and orders.

The dashboard uncovers insights into revenue, customer distribution, product categories, order trends, and profitability, enabling stakeholders to optimize strategies and identify growth opportunities.

## Features
- **Backend Analysis**:
  - Merges and processes order, customer, and product data.
  - Generates 12 visualizations covering customer, product, and order metrics.
- **Frontend Interface**:
  - Interactive dashboard with navigation for Home, Customers, Products, and Orders.
  - Key metrics (e.g., total revenue, customer count, order volume) and insights.
- Built with **Pandas** and **Matplotlib** for backend processing and **HTML/CSS** for frontend display.

## Dataset
The Python backend uses three CSV files:
- **Orders Database** (`Orders_database.csv`): Contains `OrderID`, `CustomerID`, `ProductID`, `OrderDate`, `Sales`, `Profit`, and `Discount`.
- **Customer Database** (`Customer_Database.csv`): Includes `CustomerID`, `CustomerName`, and `Region`.
- **Product Database** (`Product_Database.csv`): Contains `ProductID`, `ProductName`, `Category`, and `SubCategory`.

**Note**: Update file paths in `superstore_analytics_dashboard.py` if CSVs are not in `C:\Users\User\OneDrive\Desktop\`.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/superstore_analytics_dashboard.git
   cd superstore_analytics_dashboard
   ```
2. Install Python dependencies:
   ```bash
   pip install pandas matplotlib
   ```
3. Ensure Python 3.8+ is installed.
4. For the frontend, ensure the HTML files (`index.html`, `customers.html`, `orders.html`, `products.html`) are in the project directory. No additional setup is required for the static HTML frontend.

## Usage
1. **Backend (Python)**:
   - Place the CSV files in the specified directory or update the file paths in `superstore_analytics_dashboard.py`.
   - Run the script to generate visualizations:
     ```bash
     python superstore_analytics_dashboard.py
     ```
   - The script outputs 12 charts (bar, pie, line, scatter) for customer, product, and order analytics.
2. **Frontend (HTML)**:
   - Open `index.html` in a web browser to view the main dashboard.
   - Use the sidebar to navigate to `customers.html`, `orders.html`, or `products.html` for specific insights.
   - The frontend displays static metrics and placeholders for charts (link to Python-generated visuals or replace with actual images).

## Visualizations
The Python backend generates the following charts:

### Customer Dashboard
1. **Top 10 Customers by Average Order Value**: Bar chart showing customers with the highest average order values.
   - ![Top 10 Customers by Average Order Value]

<img width="1000" height="600" alt="top_customers_aov" src="https://github.com/user-attachments/assets/12eb13ef-89d5-46a4-a60a-a33b66343862" />

2. **Top 10 Customers by Sales**: Bar chart of customers with the highest total sales.
   - ![Top 10 Customers by Sales]

<img width="1000" height="600" alt="top_customers_sales" src="https://github.com/user-attachments/assets/aac0adb3-3ee1-4a4c-a855-421a0f88b2aa" />

### Product Dashboard
1. **Sales by Category**: Bar chart of total sales across product categories.
   - ![Sales by Category]
   - <img width="800" height="600" alt="sales_by_category" src="https://github.com/user-attachments/assets/d43e6ca0-c55c-4779-984c-9f5c9fd94544" />
2. **Top 10 Products by Sales**: Bar chart of the best-selling products.
   - ![Top 10 Products by Sales]
   - <img width="1000" height="600" alt="top_products_sales" src="https://github.com/user-attachments/assets/6fccb695-4fad-4fb4-9c56-5fa6c5434695" />
3. **Profit by Category**: Bar chart showing profitability across categories.
   - <img width="800" height="600" alt="profit_by_category" src="https://github.com/user-attachments/assets/aec41b63-09f1-451d-a97b-c24282305fc5" />
### Orders Dashboard
1. **Orders by Region**: Bar chart of order distribution across regions.
   - ![Orders by Region]
   - <img width="800" height="600" alt="orders_by_region" src="https://github.com/user-attachments/assets/035d8c50-d9aa-46e1-8ea2-f9a05dc119ed" />
2. **Orders by Category**: Bar chart of order volume across product categories.
   - ![Orders by Category]
   - <img width="800" height="600" alt="orders_by_category" src="https://github.com/user-attachments/assets/57588f34-9bae-4f23-b8a7-468b920ff8c3" />
3. **Profit by Region**: Bar chart of profit contribution by region.
   - <img width="800" height="600" alt="profit_by_region" src="https://github.com/user-attachments/assets/d50b18e4-dd14-4af2-8b9f-85d69efc8f38" />
4. **Discount vs Profit**: Scatter plot analyzing the impact of discounts on profit.
   - ![Discount vs Profit]
   - <img width="800" height="600" alt="discount_vs_profit" src="https://github.com/user-attachments/assets/95dbe26c-f716-46ee-9012-8750af148167" />
5. **Monthly Orders Trend**: Line chart of order volume over time.
   - ![Monthly Orders Trend]
   - <img width="1000" height="600" alt="monthly_orders_trend" src="https://github.com/user-attachments/assets/a5ce11fd-87a5-4487-b9e1-acb69b85d976" />
6. **Monthly Sales Trend**: Line chart of sales over time.
   - <img width="1000" height="600" alt="monthly_sales_trend" src="https://github.com/user-attachments/assets/cecbcea6-77c8-41db-95b2-299dbb68c1e3" />
## Frontend Interface
The HTML frontend provides an interactive dashboard with four pages:
- **Home (`index.html`)**: Displays key metrics (e.g., $120,000 revenue, 500 customers) and placeholders for charts like Monthly Sales Trend, Orders by Category, and Profit by Region.
- **Customers (`customers.html`)**: Shows metrics (e.g., 500 customers, $25,000 top customer revenue) and insights for top customers by revenue and AOV.
- **Products (`products.html`)**: Highlights metrics (e.g., 300 products, Technology as top category) and insights for top products, revenue, and profitability.
- **Orders (`orders.html`)**: Presents metrics (e.g., 1,000 orders, December as peak month) and insights for order trends and regional performance.

*Example Frontend Screenshot*:  
![Dashboard Home](images/dashboard_home.png) <!-- Replace with actual screenshot -->

## Contributing
1. Fork the repository.
2. Create a branch (`git checkout -b feature-branch`).
3. Commit changes (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request.
---

### Notes
- **Images**: The README now includes specific filenames for each chart (e.g., `sales_by_category.png`, `top_10_customers_by_aov.png`, etc.) based on their titles. Upload these images to an `images` folder in your GitHub repository. If the filenames differ, adjust the paths accordingly.
- **Missing Images**: The `dashboard_home.png` placeholder remains. Take a screenshot of the `index.html` page and upload it to replace this placeholder.
- **File Paths**: Ensure the CSV file paths in `superstore_analytics_dashboard.py` match your setup, or include the files in the repository.
- **Frontend Integration**: The HTML files are assumed to be static. To dynamically link these charts, you’d need a web framework (e.g., Flask) to serve the images, but for now, they’re referenced as static assets.
