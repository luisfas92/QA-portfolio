This project documents a manual security assessment focused on authentication mechanisms and session cookie management in web applications.

Scope

The assessment included:

* Registration flow analysis
* Account activation process
* Password recovery mechanism
* Session cookie behavior
* Session persistence and reuse testing
* Client-side inspection using browser DevTools

The evaluation was conducted using a non-intrusive, exploratory testing approach aligned with OWASP principles.

Identified Issues

* Session cookie reuse vulnerability (Session Hijacking risk)
* Password recovery sending auto-generated credentials via email
* Absence of multi-factor authentication (2FA)
* Weak visibility of password policy requirements

Risk Classification

Vulnerabilities were classified based on impact and probability using a simplified risk matrix model.

Ethical Note

All tests were conducted in controlled environments for educational and portfolio purposes.
No exploitation, automated attacks, or harmful actions were performed.
