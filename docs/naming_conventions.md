# Naming Conventions
This document outlines the naming conventions used for schemas, tables, views, columns, and other objects in the data warehouse.

## Table of Contents 

  1. [General Principles](#general-principles)
  2. [Table Naming Conventions](#table_naming_conventions)
       - [Bronze Rules](#bronze_rules)
       - [Silver Rules](#silver_rules)
       - [Gold Rules](#gold_rules)
  3. [Column Naming Conventions](#column_naming_conventions)
       - [Surrogate Keys](#surrogate_keys)
       - [Technical Coulmns](#technical_columns)
  4. [Stored Procedure](#stored_procedure)

## General Principles

  - **Naming Conventions:** Use snake_case, with lowercase letters and underscores (_) to separate words.
  - **Language:** Use English for all names.
  - **Avoid Reserved Words:** Do not use SQL reserved words as object names.

## Table Naming Conventions

### Bronze Rules
  - All names must start with the source system name, and table names must match their origin names without renaming.
  - **<sourcesystem>_<entity>**
      - <sourcesystem>: Name of the source system (e.g., crm, erp).
      - <entity>: Exact table name from the source system.
      - Example: crm_customer_info --> Customer information from the CRM system.
        
### Silver Rules
  - All names must start with the source system name, and table names, must match their origin names without renaming.
  - **<sourcesystem>_<entity>**
      - <sourcesystem>: Name of the source system (e.g., crm, erp)
      - <entity>: Exact table name from the source system.
      - Example: crm_customer_infor --> Customer information from the CRM system.

### Gold Rules
  - All names must be meaningful, business'aligned names for tables, starting with the category prefix.
  - **<category>_<entity>**
    - <category>: Describes the role of the table, such as dim (dimension) or fact (fact table).
    - <entity>: Descriptive name of the table, aligned with the business domain (e.g., customers, products, sales).
    - Examples:
        - dim_customers --> Dimension table for customer data.
        - fact_sales --> Fact table containing sales transactions.

#### Glossary of Category Patterns
Pattern
