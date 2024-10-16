## Simple ETL Pipeline: PostgreSQL to Snowflake

This ETL pipeline extracts data from a PostgreSQL database, validates it, and loads it into a Snowflake data warehouse. The pipeline is implemented using Python and leverages the `pandas` library alongside `SQLAlchemy` for database interactions.

### Features:

- Data Extraction:
  Connects to PostgreSQL to extract data from the `Games` table and loads it into a DataFrame.
- Data Validation:
  Performs checks to ensure data integrity, including:
    - Null value detection
    - Data type validation for each column:
      - Integer for `year`, `winner_goals`, and `opponent_goals`
      - String for `round`, `winner`, and `opponent`
- Data Loading:
  - Appends validated data into a Snowflake table using batch inserts for improved performance.

