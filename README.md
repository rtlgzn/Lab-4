# Lab-4
# Stebin George and Renata Toleugazina
# Revenue Recognition Problem (10 minutes)

## What is the Revenue Recognition problem?
The Revenue Recognition problem involves determining the appropriate timing and method for recognizing revenue from sales, especially when delivery and payment occur over an extended period.

## In the text example, what products are sold by the imaginary company?
The imaginary company sells three types of products:
- **Word Processors**
- **Spreadsheets**
- **Databases**

## How is revenue recognized for these three products?
- **Word Processors**: Revenue is recognized entirely at the time of sale.
- **Spreadsheets**: Revenue is recognized in three installments:
  - One-third at the time of sale
  - One-third after 60 days
  - Final third after 90 days
- **Databases**: Revenue is recognized in three installments:
  - One-third at the time of sale
  - One-third after 30 days
  - Final third after 60 days

## Explain what is meant by Figure 9.2.
Figure 9.2 illustrates the process of revenue recognition over time for different products, showing how revenue is allocated and recognized at various stages post-sale.

---

# Transaction Scripts Pattern (15 minutes)

## Describe the transaction script pattern at a high level. What are they?
Transaction Script is a pattern where each business operation is implemented as a single procedure or function, handling all aspects of the transaction in a straightforward manner.

## In the discussion of transaction scripts, how many transaction scripts are used and what are they?
Three transaction scripts are used:
- **Insert Order**: Handles the creation of a new order.
- **Calculate Revenue Recognitions**: Determines the schedule and amounts for revenue recognition.
- **Recognize Revenue**: Processes the actual recognition of revenue based on the schedule.

## Explain the use of the array named "allocation" in the `calculateRevenueRecognitions()` function with respect to the revenue recognition problem.
The `allocation` array stores the amounts and timings for revenue recognition, ensuring that revenue is recognized correctly over time according to the product's specific schedule.

---

# Domain Model Pattern (15 minutes)

## What is the difference between a simple domain model and a rich domain model?
- **Simple Domain Model**: Primarily represents data with minimal behavior.
- **Rich Domain Model**: Encapsulates both data and complex business logic within the domain objects.

## What does "POJO" stand for?
POJO stands for **"Plain Old Java Object"**, referring to simple Java objects not bound by any special restriction other than those forced by the Java Language Specification.

## The diagram in Figure 9.3 uses a strategy pattern. Which are the concrete strategies?
The concrete strategies include:
- **Complete Recognition Strategy**: For products where revenue is recognized entirely at the time of sale.
- **Three-Way Recognition Strategy**: For products where revenue is recognized in three installments over time.

## Of the products sold in the example problem, which strategy concrete class handles which product?
- **Word Processors**: Handled by the **Complete Recognition Strategy**.
- **Spreadsheets and Databases**: Handled by the **Three-Way Recognition Strategy**.

---

# Table Module Pattern (15 minutes)

## What is the difference between Domain Model vs Table Module?
- **Domain Model**: Business logic is incorporated within domain objects.
- **Table Module**: A single class handles business logic for all rows in a database table.

## What is the key advantage of using Table Module?
The Table Module pattern centralizes business logic related to a table, making it easier to manage and maintain, especially in systems closely aligned with relational databases.

## When is it better to use Domain Model vs Table Module?
- **Use Domain Model**: When the application has complex business logic and behaviors that fit well with object-oriented design.
- **Use Table Module**: When the application is heavily data-centric, and the business logic is straightforward and closely tied to database operations.

---

# Putting it all together

## Summarize the key things you learned during this lab.
This lab provided insights into different domain logic patterns, such as **Transaction Script, Domain Model, and Table Module**, each offering unique approaches to organizing business logic. Understanding these patterns aids in selecting the appropriate design based on the application's complexity and requirements.
