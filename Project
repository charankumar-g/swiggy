## 🥡 Swiggy Restaurant Data Exploration – SQL Project 

### 📌 Project Overview

This SQL-based project explores a mock Swiggy restaurant dataset, analyzing restaurant distributions, ratings, costs, cuisines, and more. It is designed to showcase strong SQL skills through various queries on demo data.

> ✅ **Note**: The dataset used is a *demo* and not extracted from Swiggy directly.

---
###📁 Dataset Link: [Download from Google Drive](https://drive.google.com/file/d/19qpIadbJC4SNROoeDXFbUlfdFPGP7R6U/view?usp=sharing)

### 📁 Dataset Fields

`restaurant_name`, `city`, `cuisine`, `rating`, `menu_category`, `price`, `cost_per_person`, `veg_or_nonveg`

---

### 🔍 SQL Queries Used

#### 1. Count of Highly Rated Restaurants (> 4.5)
```sql
SELECT COUNT(DISTINCT restaurant_name) AS highest_rated_restaurants 
FROM restaurants 
WHERE rating > 4.5;
```

#### 2. City with the Highest Number of Restaurants
```sql
SELECT COUNT(DISTINCT restaurant_name) AS restaurant_count, city 
FROM restaurants 
GROUP BY city 
ORDER BY restaurant_count DESC 
LIMIT 1;
```

#### 3. Restaurants with "Pizza" in Their Name
```sql
SELECT COUNT(DISTINCT restaurant_name) AS restaurant_with_name_pizza 
FROM restaurants 
WHERE restaurant_name LIKE '%pizza%';
```

#### 4. Most Common Cuisine
```sql
SELECT cuisine, COUNT(*) AS most_common_cuisine 
FROM restaurants 
GROUP BY cuisine 
ORDER BY most_common_cuisine DESC 
LIMIT 1;
```

#### 5. Average Rating per City
```sql
SELECT city, AVG(rating) AS average_rating 
FROM restaurants 
GROUP BY city;
```

#### 6. Highest Priced Recommended Item by Restaurant
```sql
SELECT DISTINCT restaurant_name, MAX(price) AS highest_priced_item 
FROM restaurants 
WHERE menu_category = 'Recommended' 
GROUP BY restaurant_name 
ORDER BY highest_priced_item DESC;
```

#### 7. Top 5 Expensive Restaurants (Any Cuisine)
```sql
SELECT restaurant_name, MAX(cost_per_person) AS expensive_restaurant 
FROM restaurants 
GROUP BY restaurant_name 
ORDER BY expensive_restaurant DESC 
LIMIT 5;
```

#### 8. Top 5 Expensive Restaurants (Excluding Indian Cuisine)
```sql
SELECT restaurant_name, MAX(cost_per_person) AS expensive_restaurant 
FROM restaurants 
WHERE cuisine <> 'INDIAN' 
GROUP BY restaurant_name 
ORDER BY expensive_restaurant DESC 
LIMIT 5;
```

#### 9. Restaurants Costlier Than Average
```sql
SELECT restaurant_name, AVG(cost_per_person) AS avg_cost 
FROM restaurants 
GROUP BY restaurant_name 
HAVING avg_cost > (SELECT AVG(cost_per_person) FROM restaurants);
```

#### 10. Duplicate Restaurants (Same Name in Multiple Cities)
```sql
SELECT restaurant_name, city, cost_per_person, rating 
FROM restaurants 
GROUP BY restaurant_name, city 
HAVING COUNT(restaurant_name) > 1;
```

#### 11. Average Cost Per Person by Restaurant
```sql
SELECT restaurant_name, AVG(cost_per_person) AS avg_cost 
FROM restaurants 
GROUP BY restaurant_name;
```

#### 12. Cuisine-Wise Restaurant Count
```sql
SELECT cuisine, COUNT(*) AS cuisine_count 
FROM restaurants 
GROUP BY cuisine 
ORDER BY cuisine_count DESC;
```

#### 13. City-Wise Restaurant Count
```sql
SELECT city, COUNT(DISTINCT restaurant_name) AS restaurant_count 
FROM restaurants 
GROUP BY city 
ORDER BY restaurant_count DESC;
```

#### 14. City with the Highest Average Rating
```sql
SELECT city, AVG(rating) AS average_rating 
FROM restaurants 
GROUP BY city 
ORDER BY average_rating DESC 
LIMIT 1;
```

#### 15. Most Expensive Menu Item Overall
```sql
SELECT restaurant_name, price, menu_category 
FROM restaurants 
ORDER BY price DESC 
LIMIT 1;
```

#### 16. Veg vs Non-Veg Item Count
```sql
SELECT veg_or_nonveg, COUNT(*) AS total_items 
FROM restaurants 
GROUP BY veg_or_nonveg;
```

#### 17. Cuisine with the Highest Average Cost per Person
```sql
SELECT cuisine, AVG(cost_per_person) AS avg_cost 
FROM restaurants 
GROUP BY cuisine 
ORDER BY avg_cost DESC 
LIMIT 1;
```

---

### 💻 Tools Used
- **SQL** – MySQL for query execution
---

### 👤 Author
- **Name**: Charan Kumar G  
- **Email**: charankumar.career@gmail.com  
- **LinkedIn**: [linkedin.com/in/charankumar-g](https://linkedin.com/in/charankumar-g)

---

⭐ If you found this project useful or insightful, consider giving it a ⭐ on GitHub!  
Let me know if you also want a `README.md` file version or folder structure suggestion to upload.
