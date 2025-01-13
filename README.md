# IDS Codebook
George Alter

The Access database "IDS_codebook_general.accdb" runs SQL queries that create a codebook describing an IDS database.  Summaries are created for the INDIVIDUAL and CONTEXT tables showing the number of rows by Value for each Type found in the table.  The INDIV_INDIV, INDIV_CONTEXT, and CONTEXT_CONTEXT tables appear in one section showing the number of rows for each Relation.   
   
Steps:
1. Use the MS-Access Linked Table Manager (under the External Data tab) to link the IDS files (CONTEXT, CONTEXT_CONTEXT, INDIV_CONTEXT, INDIV_INDIV, INDIVIDUAL) to the data in a separate MS-Access database. Check the "Always prompt for new location" to change to a different database.  Test data have been provided in the Fam_Recon_test_data_v2.accdb file.     
        
2. Use the MS-Access Linked Table Manager to link the metadata tables.     
The "METADATA_STANDARD" table should be linked to the latest version of IDS Metadata.   
The "METADATA_LOCAL" table can be used for metadata definitions developed locally that are not part of the IDS standard. 
       
3. Enter the author, title, and production date in the "Study_description" table.

4. Run the "Run codebooks" macro.  Executing the macro called "Run report" will run all of the queries and create a codebook.    
   
5. Select "Print Preview" under the "Views" option on the "Home" tab.  Click "Print" to print the codebook.   
         
Notes:      
The Linked Table Manager can be used to link to data in other IDS databases in Access or other database systems.   Databases other than Access (MySQL, Posgres, Oracle, etc.) can be linked via ODBC.   
   
The queries given here may require editing before they can be used in other database systems.  While basic SQL keywords are the same in all versions of SQL, functions are often implemented differently.  These queries make extensive use of functions for dates and for parsing text, which may not be compatible with other dialects of SQL.   
   
These queries can be tested using the [Fam_Recon_test_data_v2.accdb](https://github.com/altergc/IDS/blob/main/Tools/IDS_Validation/Fam_Recon_test_data_v2.accdb), which is provided in this repository.  This test should generate the result found in the [IDS_Codebook_test.pdf](https://github.com/altergc/IDS/blob/main/Tools/IDS_Validation/IDS_Codebook_test.pdf) file.   
   
   
## License    
This work is licensed under the [MIT License](https://opensource.org/licenses/MIT).    
Please see the LICENSE.txt file in this folder.    
    
## Citation	 
Please cite this work as:    
Alter, G. C. (2022). IDS Validation Queries [SQL]. https://github.com/altergc/IDS/tree/main/Tools/IDS_Validation


