# AWS Course Day 2
## AWS DynamoDB Intro

1. Run `python createTable.py`. This script creates a dynamo service client, then creates a table, and utilizes a waiter to wait until the async task of creating the table is complete.

2. Run `python loadData.py` to load the data from `notes.json` into the dynamoDB.

3. Run `python queryData.py` to query a specific note out of the db.

4. Run `python paginateData.py` to return all of the notes and display them in pages. 

5. Run `python updateItem.py` to update a record in the db. One aspect of this is to create an `is_incomplete` attribute. Look at line 16 - if you comment this line out, the update will be seen as invalid. this is an example of how to lock a record that is in use - by creating an `in_use` field instead of `is_incomplete`, for instance.

6. Run `python partiQL.py` to see how PartiQL - a SQL-compatible query language can be used with dynamoDB.