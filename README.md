# xss-security-notes
Notes and practical exercises from the TryHackMe Intro to Cross-Site Scripting (XSS) room, covering XSS types, exploitation techniques, and prevention methods.
Cross-Site Scripting (XSS) – Notes

Cross-Site Scripting (XSS) is a common web security vulnerability that allows attackers to inject malicious JavaScript into web pages viewed by other users. When a vulnerable application renders unsanitized user input in the browser, the injected script executes with the same privileges as the legitimate website. This can allow attackers to manipulate the page, steal sensitive information such as session cookies, or perform actions on behalf of the victim.

Types of XSS

Reflected XSS
Reflected XSS occurs when malicious input is immediately returned in the server’s response without proper validation or encoding. The payload is usually delivered through a crafted URL and executed when the victim visits the link.

Stored XSS (Persistent XSS)
Stored XSS happens when malicious input is permanently stored in a database (for example in comments, forums, or profile fields). When other users access the affected page, the payload is executed in their browsers.

DOM-Based XSS
DOM-based XSS occurs when client-side JavaScript processes user input insecurely within the browser’s Document Object Model (DOM), allowing the attacker’s code to execute without involving the server.

Potential Impact

Successful XSS exploitation can allow attackers to:

Steal session cookies and hijack user sessions

Perform actions on behalf of the victim

Modify or deface web content

Redirect users to malicious websites

Capture sensitive user information

Prevention Techniques

Developers can reduce XSS risks by implementing secure coding practices:

Proper input validation and sanitization

Output encoding before rendering user data

Implementing a Content Security Policy (CSP)

Using HttpOnly cookies to protect session data

Avoiding unsafe DOM manipulation

Learning Context

These notes are based on practical exercises completed in the TryHackMe “Intro to Cross-Site Scripting” room, where the concepts were explored through hands-on labs involving identifying, testing, and exploiting XSS vulnerabilities.
