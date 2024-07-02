# PDI Data Transformation Project

## Overview

This repository contains files related to a data transformation project carried out using Pentaho Data Integration (PDI). The project was completed as part of the "Decision Support Systems" course. The main objective was to perform a series of data transformations and cleanups based on the provided `pessoa.sql` script. The database used for this project was PostgreSQL.

## Challenges

The following transformations were performed:

1. **Concatenate Fields to Create Full Name:**
   - Created a new field `nomecompleto` by concatenating `nome`, `nomedomeio`, and `sobrenome`.
   - Removed the original fields (`nome`, `nomedomeio`, `sobrenome`).

2. **Gender Data Cleaning:**
   - Standardized the `gênero` field to use "M" for male, "F" for female, and "O" for others.

3. **City Data Cleaning:**
   - Performed data cleaning on the `cidade` field to ensure consistency and accuracy.

4. **Region Data Consistency:**
   - Ensured data consistency in the `região` field.

5. **Decimal Formatting:**
   - Converted the `altura`, `peso`, and `rem_em_dolar` fields to two decimal places.

6. **Height Classification:**
   - Created a new field to classify individuals based on their height:
     - Up to 1.70m: `baixo`
     - Between 1.71m and 1.80m: `médio`
     - Above 1.80m: `alto`

7. **Shirt Size Classification:**
   - Created a new field `tamanho_de_camisa` based on weight:
     - Up to 70.00kg: `P`
     - Between 70.01kg and 90.00kg: `M`
     - Between 90.01kg and 120.00kg: `G`
     - Between 120.01kg and 150.00kg: `GG`
     - Above 150.00kg: `XG`

8. **Currency Conversion:**
   - Converted the `rem_em_dolar` field to Brazilian Real (BRL), using a parameter for the exchange rate.

## Files

- **Transformation Files:** Contains the PDI transformation files (`.ktr` and `.kjb`).
- **SQL Scripts:** The original `pessoa.sql` script and any other SQL files used during the transformation process.
- **Documentation:** Additional documentation explaining the transformations and the PDI process.

## Getting Started

To replicate or understand the transformations, follow these steps:

1. **Setup PostgreSQL:**
   - Ensure you have a PostgreSQL database setup.
   - Run the `pessoa.sql` script to create and populate the necessary tables.

2. **Install Pentaho Data Integration:**
   - Download and install PDI from the official Pentaho website.

3. **Load Transformation Files:**
   - Open PDI and load the provided `.ktr` and `.kjb` files.

4. **Adjust Parameters:**
   - Ensure to set the exchange rate parameter for currency conversion as required.

5. **Execute Transformations:**
   - Execute the transformations and verify the results in your PostgreSQL database.
