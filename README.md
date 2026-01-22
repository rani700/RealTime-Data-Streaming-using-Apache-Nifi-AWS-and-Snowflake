Built a realtime streaming service which picks the data from EC2 Machine and store it in s3 bucket using the Apache NiFI, From the S3 bucket data is transferred to Snowflake using SnowPipe for the staging purpose. And then CDC (Change Data Capture) is done using snowflake stream(object that record DML changes made to a table) and snowflake task (Task used to schedule sql statement).

After the whole process we will have 3 tables
1. Staging Data Table
2. Actual Data table (SCD - Slowly changing dimension 1)
3. History Data Table (SCD - Slowly chaning dimesion 2)

The whole above activity was done on an EC2 machine using docker and docker-compose there.
<img width="1512" height="596" alt="Screenshot 2026-01-22 at 2 06 45 PM" src="https://github.com/user-attachments/assets/e7ed03ff-ac62-4f37-826b-405c037ec393" />

