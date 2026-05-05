# IT3040 ITPM Assignment 1 - Option 1
## Transliteration Accuracy Testing

This project automates negative test cases for the Pixelssuite Chat Sinhala transliteration function.

## Objective
Evaluate how accurately the application converts chat-style Singlish input into Sinhala output.

Target URL:
https://www.pixelssuite.com/chat-translator

## Test Case Coverage
The Excel file contains 50 negative test cases (`Neg_0001` to `Neg_0050`).

Coverage includes:
1. Question forms
2. Command forms
3. Greetings
4. Requests
5. Responses
6. Repeated words
7. Inputs with punctuation marks
8. Romanization / spelling variants
9. Isolated English word insertions in Singlish
10. Multi-word English phrases in Singlish
11. English digital terms in Singlish
12. Platform/app names in Singlish
13. English abbreviations/acronyms in Singlish
14. English clipped forms in Singlish
15. Place names embedded in Singlish
16. Person names embedded in Singlish
17. Inputs with numbers and numeric suffixes
18. Inputs with currency
19. Inputs with time formats
20. Inputs with dates
21. Inputs with unit of measurements
22. Inputs with slang and casual phrasing
23. Online identifiers in Singlish
24. Inputs containing emojis

Each input type is covered with at least two test cases.

## Prerequisites
Install:
- Python 3.11 or 3.12
- Google Chrome

## Installation
Open Command Prompt inside the extracted project folder and run:

```bash
pip install -U pip
pip install playwright openpyxl
playwright install
```

## How to Run the Automation
From the parent folder, run:

```bash
python test_automation.py --excel "Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

If you are running from outside the project folder, use the full path to the Excel file.

## Expected Workflow
1. Open `Assignment 1 - Test cases.xlsx`.
2. Confirm that `TC ID`, `Input length type`, `Input`, and `Expected output` are filled.
3. Run the Playwright script.
4. Reopen the Excel file.
5. Confirm that `Actual output` and `Status` are automatically filled.
6. Review failed/pass results and adjust expected outputs only if necessary.
7. Submit the full project folder as a ZIP file.

## Important Submission Notes
- Rename the final folder using your registration number.
- Rename required files using your registration number if instructed by CourseWeb.
- Add your public GitHub repository link to `repository_link.txt`.
- Make sure the GitHub repository is public before submission.
