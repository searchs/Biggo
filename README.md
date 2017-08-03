# Agile Biggo
A Test Framework for BigData testing to allow Continuous Integration and Delivery.  This will be a scalable Big data Test framework that generates representative data sets and validate data transfers and transformation.

### Goal of Framework
The framework should compare the source data with the target data to evaluate whether the target data was transformed correctly. The testers are required to write the transformation specification in a format that the test framework can read. Then the framework automatically analyzes the specification and generates tests to validate the transformation.

Big Data testing tests the process and then checks data integrity.  It is important to check the quality of the data. Various data characteristics like data completeness,conformity, accuracy, duplication, consistency, validity and many more data attributes should be checked.

Data processing can be:
  1.  Batch
  2.  Real time
  3.  Interactive
  
Understanding of the business rules is key to verification.

#### Data Dictionary:  Include field value before and after transformation
__High Level View__
*  First, we validate whether the target data has correct data types and value ranges at a high level.
*  Secondly, derive detailed specifications to validate every transformation rule.

The framework derives data types and value ranges from requirements, then generate test to validate the target
data. 

We only validate the source and target data, not the transition points in the middle. These are only checked for
failure diagnosis (debugging).


#### Validation of Source and Target:
* Not all fields will make it to the end in their current state.
* Validate the source and target data quickly by checking the number of columns, rows, and the columns’ names and data types.
* Validate only the Source and Target data.  Not the transitions 
* Validate fields that remain the same (Data integrity)
* Validate fields that SHOULD be transformed (Data integrity)
* Validate fields that should not make it to the final output - simple check on the final columns names
* For ETL processes, we only need to validate data transfer. Since there are other data sources involved in that step.

### Test Data Source
*  Generate a representative data set from a large original data set.


### Future Considerations
Every data cell should be evaluated. The validation can be automated when source and target data are provided.







