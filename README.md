SELECT cust_gender, COUNT(*) AS total_customers
FROM customer c
INNER JOIN orders o ON c.cust_id = o.CUST_ID
WHERE o.ORD_AMOUNT >= 3000
GROUP BY cust_gender;
SELECT s.SUPP_ID, s.SUPP_NAME
FROM supplier s
INNER JOIN supplier_pricing sp ON s.SUPP_ID = sp.SUPP_ID
GROUP BY s.SUPP_ID, s.SUPP_NAME
HAVING COUNT(DISTINCT sp.PRO_ID) > 1;
