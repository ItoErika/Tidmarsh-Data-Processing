# Tidmarsh data processing

## Workflow
**Note:** The [brackets] in the example script indicate portions that must be replaced with specific directory paths or names specific to unique map sources. For example, a `path` might look like `~/Desktop/Folder`

### 1. Create Dataset

**Data Requirements:** 
+ vector geometry
+ age
+ lithology / description
 
### 3. Import data table(s) of interest into PostgreSQL

`cd [path to repo folder]`

Import to Postico

`./import [table_name] [path to shapefile] false LATIN1`
   

### 4. Process dataset

**Move the issue to the "In progress" column in [Processing](https://github.com/UW-Macrostrat/burwell-processing/projects/1).**

Homogenize data tables
  
### 5. Zip completed data table(s) (in terminal)**
Zip each data table
`pg_dump -x -O -t sources.[table_name] [schema]|gzip>[table_name].sql.gz`
  
### 6. Create a new folder for the dataset, and include:
   + zipped SQL dump(s) of updated attribute tables
   + any metadata
   
### 7. Secure copy this new folder to push to MIT computer:
Before copying the folder, make sure permissions on it are correctly set:

`
chmod -R 777 [folder]
`

Next, push the folder to MIT computer in terminal:   

**Data of Interest (in order of priority):**
