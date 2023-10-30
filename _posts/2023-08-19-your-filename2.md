---
published: true
---
---
title: "SQL"
# subtitle: "Introduction"
author:
    - JeongWook Lee
---

> R version 4.3.1/ Rstudio 2023.09.1-494 {#sec-r-version-4.3.1-rstudio-2023.09.1-494}
>
> Environment: Mac OS {#sec-environment-mac-os}


> Contents {style="gray"}

-   I. Concept

    -   1\. SQL (Structured Query Language)

    -   2\. SQL Select Statement

    -   3\. Objective

-   II\. Getting started

-   III\. Setting up the Environment

-   VI\. Uploading Data

-   V. Loading Data

    -   Comparison

-   IV\. Working with Data

# I. Concept

## 1. SQL (Structured Query Language)

> "The optimal programming language for storing and processing information in a database. It stores information in a tabular format based on **a relational database**, where rows and columns represent various relationships between different data attributes and values. **It allows storing, updating, removing, and retrieving information from the database** using SQL statements."

**NOTE:** SQL **plays a connecting role** in most types of applications as the commonly used programming language, **bridging the gap between data analysts and developers** who might use different programming languages.

-   It is a scripting programming language used **for storing and processing information in a database.**
-   It is a **type of relational database** where information is stored in tabular form.
-   It does **not differentiate between upper and lower case**.
-   It has a **simpler syntax** **and usage** compared to other languages like C or Java.

[![](images/SQL-schema-used-by-RetroRules-The-tables-in-white-are-the-parsed-meta-information-from.png "The basic format of an SQL statement"){#Basic format of an SQL statement}](https://www.researchgate.net/figure/SQL-schema-used-by-RetroRules-The-tables-in-white-are-the-parsed-meta-information-from_fig1_328306325)

## 2. SQL Select Statement

Viewing table data is a key need of interacting with a database.

This is best accomplished using the `SELECT` command.

``` sql
SELECT <tuple_projection_definition> 
FROM <table_expressions>
WHERE <tuple_retrictions>
```

**NOTE:** The result of a `SELECT` statement is a *table,* aka a relation.

The parts are defined as follows:

-   **tuple_projection_definition:** a list of columns, functions over columns, or other column expressions.

-   **table_expressions:** a list of tables and table expressions that provide source data for selected columns.

-   **tuple_retrictions:** a boolean expression that evaluates to either `TRUE` or `FALSE` for every row composited from the *tableexpressions\_.* Only the `TRUE` evaluative rows are returned in the result table.

Additionally, SQL supports the aggregation of data:

``` sql
SELECT <tuple_projection_definition, <aggregate_projection> >
FROM <table_expressions>
WHERE <tuple_retrictions>
GROUP BY <tuple_projection_definition>
HAVING <restriction_on_aggregate_projection>
```

## 3. Objective

> SQL is a widely used language in the field of data science worldwide, so it is essential for data scientists to have this skill. **One way to acquire a basic knowledge of SQL is through familiar R.**

------------------------------------------------------------------------

# II. Getting started

**Process**

```{r echo=FALSE, fig.height=1, fig.width=10, paged.print=TRUE}
library(knitr)
library(DiagrammeR)

# Mermaid 코드 작성
mermaid_code <- "
graph LR;
  Setting_path --> Uploading_file;
  Uploading_file --> Loading_the_file;
  Loading_the_file --> Aggregation;
"
  
# Mermaid 그래프 생성
mermaid_graph <- mermaid(mermaid_code)

 mermaid_graph
```
