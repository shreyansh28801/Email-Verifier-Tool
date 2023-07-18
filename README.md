# GO Email Checking Tool

Welcome to the Email Verifier Tool repository! This repository contains the source code and documentation for a simple tool that verifies the validity of email addresses. The tool is built using Go and performs various checks on a given domain to determine its email-related properties.

## Functionalities
The Email Verifier Tool provides the following functionalities:

- Domain Validation:
   Verify the validity of a domain by performing the following checks:
   - MX Record: Check if the domain has MX (Mail Exchange) records.
   - SPF Record: Check if the domain has an SPF (Sender Policy Framework) record.
   - DMARC Record: Check if the domain has a DMARC (Domain-based Message Authentication, Reporting, and Conformance) record.

## Getting Started
To get started with the Email Verifier Tool, follow the instructions below:

## Prerequisites
Make sure you have Go installed on your system.

## Installation
Clone this repository to your local machine or download the source code as a ZIP file.

```
git clone https://github.com/your-username/email-verifier-tool.git
```

Open a terminal and navigate to the project directory.

```
cd email-verifier-tool
```

## Usage
1. Open the main.go file and provide a list of domains to be verified. Each domain should be on a separate line in a text file.

2. Run the following command to execute the Email Verifier Tool:

```
go run main.go < domains.txt
```

The tool will perform various checks on each domain and display the results in the format: domain, hasMX, hasSPF, spfRecord, hasDMARC, dmarcRecord. The results will be printed to the console.

## Input and Output

 Here's an example of the input and corresponding output based on the provided main.go file:
### Input (domains.txt):

 ```
example.com
google.com
github.com
```

### Output:

```
domain,hasMX,hasSPF,spfRecord,hasDMARC,dmarcRecord
example.com, true, true, v=spf1 -all, true, v=DMARC1; p=none
google.com, true, true, v=spf1 include:_spf.google.com ~all, true, v=DMARC1; p=none
github.com, true, false, , true, v=DMARC1; p=none
```



