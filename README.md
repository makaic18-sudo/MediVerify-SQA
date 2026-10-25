# MediVerify QA Testing

Manual QA testing of **MediVerify**, my final year project: a web app that checks whether a medicine is genuine or fake.

**App link:** https://mediverify-check.vercel.app

## About the app
Users can verify a medicine in two ways: by uploading an image of the back of the medicine, or by typing its code. The app shows the medicine name, expiry date and whether it is legit or fake. It also has sign up, login, an About page, and a history of previously verified medicines.

## What I did
- Wrote a **test plan** covering scope, approach, environment and exit criteria
- Wrote and executed **50 test cases** (positive, negative and boundary)
- Found and reported **13 bugs** with steps to reproduce, expected and actual results, and screenshots

## Results at a glance
- **Test cases executed:** 50
- **Passed:** 37
- **Failed:** 13
- **Bugs reported:** 13 (Critical: 1, High: 4, Medium: 6, Low: 2)

| Module | Total | Passed | Failed |
|---|---|---|---|
| Login | 7 | 7 | 0 |
| Sign Up | 7 | 7 | 0 |
| Code Verification | 8 | 3 | 5 |
| Image Upload | 8 | 7 | 1 |
| Result Display | 4 | 2 | 2 |
| History | 6 | 5 | 1 |
| About / Navigation | 4 | 1 | 3 |
| Session | 3 | 2 | 1 |
| UI / Compatibility | 3 | 3 | 0 |
| **Total** | **50** | **37** | **13** |

## Bugs found
| Bug | Module | Severity | Test case | Title |
|---|---|---|---|---|
| [BUG-001](bug-reports/BUG-001.md) | Code Verification | Critical | TC-016 | Fake medicine code is shown as legit |
| [BUG-002](bug-reports/BUG-002.md) | Session | High | TC-046 | Protected history is visible after logout when Back button is clicked |
| [BUG-003](bug-reports/BUG-003.md) | Code Verification | High | TC-022 | Same code gives inconsistent results when verified twice |
| [BUG-004](bug-reports/BUG-004.md) | Result Display | High | TC-032 | Expiry date is not displayed in the result |
| [BUG-005](bug-reports/BUG-005.md) | Result Display | High | TC-033 | Legit and Fake results look the same and are not clearly different |
| [BUG-006](bug-reports/BUG-006.md) | Code Verification | Medium | TC-019 | Leading and trailing spaces in the code are not trimmed |
| [BUG-007](bug-reports/BUG-007.md) | Code Verification | Medium | TC-021 | Code verification behaves differently for lowercase and uppercase codes |
| [BUG-008](bug-reports/BUG-008.md) | Code Verification | Medium | TC-017 | No validation message when the code field is empty |
| [BUG-009](bug-reports/BUG-009.md) | Image Upload | Medium | TC-024 | Result is not shown after uploading a PNG image |
| [BUG-010](bug-reports/BUG-010.md) | About / Navigation | Medium | TC-041 | About page is blank |
| [BUG-011](bug-reports/BUG-011.md) | About / Navigation | Medium | TC-042 | Navigation menu links do not open the correct pages |
| [BUG-012](bug-reports/BUG-012.md) | History | Low | TC-036 | History is not sorted newest first |
| [BUG-013](bug-reports/BUG-013.md) | About / Navigation | Low | TC-044 | Home page loads slowly |

## Key findings
- The most serious problem is that a **fake medicine code is shown as legit**, which defeats the purpose of the app.
- A logged-out user can still see **History data** by using the browser Back button.
- Most failures are in **Code Verification** (5 of 8 cases failed) and in the **About / Navigation** pages.

## Repository structure
```
mediverify-qa-testing/
├── README.md
├── test-plan/        Test plan (Word and PDF)
├── test-cases/       50 test cases with results (Excel and CSV)
├── bug-reports/      13 bug reports + a reusable template
└── screenshots/      Evidence for each bug
```

## Testing details
- **Type:** manual functional, negative, boundary, UI and basic security testing
- **Tools:** Excel / Google Sheets, browser developer tools, GitHub
- **Browsers:** Chrome, Edge, Firefox

## Author
**[Your Name]**
Aspiring SQA Engineer | [LinkedIn link] | [Email]
