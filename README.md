ELT Pipeline with dbt, Snowflake, and Apache Airflow
========

This project demonstrates how to build an ELT (Extract, Load, Transform) pipeline using dbt, Snowflake, and Apache Airflow. The pipeline extracts sample data from Snowflake's TPCH dataset, loads it into a staging area within Snowflake, transforms it into analytical models using dbt, and orchestrates the entire workflow using Apache Airflow.

Project Objectives
================

- Implement a Scalable ELT Pipeline: Showcase the integration of modern data tools to build a scalable and maintainable data pipeline.
- Leverage Cloud Data Warehousing: Utilize Snowflake's cloud-based data warehousing capabilities for efficient data storage and processing.
- Modular Data Transformations: Use dbt to perform modular, testable, and version-controlled data transformations.
- Automate Workflow Orchestration: Employ Apache Airflow to schedule, monitor, and manage data workflows.

Technologies Used
===========================

- Snowflake: A cloud-based data warehouse platform that offers high performance, scalability, and flexibility..

    - Role in ELT: Acts as the central repository where raw data is loaded and transformations are executed.
- dbt (Data Build Tool): An open-source tool that enables data analysts and engineers to transform data in their warehouse by simply writing SQL select statements.

    - Role in ELT: Manages data transformations, dependencies, testing, and documentation within the warehouse.
- Apache Airflow: An open-source platform to programmatically author, schedule, and monitor workflows.

    - Role in ELT: Orchestrates the entire data pipeline, scheduling extraction, loading, and transformation tasks.


How the Project Works
=================================

This project builds an ELT pipeline using Snowflake, dbt, and Apache Airflow:

- Data Source: Leverages Snowflake's TPCH sample data (orders and lineitem tables).

- Data Transformation with dbt:

    - Staging Models: Clean and prepare raw data.
    - Macros: Use reusable SQL snippets for calculations.
    - Intermediate and Fact Models: Join and aggregate data to form analytical tables.
- Workflow Orchestration with Apache Airflow:

    - DAG Scheduling: Airflow automates the execution of dbt models on a daily schedule.
    - Monitoring: Provides logging and monitoring of the pipeline's execution.
- Data Flow Summary:

    - Extract: Reference sample data directly from Snowflake.
    - Load: Use dbt to load data into staging models within Snowflake.
    - Transform: Apply transformations using dbt to create intermediate and fact models.
    - Orchestrate: Airflow schedules and runs the dbt pipeline, managing dependencies and execution order.
