[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/r-tQZu0l)
# BBT3104-Lab1of6-DatabaseTransactions


| **Key**                                                               | Value                                                                                                                                                                              |
|---------------|---------------------------------------------------------|
| **Group Name**                                                               |B4|
| **Semester Duration**                                                 | 19<sup>th</sup> August - 25<sup>th</sup> November 2024                                                                                                                       |

## Flowchart
![FLOWCHART](https://github.com/user-attachments/assets/2aaf0537-a2bc-4003-872b-a92b038571fd)


## Pseudocode
STEP 1: START TRANSACTION

STEP 2:SET @orderNumber = MAX(orderNumber) + 1  FROM orders

STEP 3:INSERT INTO orders (@orderNumber, currentDate, requiredDate, status, customerNumber)
STEP 4: SAVEPOINT before_product_one

INSERT INTO orderdetails (OrderNumber, productCode, quantityOrdered, priceEach, orderLineNumber)

UPDATE products SET quantityInStock = quantityInStock - orderedQuantity

SAVEPOINT before_product_2
INSERT PRODUCT 
         IF error THEN
              ROLLBACK TO SAVEPOINT before_product_2
ENDIF
 INSERT remaining products
RECEIVE payment from customer

COMMIT TRANSACTION
## Support for the Sales Departments' Report
The pseudocode provided demonstrates a comprehensive approach to managing a multi-step transaction involving order placement, product details insertion, inventory updates, and payment processing. It emphasizes the importance of transaction control mechanisms in ensuring data integrity and reliability across several database operations.
Atomicity is a concept that states that a transaction is a single unit of work that must be successfully executed. It ensures data consistency throughout the process, with savepoints allowing the system to go back to specific points of the transaction. Isolation prevents other users or processes from seeing unfinished or erroneous orders, ensuring consistency and protection from interference until the transaction completes successfully. Durability is also maintained, as changes are permanently saved in the database, ensuring data is not lost during system failures.
