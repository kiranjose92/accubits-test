# accubits-test
Repsoitory for Accubits machine test

### Task :

Your task will be to create an API to upload a CSV file with 1000 records, you will have to save the records in a MySQL database, the format of the columns are as given below.

| Module_code | Module_name | Module_term |
| ------------- |:-------------:| -----:|
||||
||||
||||

The CSV file should be thoroughly validated to 
Check for the file extension
The column counts, the column names, and row validations should be configurable so that you can reuse the same validator later on in some other CSV file with a different format.
All cells in the CSV files should be validated and all the similar errors should be grouped together 
 
   [
       "Header column (Module C#ode at 1st column) is incorrect in csv file",
       "Module Code contains symbols at row  0",
       "Term Name is missing at row 1",
       "Module Name is missing at row 2 and 3",
       "Term Name contains symbols at row  3"
   ]

The file processing task should take place in the background as a queue operation.
Once the queue operation is completed a mail shall be sent automatically to charush@accubits.com detailing about the errors in the columns and rows in the CSV file.

All the operations and functions used to build the API should strictly use laravel specific implementations, example regex should be handled using laravel validator 
  
The CSV file can be generated using https://mockaroo.com/
