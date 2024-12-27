# OWASP Juice Shop Attack Simulation Report

This repository contains the penetration testing report and associated scripts used for identifying vulnerabilities in the OWASP Juice Shop application. The project aims to simulate attacks and highlight potential security risks, along with recommendations for mitigation.

---

## Project Structure

### Files Included:

- **`OWASP_Juice_Attack_Report.docx`**
  - A comprehensive report detailing findings, methodologies, and recommendations from the penetration test.

- **Code Snippets Used in Testing:**

```html
<iframe src="javascript:alert(`xss` )">
```

```bash
ping -c 1 juice-shop.herokuapp.com
```

```bash
hydra -l admin@juice-sh.op -P /usr/share/wordlists/rockyou.txt 192.168.1.4 https-post-form "/rest/user/login:email=^USER^&password=^PASS^:F=Invalid email or password" -V -I
```

```bash
cd /usr/share/wordlists/
gunzip rockyou.txt.gz
```

```bash
dirb http://localhost:3000 /usr/share/wordlists/dirb/common.txt
```

---

## Tools Used

- **Hydra**: For brute-force password attacks.
- **Burp Suite**: For payload injection and vulnerability scanning.
- **OWASP ZAP**: For request analysis.
- **Dirb**: For directory enumeration.
- **Kali Linux**: As the testing environment.

---

## How to Use

1. **Install Required Tools:**
   Ensure the following tools are installed:
   - Hydra
   - Burp Suite
   - OWASP ZAP
   - Dirb

2. **Setup Testing Environment:**
   - Deploy OWASP Juice Shop locally or on a cloud environment.

3. **Execute Code Snippets:**
   - Use the code snippets provided in the report for testing specific vulnerabilities.

4. **Analyze Results:**
   - Refer to the `OWASP_Juice_Attack_Report.docx` for a detailed explanation of vulnerabilities and their impact.

---

## Recommendations

1. Enforce strict input validation and output encoding.
2. Implement account lockout mechanisms.
3. Secure critical paths with randomized URLs and access restrictions.
4. Conduct regular penetration testing and monitoring.

---

## References

- [OWASP Juice Shop Documentation](https://owasp.org/www-project-juice-shop/)
- [Kali Linux](https://www.kali.org/)

---

## Disclaimer

This project is intended for educational and ethical purposes only. Unauthorized testing or exploitation of applications without explicit permission is illegal and unethical.
