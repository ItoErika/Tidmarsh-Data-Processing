# Tidmarsh data processing

## Workflow
**Note:** The [brackets] in the example script indicate portions that must be replaced with specific directory paths or names specific to unique map sources. For example, a `path` might look like `~/Desktop/Folder`

### 1. Create and organize Dataset

**Data Requirements:** 
 
### 2. Import data table(s) of interest into PostgreSQL

### 3. Process dataset and check for errors

**Move the issue to the "In progress" column in [Processing](https://github.com/UW-Macrostrat/burwell-processing/projects/1).**

Homogenize data tables
  
### 4. Zip completed data table(s) (in terminal)**
Zip each data table
`pg_dump -x -O -t sources.[table_name] [schema]|gzip>[table_name].sql.gz`
  
### 5. Create a new folder for the dataset, and include:
   + zipped SQL dump(s) of updated attribute tables
   + any metadata
   
### 6. Secure copy this new folder to push to MIT computer:
Before copying the folder, make sure permissions on it are correctly set:

`
chmod -R 777 [folder]
`

Next, push the folder to MIT computer in terminal:   

**Data of Interest (in order of priority):**
