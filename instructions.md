# PostgreSQL Universe Database Project

## Instructions

To complete this project, follow the steps below:

1. Log in to PostgreSQL with `psql` by entering the following command in the terminal:
   ```bash
   psql --username=freecodecamp --dbname=postgres
   ```
2. Make all the tests below pass to complete the project. Be sure to get creative, and have fun! 🎉

> **Note:** Don't forget to connect to your database after you create it:
> ```sql
> \c universe
> ```

## Ideas for Columns and Tables

Here are some ideas for column and table names you can use:
- Columns: `description`, `has_life`, `is_spherical`, `age_in_millions_of_years`, `distance_from_earth`
- Tables: `planet_types`, `galaxy_types`

---

## Saving Your Database

- If you leave your virtual machine, your database may not be saved. To ensure your progress is saved, create a dump of your database by running:
  ```bash
  pg_dump -cC --inserts -U freecodecamp universe > universe.sql
  ```
  This will save the commands to rebuild your database into a file named `universe.sql`. The file will be located in the directory where the command is executed. 
  - If this directory is inside the project folder, the file will remain in the virtual machine (VM).

- To rebuild your database later, use the following command:
  ```bash
  psql -U postgres < universe.sql
  ```

---

## Submitting Your Progress

If you're saving your progress on freeCodeCamp.org:
1. After completing all tasks, save a dump of your database as described above.
2. Save the `universe.sql` file in a public repository.
3. Submit the repository URL on freeCodeCamp.org.

---

## Requirements

To complete the project, ensure the following tasks are completed:

### Database Creation
- Create a database named `universe`.
- Connect to the database using:
  ```sql
  \c universe
  ```

### Tables
Create the following tables:
1. **galaxy**
2. **star**
3. **planet**
4. **moon**
5. **(Optional additional table)**

Each table must meet these criteria:
- Have a primary key that **automatically increments**.
- Include a `name` column of type `VARCHAR`.
- Use the `INT` data type for at least **two columns** that are not primary or foreign keys.
- Use the `NUMERIC` data type at least **once**.
- Use the `TEXT` data type at least **once**.
- Use the `BOOLEAN` data type in at least **two columns**.
- At least **two columns per table** should **not accept NULL values**.
- At least **one column per table** should be **UNIQUE**.

### Relationships
- Each **star** should have a foreign key referencing a row in the `galaxy` table.
- Each **planet** should have a foreign key referencing a row in the `star` table.
- Each **moon** should have a foreign key referencing a row in the `planet` table.
- Foreign key columns should have the same name as the column they reference.

### Data Population
- The `galaxy` and `star` tables must each have at least **6 rows**.
- The `planet` table must have at least **12 rows**.
- The `moon` table must have at least **20 rows**.
- Each table must have at least **3 columns**.
- The `galaxy`, `star`, `planet`, and `moon` tables must each have at least **5 columns**.

### Naming Conventions
- Primary key columns should follow the naming convention: `<table_name>_id`. For example:
  - `galaxy_id` for the `galaxy` table.
  - `moon_id` for the `moon` table.
- Foreign key columns should have the same name as the column they reference.

---

## Good Luck! 😄
Feel free to customize your database and get creative while meeting the requirements. If you encounter any issues, revisit the notes above or consult PostgreSQL documentation.
