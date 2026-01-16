# Find the Score Board

## Challenge Description

The objective of this challenge is to discover the hidden Score Board page of the OWASP Juice Shop application by manually accessing a known but undocumented URL endpoint using a web browser.

---

## Table of Contents

- [Challenge Name](#challenge-name)
- [Challenge Description](#challenge-description)
- [Usage](#usage)
- [Recording of the Challenge](#recording-of-the-challenge)
- [Vulnerability Category](#vulnerability-category)
- [Tools Used](#tools-used)
- [Step-by-Step Solution](#step-by-step-solution)
- [Result](#result)
- [Security Impact](#security-impact)
- [Mitigation](#mitigation)
- [Disclaimer](#disclaimer)

---

## Challenge Name

Find the Score Board

---

## Usage

This challenge is performed in a local or controlled lab environment using the OWASP Juice Shop application. The user interacts with the application through a web browser to manually access undocumented endpoints and analyze exposed application functionality.

---

## Recording of the Challenge

https://go.screenpal.com/watch/cOV6rinrwxN

---

## Vulnerability Category

Information Disclosure

---

## Tools Used

- Kali Linux  
- Mozilla Firefox  

---

## Step-by-Step Solution

1. Start the OWASP Juice Shop application locally on a Kali Linux virtual machine.
2. Open Mozilla Firefox.
3. Navigate to the base URL `http://127.0.0.1:3000`.
4. Manually append `/score-board` to the URL in the browser’s address bar.
5. Access the hidden Score Board page.
6. Review the list of all challenges and their completion status.

---

## Result

The Score Board page, which is not linked anywhere in the application interface, was accessible directly via its URL without authentication or authorization.

---

## Security Impact

Exposing the Score Board allows unauthorized users to gain insight into the internal structure and status of the application. In real-world scenarios, this type of information disclosure could reveal sensitive internal data, application logic, or security weaknesses that may facilitate further attacks.

---

## Mitigation

- Restrict access to administrative or internal pages such as the Score Board.
- Implement proper authentication and authorization checks.
- Protect sensitive endpoints with role-based access control.
- Avoid exposing internal status or debugging pages in production environments.

---

## Disclaimer

This challenge was solved in a controlled lab environment and is documented strictly for educational purposes.
