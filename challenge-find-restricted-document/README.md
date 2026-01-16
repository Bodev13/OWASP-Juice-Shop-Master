# find-restricted-document

## Challenge Name

Find Restricted Document

## Challenge Description

The objective of this challenge is to locate a restricted document within the OWASP Juice Shop application by analyzing publicly accessible links and manually manipulating URLs using a web browser

## Recording of the challenge
https://go.screenpal.com/watch/cOVDXanrKV3


## Vulnerability Category

Broken Access Control / Directory Listing

## Tools Used

- Kali Linux  
- Mozilla Firefox  

## Step-by-Step Solution

1. Start OWASP Juice Shop locally
2. Navigat to the **About Us** page
3. Identify a publicly accessible document link pointing to `/ftp/legal.md`
4. Manually modify the URL in the browser’s address bar by removing the file name `legal.md`
5. Access the `/ftp/` directory directly
6. Browse through the available folders and files
7. Locate and opened the restricted document


## Result

The application allowed unrestricted access to internal files and directories without authentication or authorization checks

## Security Impact

Due to missing access control, unauthorized users can browse internal directories and access sensitive files. This may lead to information disclosure, data leaks, and potential legal or compliance issues

## Mitigation

- Disable directory listing on the web server
- Implement proper access control and authorization checks
- Restrict public access to internal directories such as `/ftp/`
- Validate and sanitize all user-accessible file paths


## Disclaimer

This challenge was solved in a controlled lab environment and is documented strictly for educational purposes
