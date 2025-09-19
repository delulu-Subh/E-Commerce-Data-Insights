# E-Commerce-Data-Insights[superstore_analytics_dashboard.py](https://github.com/user-attachments/files/22421438/superstore_analytics_dashboard.py)
#!/usr/bin/env python
# coding: utf-8

# In[1]:


import pandas as pd
import matplotlib.pyplot as plt


# In[7]:


# Load CSVs
orders = pd.read_csv(r"C:\Users\User\OneDrive\Desktop\Orders database.csv")
customers = pd.read_csv(r"C:\Users\User\OneDrive\Desktop\Customer Database.csv")
products = pd.read_csv(r"C:\Users\User\OneDrive\Desktop\Product Database.csv")

# Merge them into one DataFrame
df = orders.merge(customers, on="CustomerID").merge(products, on="ProductID")

# Convert OrderDate to datetime (important for time-based charts)
df['OrderDate'] = pd.to_datetime(df['OrderDate'])

print(df.head())  # Check first 5 rows


# In[9]:


import matplotlib.pyplot as plt

# --------------------------
# CUSTOMER DASHBOARD
# --------------------------

# 1. Revenue by Region
customer_region = df.pivot_table(values="Sales", index="Region", aggfunc="sum").sort_values("Sales", ascending=False)
customer_region.plot(kind="bar", legend=False, title="Revenue by Region")
plt.ylabel("Revenue")
plt.show()



# In[11]:


# 2. Top 10 Customers by Revenue
top_customers = df.pivot_table(values="Sales", index="CustomerName", aggfunc="sum").sort_values("Sales", ascending=False).head(10)
top_customers.plot(kind="bar", legend=False, title="Top 10 Customers by Revenue")
plt.ylabel("Revenue")
plt.show()


# In[13]:


# 3. Customer Count per Region
cust_count = df.groupby("Region")["CustomerID"].nunique()
cust_count.plot(kind="pie", autopct='%1.1f%%', title="Customer Distribution by Region")
plt.ylabel("")
plt.show()


# In[15]:


# 4. Average Order Value per Customer
avg_order_value = df.groupby("CustomerName").apply(lambda x: x["Sales"].sum() / x["OrderID"].nunique()).sort_values(ascending=False).head(10)
avg_order_value.plot(kind="bar", title="Top 10 Customers by Avg Order Value")
plt.ylabel("Avg Order Value")
plt.show()


# In[17]:


# --------------------------
# PRODUCT DASHBOARD
# --------------------------

# 1. Revenue by Category
category_sales = df.pivot_table(values="Sales", index="Category", aggfunc="sum").sort_values("Sales", ascending=False)
category_sales.plot(kind="bar", legend=False, title="Revenue by Product Category")
plt.ylabel("Revenue")
plt.show()


# In[19]:


# 2. Revenue by Sub-Category
subcategory_sales = df.pivot_table(values="Sales", index="SubCategory", aggfunc="sum").sort_values("Sales", ascending=False).head(10)
subcategory_sales.plot(kind="bar", legend=False, title="Top Sub-Categories by Revenue")
plt.ylabel("Revenue")
plt.show()


# In[21]:


# 3. Profitability by Category
category_profit = df.pivot_table(values="Profit", index="Category", aggfunc="sum")
category_profit.plot(kind="bar", legend=False, title="Profit by Product Category")
plt.ylabel("Profit")
plt.show()


# In[23]:


# 4. Top 10 Products by Sales
top_products = df.pivot_table(values="Sales", index="ProductName", aggfunc="sum").sort_values("Sales", ascending=False).head(10)
top_products.plot(kind="bar", legend=False, title="Top 10 Products by Sales")
plt.ylabel("Revenue")
plt.show()


# In[25]:


# --------------------------
# ORDERS DASHBOARD
# --------------------------

# 1. Sales Trend over Time
sales_trend = df.pivot_table(values="Sales", index="OrderDate", aggfunc="sum").resample("M").sum()
sales_trend.plot(kind="line", title="Monthly Sales Trend")
plt.ylabel("Revenue")
plt.show()


# In[27]:


# 2. Order Volume over Time
order_trend = df.groupby("OrderDate")["OrderID"].nunique().resample("M").sum()
order_trend.plot(kind="line", title="Monthly Order Volume")
plt.ylabel("Orders")
plt.show()


# In[29]:


# 3. Sales vs Discount Scatter
df.plot(kind="scatter", x="Discount", y="Sales", alpha=0.5, title="Sales vs Discount")
plt.show()


# In[31]:


# 4. Profit vs Sales Scatter
df.plot(kind="scatter", x="Sales", y="Profit", alpha=0.5, title="Profit vs Sales")
plt.show()


# In[ ]:




