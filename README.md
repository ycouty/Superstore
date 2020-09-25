# Superstore
Sample Superstore Kinesis Project and Test Plans 

# Kinesis CI - Superstore Sample Projects

Superstore is a sample project for users of Kinesis CI for Tableau. Kinesis CI is a test framework that adds automated testing and continuous integration capability to Tableau Server. For more information on Kinesis CI, please visit http://kinesis-ci.com 

# Concept

This collection of projects is designed to give you examples for testing as well as for setting up your testing projects in Kinesis CI.

Each project contains a collection of test cases for a Tableau Workbook - Superstore, including the following test cases:

## Functional Testing
- Publish a Tableau workbook and a data source to Tableau Server
- Login and Open a viz
- Refresh data extract
- Set / Assert Filters
- Set / Assert Parameters
- Switch Tab
- Checking data against an expected data set
- Checking the layout of the Dashboard to an expected layout
- Selecting Marks for testing interactivity/user clicks

## Regression Testing
Running regression test on a Tableau dashboard to compare against a baseline in terms of data, layout, filter and parameter consitency

## Cross Environment Testing
Comparing the same Tableau View on two different environments i.e. dev and prod or two different Tableau Server versions, when doing and upgrade, in terms of data, layout, filter and parameter consistency

## Performance Testing
Testing the performance of your Tableau Server by driving load against it

This example goes hand in hand with the documentation of Kinesis CI, which you can find under https://kinesis-ci.com/documents

# How to use the demo projects
1. Clone the repository of your choice in Kinesis Designer (File -> Clone Git Repository and enter https://github.com/Superstore and open project.json. This project.json file contains key information to identify the individual test projects within this directory. Alternatively, you can use the Kinesis Command Line Interface and open the files in a text editor.

2. Edit the Context Variables in order to fit your environment, i.e. to reference the Tableau Server(s) you are using within your organisation. 
For more information on context variables, visit https://kinesis-ci.com/documents/#/context-variables

3. Use task 01.Import_Sample_Workbook if you need a workbook and data set to perform your tests. This task will import into Tableau the Superstore workbook and associated Excel data source.

5. In Regression test, create a new Baseline from your Tableau Server to compare against. 
For more information on Regression Tests, visit https://kinesis-ci.com/documents/#/regression-test

6. In Cross Environment test, update the target environment to fit your target environment you want to compare to your source environment. 
For more information on Cross Environment tests, visit https://kinesis-ci.com/documents/#/cross-environment-test 

# Directory Layout
For more information on the Directory Layout, please see https://kinesis-ci.com/documents/#/getting-started?id=create-new-project

# Schedule test runs and integration with CD tools (i.e. Jenkins)

If you want to run tests automatically, then you will need to install the Kinesis Command Line Interface on the server from which you want to schedule the tests or the CD tool server.
You can use the syntax available in Kinesis Designer when you click on Windows Scheduler, Cron or Jenkins.
Note: For Mac users, the command line will not be compatible with Windows, so it's best to generate it from a Windows machine.

Follow the steps detailed in https://kinesis-ci.com/documents/#/schedule-test-runs.

