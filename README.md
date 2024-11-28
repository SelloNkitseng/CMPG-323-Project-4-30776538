# Project-4-Robotic-Process-Automation

Project Overview

This UiPath automation project reads data from an Excel file, iterates over each record, and inputs the data into a web application to create a new record. The automation will then verify if the record was successfully created on the web application and update the Excel sheet with the test results (TRUE or FALSE) based on whether the record passed or failed.

Process Workflow

1. Read Data from Excel File

Use the Excel Application Scope activity to open the Excel file.
Inside the scope, use the Read Range activity to read the data into a Data Table.
Ensure the Excel file contains all required fields for data entry and a Test Passed column for tracking results.

3. Iterate Over Data Table

Use a For Each Row activity to loop through each record in the Data Table.

4. Navigate to the Web Application

Use the Open Browser activity to navigate to the URL where new records are created.
Ensure that the URL for the form page is provided.

5. Enter Data into Web Application

For each record, use Type Into activities to input the required data into the respective fields on the web form.
After entering the data, use the Click activity to click the "Submit" button to create the new record.

6. Verify Record Creation

Navigate to the URL where the newly created record can be viewed using the Navigate To activity.
Check for the presence of the newly created record using the Element Exists activity.

7. Update Testing Results in Data Table

If the record was created successfully, update the corresponding row in the Data Table with TRUE in the Test Passed column.
If the record was not created or any errors occur, update the Test Passed column with FALSE.

8. Update Excel File with Results

Once all records are processed, use the Write Range activity to write the updated Data Table back to the Excel file.
Ensure that the updated Test Passed column is saved correctly.
