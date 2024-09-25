# STORE CUSTOMER CLTV ANALYSIS & MODEL TRAINING

## What will you learn from this project?
* Data Reading
* Data Cleaning
* Data Preparation
* CLTV Analysis
* Customer Lifetime Value
* BG/NBD Model
* Gamma Gamma Submodel
* Segmentation
* CLTV Prediction with Time Projection

## Introduction
* ***Customer Lifetime Value (CLTV):*** is considered to be the monetary value that a customer will bring to a company during its relationship and communication with that company.

* CLTV Prediction with Time Projection:
  > CLTV = Expected Number of Purchases x Expected Profit Margin

  As a result of this model, we can calculate the expected average profit and the expected number of transactions for each person by reducing the general behavioural characteristics of the crowd to each individual and asking the individual characteristics to the model. With the multiplication of these values, the CLTV value can be developed and the CLTV calculation can be performed for each individual by using a time-projected, conditional expected expression, in a way to accommodate the characteristics of the general mass carried by the conditional expected expression.

  > CLTV = BG/NBD Model x Gamma Gamma Model

* ***BG/NBD Model:*** It is a probabilistic model that is also used as a stand-alone sales forecasting model. BG/NBD probabilistically models two processes for the expected number of transactions:
  * The purchase Process:
    - It is the modelling of the purchasing process. In this context, the number of transactions to be performed by a customer in a given time period is distributed possionally with the transaction rate parameter.
    - A user will continue to make random purchases around its transaction rate for as long as it is alive.
    - Transaction rates vary for each customer and are gamma-distributed for the whole population.
  * Dropout Process (Churn):
    - Modelling the process by which the user leaves the brand.
    - Each customer has a dropout rate (dropout probability) with probability p.
    - A customer drops with a certain probability after shopping.
    - The dropout rate varies for each customer and is beta distributed for the entire audience.

* ***Gamma-Gamma Model:*** It is used to estimate how much profit a customer can generate on average per transaction, and the monetary value of the customer's transactions is randomly distributed around the average of their transaction values.

## Analysis Content
1. [Python Libraries](#1)
2. [Data Content](#2)
3. [Read & Analyse Data](#3)
4. [Data Distributions](#4)
5. [Data Preprocessing](#5)
6. [Data Preprocessing (Suppression)](#6)
7. [Data Preparation](#7)
8. [Lifetime Data Structure Preparation](#8)
9. [BG-NBD Model Setup](#9)
10. [Gamma Gamma Model Setup](#10)
11. [CLTV Calculation with BG-NBD & GG Model ](#11)
12. [CLTV Segmentation](#12)
13. [Conclusion](#13)

---

## Data Content
* This Online Retail II data set contains all the transactions occurring for a UK-based and registered, non-store online retail between 01/12/2009 and 09/12/2011.The company mainly sells unique all-occasion gift-ware. Many customers of the company are wholesalers.
    
    * ***InvoiceNo:*** Invoice number. Nominal. A 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a cancellation. 
    * ***StockCode:*** Product (item) code. Nominal. A 5-digit integral number uniquely assigned to each distinct product. 
    * ***Description:*** Product (item) name. Nominal. 
    * ***Quantity:*** The quantities of each product (item) per transaction. Numeric.	
    * ***InvoiceDate:*** Invice date and time. Numeric. The day and time when a transaction was generated. 
    * ***UnitPrice:*** Unit price. Numeric. Product price per unit in sterling (Â£). 
    * ***CustomerID:*** Customer number. Nominal. A 5-digit integral number uniquely assigned to each customer. 
    * ***Country:*** Country name. Nominal. The name of the country where a customer resides.

* Online Retail II Official Website: https://archive.ics.uci.edu/dataset/502/online+retail+ii
