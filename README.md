# Introduction
This case study aims to develop our skills in transforming unstructured data into 
structured data. The provided dataset contains 43 text files. The original files include 
data such as header lines with page information, run times, amounts, sections 
organized by transaction date, DEBIT/CREDIT columns, and transaction codes that can 
repeat. The following report provides the approach, technical steps, assumptions, and 
data quality profiling applied throughout this data transformation exercise.

# Approach

This case study uses Python and RegEx to extract structured data from unstructured text files. Pandas converts the extracted data into a table and exports them to Excel formats. Pathlib handles file operations, including looping through all files and counting them for verification.
We did not develop the code and run everything for the final output all at once. Instead, we gradually developed the code by breaking it down into five phases or cells in a Jupyter Notebook, which allowed us to run each chunk of code for easier debugging. During the transformation process, we printed the results so we could identify and fix issues early. The five phases serve different purposes as follows:

• **Phase 1**:
Identifying the elements and patterns we need for final output. Then test if the script detects the right elements by printing the result so we can manually check the results against the original file.
• **Phase 2**:
Identify the header boundary, extract transactions using regex, and return structured data as a list of dictionaries.
• **Phase 3**: Testing the function, which returns a list of dictionaries. Convert this to a table and print summaries including total transactions, DEBIT count, CREDIT count, and a sample of the table so that we can manually verify accuracy against the original file.
• **Phase 4**: Using the glob method with a wildcard pattern to count how many files exist in the folder and to ensure that we have access to all 43 files.
• **Phase 5**: Iterate through all files, extract transactions from each, combine into one master list, then convert to a table.
• **Phase 6**: Export the file into a local computer
