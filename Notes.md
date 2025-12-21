## OWASP API Top 10 (2023)
### Broken Object Level Authentication (BOLA)
An application or API fails to verify if a logged-in user has permission to access a specific data object (like a user profile, order, or file), allowing attackers to manipulate object IDs in requests (e.g., changing /orders/123 to /orders/124) to view, modify, or delete other users' sensitive data

Examples:
* [Coinbase - Change product id from Ethereum to Bitcoin](https://salt.security/blog/understanding-the-coinbase-api-vulnerability)

* [Peleton - No Authorization check for accessing all user info](https://salt.security/blog/the-peloton-api-security-incident-what-happened-and-how-you-can-protect-yourself)

#### Preventive Measures
1. Discuss Authorization rules during API design phase
2. Review Business requirements and define data access policies
3. Enforce Authorization controls at application logic layer
4. Implement Automated, pre-production testing to find BOLA flaws

### Broken Authentication
