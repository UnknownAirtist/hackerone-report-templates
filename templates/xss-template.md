# Cross-Site Scripting (XSS) Vulnerability Report

## Summary

A Cross-Site Scripting vulnerability was discovered in [AFFECTED COMPONENT/URL]. This vulnerability allows an attacker to inject malicious JavaScript code that executes in the context of other users' browsers.

**Vulnerability Type:** Cross-Site Scripting (XSS)  
**Severity:** [High/Medium/Low]  
**CVSS Score:** [Score] ([Vector String])

## Description

I discovered that the [PARAMETER/INPUT FIELD] in [PAGE/FUNCTIONALITY] is vulnerable to [Reflected/Stored/DOM-based] XSS. When a user submits specially crafted input containing JavaScript code, the application fails to properly sanitize this input before returning it in the response, allowing the injected script to execute.

## Steps to Reproduce

1. Navigate to [URL]
2. [DETAILED STEPS TO TRIGGER THE VULNERABILITY]
3. Observe that the JavaScript payload executes in the browser

### Proof of Concept Payload

```
[YOUR XSS PAYLOAD]
```

## Proof of Concept

[INCLUDE SCREENSHOTS OR SCREEN RECORDING SHOWING THE EXPLOIT]

Here's a simple proof of concept that demonstrates the vulnerability:

1. [STEP 1 WITH SCREENSHOT]
2. [STEP 2 WITH SCREENSHOT]
3. [FINAL RESULT SHOWING JS EXECUTION]

## Impact

An attacker exploiting this vulnerability could:

1. Steal users' session cookies and hijack their accounts
2. Perform actions on behalf of the victim
3. Access sensitive information displayed on the page
4. Redirect users to malicious websites
5. Modify the page content to conduct phishing attacks

## Affected Parameters/Inputs

- URL Parameter: [PARAMETER NAME]
- Input Method: [GET/POST/OTHER]
- Context: [HTML/JS/ATTRIBUTE/etc.]

## Affected Users/Roles

[DESCRIBE WHICH USERS ARE AFFECTED - All users, authenticated users, specific roles, etc.]

## Browser/Environment Information

- Browser: [BROWSER NAME AND VERSION]
- Operating System: [OS NAME AND VERSION]
- Additional relevant environment information: [ANY OTHER RELEVANT DETAILS]

## Mitigation Recommendation

To fix this vulnerability, I recommend:

1. Implement proper input validation and output encoding specific to the context where user input is displayed
2. Consider implementing a Content Security Policy (CSP) to provide defense in depth
3. Use framework-specific XSS protection mechanisms
4. Sanitize user input using a trusted library such as DOMPurify for client-side sanitization or an equivalent server-side library

## References

- [OWASP XSS Prevention Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html)
- [CWE-79: Improper Neutralization of Input During Web Page Generation](https://cwe.mitre.org/data/definitions/79.html)
- [Any other relevant references]