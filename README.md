📘 JMeter Project: User Creation Performance Test
🔧 Project Overview
This JMeter project (first.jmx) is designed to simulate and test user creation functionality by sending HTTP requests with data from a CSV file. It measures the performance, reliability, and behavior of the endpoint under load.

📁 Project Structure
1. Test Plan
Main container for all testing components.

Configured with relevant user-defined variables, test setup, and teardown actions.

2. Thread Group
Users: Defines the number of virtual users (threads) and loop count.

Simulates concurrent user creation requests.

Parameters like:

Number of Threads (Users)

Ramp-Up Period

Loop Count

3. CSV Data Set Config
File: user-create-data-file - Sheet1.csv

Supplies dynamic test data (e.g., user details) to the HTTP Request Sampler.

Ensures unique or varied input during test execution.

4. HTTP Request Sampler
Sends HTTP POST requests to the user creation API.

Uses values from the CSV for dynamic payloads.

5. Assertions
Verifies successful responses (e.g., HTTP 200 or response body contains expected text).

6. Listeners
Includes:

View Results Tree

Summary Report

Aggregate Report

Used to view request/response data and overall performance metrics.

🗂️ CSV File: user-create-data-file - Sheet1.csv
Contains user data (e.g., username, email, password) for use in test execution. Make sure:

It’s located in the same directory as the .jmx file or correctly referenced in the CSV Data Set Config.

Data format matches parameter names in the HTTP sampler body.

▶️ How to Run
Open Apache JMeter.

Load the file first.jmx.

Ensure the CSV file path is correct in CSV Data Set Config.

Adjust Thread Group settings if needed.

Click Start (Green play button) to begin the test.

View results using listeners.

📊 Output
Success rate of user creation requests.

Average response time, throughput, and error rate.

Useful for detecting bottlenecks and backend API issues.
