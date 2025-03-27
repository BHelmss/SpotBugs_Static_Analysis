# SpotBugs_Static_Analysis

## Project Overview
Author: Brendan Helms (ID: 700695073)
Abstract: This project focuses on analyzing the OWASP WebGoat application, a deliberately vulnerable teaching tool maintained by OWASP, to identify and remediate security vulnerabilities using SpotBugs, a static analysis tool. SpotBugs was integrated via Maven to scan WebGoat for common vulnerabilities, initially identifying 209 bugs. The project specifically targeted 5 security-category bugs related to SQL injection vulnerabilities, rectified them using prepared statements, and reduced the total bug count to 195.
## Objectives
Perform static analysis on OWASP WebGoat using SpotBugs to identify security vulnerabilities.

Focus on 5 security-category bugs, particularly SQL injections caused by nonconstant strings in query statements.

Remediate vulnerabilities by implementing secure coding practices (e.g., prepared statements with placeholders).

Document findings and verify remediation through updated SpotBugs reports.

## Project Steps and Findings
Initial Analysis:
Conducted a SpotBugs scan on WebGoat, identifying 209 bugs, with a focus on security vulnerabilities.

Targeted 5 bugs in the security category, all related to SQL injection risks due to dynamic string concatenation in SQL queries.

## Bug Identification and Remediation:
Bug #1 (JWTHeaderKIDEndpoint): Identified SQL injection risk on lines 91-92 due to the kid variable in a dynamic string. Replaced with a prepared statement using ? placeholders, removing the vulnerability.

Bug #2 (CheckUserQuery): Found SQL injection risk from the username_reg variable in a query string. Removed the variable and used a prepared statement, eliminating the security bug.

Bug #3 (SqlInjectionLesson5a): Detected a nonconstant string with the accountName variable on line 67. Implemented a prepared statement with ? placeholders, reducing vulnerabilities in the report.

Bug #4 (Lesson 8): Identified SQL injection risk from two variables (name and auth_tan) in a query string. Replaced with ? placeholders and set parameters safely, leaving only one remaining bug in the lesson.

Bug #5 (Lesson 8): Found SQL injection risk from time and action variables in a dynamic string. Used ? placeholders in a parameterized query, fully resolving security bugs in Lesson 8.

## Outcomes:
Successfully remediated all 5 targeted SQL injection vulnerabilities, ensuring safer data handling and protecting database integrity and confidentiality.

Reduced the total bug count from 209 to 195, addressing additional minor issues during the process.

Verified remediation through updated SpotBugs reports, confirming the removal of security-category bugs in targeted sections.

## Key Takeaways
Demonstrated proficiency in static analysis using SpotBugs to identify common vulnerabilities like SQL injections.

Applied secure coding practices (e.g., prepared statements) to mitigate risks, enhancing the security of WebGoat.

Gained hands-on experience in vulnerability analysis, remediation, and report writing, aligning with industry best practices for secure software development.

## Tools Used
SpotBugs: Static analysis tool integrated via Maven to identify vulnerabilities in WebGoat.

OWASP WebGoat: Vulnerable application used as a teaching tool for security analysis.

Maven: Build automation tool used to run SpotBugs scans.

## Conclusion
This project highlights my ability to analyze and secure applications by identifying and remediating critical vulnerabilities. By reducing the bug count in WebGoat and eliminating SQL injection risks, I’ve strengthened my skills in static analysis, secure coding, and vulnerability management, preparing me for roles in cybersecurity where protecting applications from threats is paramount.
