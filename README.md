# Day-50-100-Days-challenge-in-cybersecurity-
## Day 50: The Handshake - HTML & PHP Integration

### 📑 Overview
Today’s focus was on the relationship between frontend data collection and server-side processing. Understanding this "handshake" is vital for identifying web-based vulnerabilities.

### 🏗️ Conceptual Model: The Restaurant Analogy
* **HTML (The Menu):** Collects user input via forms and buttons. It is **stateless**, meaning it does not retain data after the page is left.
* **PHP (The Kitchen):** Processes the data, interacts with databases, and handles authentication logic.

### 📩 Data Transport Methods
| Method | Data Location | Security Profile | Use Case |
| :--- | :--- | :--- | :--- |
| **GET** | URL Parameters | **Low:** Visible in logs/history | Searches, Filters |
| **POST** | Request Body | **Higher:** Hidden from URL | Logins, Sensitive Data |

### 🛠️ Technical Deep Dive: Superglobals
* `$_GET`: Accesses data sent via URL. High risk for **XSS** if not sanitized.
* `$_POST`: Accesses data sent via request body. Primary target for **SQL Injection**.
* `$_REQUEST`: A "catch-all" variable. **Security Risk:** Can allow attackers to bypass POST-only restrictions by using GET parameters.

### 🔐 Security Implications for Ethical Hacking
1.  **Information Leakage:** Sensitive tokens exposed in GET URLs.
2.  **IDOR (Insecure Direct Object Reference):** Manipulating IDs in the URL to access unauthorized records.
3.  **Form Tampering:** Intercepting POST requests (via Burp Suite) to modify business logic, such as changing product prices.

---
*Progress: 50% Complete*
