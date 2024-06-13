# Postman-API-Automation
# Newman Installation and Execution Guide
This guide provides detailed steps to install Newman and generate HTML reports for your Postman collections and environments. Follow the instructions below to set up Newman, install the necessary reporters, and execute your Postman collections.

## Prerequisites
- Node.js installed on your system. You can download and install Node.js from [here](https://nodejs.org/).

## Step 1: Install Newman
Open your command prompt or terminal and run the following command to install Newman globally:
```sh
npm install -g newman
```
## Step 2: Install HTML Reporters
Install the basic HTML reporter and the enhanced HTML reporter using the following commands:
```sh
npm install -g newman-reporter-html
npm install -g newman-reporter-htmlextra
```
## Step 3: Export Postman Collection and Environment
Ensure you have exported your Postman collection and environment files. Save them to a location on your system. In this guide, we assume the following paths:
- Collection file: `D:\Postman\Hotel Booking API\Hotel Booking Details.postman_collection.json`
- Environment file: `D:\Postman\Hotel Booking API\Hotel Booking Utils.postman_environment.json`
## Step 4: Run Newman with Basic HTML Report
To generate a basic HTML report, use the following command:
```sh
newman run "D:\Postman\Hotel Booking API\Hotel Booking Details.postman_collection.json" -e "D:\Postman\Hotel Booking API\Hotel Booking Utils.postman_environment.json" -r html --reporter-html-export "D:\Postman\Hotel Booking API\Basic-report.html"
```
### Explanation of the Command
- `newman run` : Executes the Newman command.
- `"D:\Postman\Hotel Booking API\Hotel Booking Details.postman_collection.json"` : Path to your Postman collection file.
- `-e "D:\Postman\Hotel Booking API\Hotel Booking Utils.postman_environment.json"` : Path to your Postman environment file.
- `-r html` : Specifies the reporter type as basic HTML.
- `--reporter-html-export "D:\Postman\Hotel Booking API\Basic-report.html"` : Path where the HTML report will be saved.
## Step 5: Run Newman with Enhanced HTML Report
To generate an enhanced HTML report, use the following command:
```sh
newman run "D:\Postman\Hotel Booking API\Hotel Booking Details.postman_collection.json" -e "D:\Postman\Hotel Booking API\Hotel Booking Utils.postman_environment.json" -r htmlextra --reporter-htmlextra-export "D:\Postman\Hotel Booking API\Enhanced-report.html"
```
### Explanation of the Command
- `newman run` : Executes the Newman command.
- `"D:\Postman\Hotel Booking API\Hotel Booking Details.postman_collection.json"` : Path to your Postman collection file.
- `-e "D:\Postman\Hotel Booking API\Hotel Booking Utils.postman_environment.json"` : Path to your Postman environment file.
- `-r htmlextra` : Specifies the reporter type as enhanced HTML.
- `--reporter-htmlextra-export "D:\Postman\Hotel Booking API\Enhanced-report.html"` : Path where the enhanced HTML report will be saved.
## Summary
By following the steps outlined in this guide, you can install Newman, set up HTML reporters, and execute your Postman collections to generate both basic and enhanced HTML reports. Make sure to adjust file paths according to your setup.
For more detailed documentation and options, you can refer to the official [Newman documentation](https://github.com/postmanlabs/newman#readme).
